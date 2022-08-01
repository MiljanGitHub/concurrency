1. Position to project directory
2. Create volumes directory: **mkdir db**
3. Run command: **docker run -d --name transactions_container -v %cd%\db:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=transactions -p 3307:3306 mysql:5.7.39**
4. Open new terminal and run following commands to get to a database container terminal session:
   1. **docker container exec -it transactions-container bash**
   2. **mysql -u root -p**
   3. **use transactions**
5. Optionally, you may use database client, such as DBeaver, to connect to database.

Note: In step 3. '%cd%\db' is a Windows version, while for Linux '$(pwd)/db'. Or it b can be replaced with any valid directory on your system.