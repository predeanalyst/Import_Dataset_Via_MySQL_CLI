# Import_Dataset_Via_MySQL_CLI
There are different ways to import a SQL file into a MySQL database, depending on the size and format of the file, and the operating system you are using. Here are some common methods:
●	Using the mysql command: This is the simplest and most widely used method. You can use the following syntax to import a SQL file into a database :mysql -u username -p database_name < file.sqlYou need to replace username, database_name, and file.sql with your own values. You will be prompted to enter your password after typing the command. Note that there is no space between -p and the password.If you are using Windows, you may need to change the directory to your MySQL/bin folder before executing the command. You can also use PowerShell with this syntax:cmd.exe /c "mysql -u username -p database_name < file.sql"
●	Using the source command: This method is useful if you are already in the interactive MySQL mode. You can use the following steps to import a SQL file into a database:You need to replace username, database_name, and file.sql with your own values. Make sure that the SQL file is in the same directory as MySQL, or use the full path of the file.
a.	Connect to MySQL via command line: mysql -u username -p
b.	Enter your password when prompted.
c.	Select the target database: use database_name
d.	Select your SQL file for import: source file.sql
●	Connect to MySQL via command line: mysql -u username -p
●	Enter your password when prompted.
●	Select the target database: use database_name
●	Select your SQL file for import: source file.sql
●	Using mysqldump: This method is usually used for making a backup of an entire database, but you can also use it to import a SQL file into a database. You can use the following syntax to dump a database into a SQL file:mysqldump db_name > backup-file.sqlYou need to replace db_name and backup-file.sql with your own values. You can then load the dump file back into the server with this syntax:mysql db_name < backup-file.sqlIf you are using Windows, you may need to use PowerShell with this syntax:mysql -p -u username database_name < backup-file.sql
