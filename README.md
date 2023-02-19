# MySQL-Python-connector-fetch-data
 
 Python MySQL Tutorial. Part 1
 
 
![Python-MySQL](https://user-images.githubusercontent.com/29576337/218214260-74a464a4-37f0-4faf-8e87-2939b7fba672.png)

In this section, you’ll learn how to connect to MySQL database and perform common database operations such as SELECT in Python. Also you'll get started with MySQL Python connector by learning about the MySQL Python connector’s features and how to install it on your system.

Full tutorial in >> https://www.mysqltutorial.org/python-mysql/

MySQL Connector/Python versions
You will need to install the correct versions of Python, MySQL, and Connect/Python. The following table illustrates the compatible versions of Connect/Python, MySQL, and Python:
![MySQL Connector Python versions](https://user-images.githubusercontent.com/29576337/218214528-38a8a3f1-cccc-46ff-9307-4e0d197e7f98.png)



How to Connect to MySQL Database in Python

Install MySQL connector module
Use the pip command to install MySQL connector Python.
pip install mysql-connector-python

Import MySQL connector module
Import using a import mysql.connector statement so you can use this module’s methods to communicate with the MySQL database.

Use the connect() method
Use the connect() method of the MySQL Connector class with the required arguments to connect MySQL. It would return a MySQLConnection object if the connection established successfully

Use the cursor() method
Use the cursor() method of a MySQLConnection object to create a cursor object to perform various SQL operations.

Use the execute() method
The execute() methods run the SQL query and return the result.

Extract result using fetchall()
Use cursor.fetchall() or fetchone() or fetchmany() to read query result.

Close cursor and connection objects
use cursor.close() and connection.close() method to close open connections after your work completes

GoTo >> https://pynative.com/python-mysql-database-connection/

![image](https://user-images.githubusercontent.com/29576337/218215893-6180069b-9d1c-47f1-b9cb-7dad604bcab8.png)


Setting up a sample database
MySQL Python Connect
First, download the following  python_mysql database, uncompress the file and copy it to a folder such as C:\mysql\python_mysql.sql :

Download Python MySQL Sample Database >> /python_mysql.zip

Next, log in to MySQL Server using mysql tool:

mysql -u root -p
Code language: SQL (Structured Query Language) (sql)
Enter the password for the root user.

Enter password: ********
Code language: SQL (Structured Query Language) (sql)
Then, create a new database named  python_mysql:

mysql>create database python_mysql;
Code language: SQL (Structured Query Language) (sql)
After that, select the database python_mysql:

mysql>use python_mysql;
Code language: SQL (Structured Query Language) (sql)
Finally, use this command to load data from the file:

mysql> source c:\mysql\python_mysql.sql
Code language: SQL (Structured Query Language) (sql)
To double-check the loading, use the SHOW TABLES command to list all the tables from the python_mysql database:

mysql> SHOW TABLES;
Code language: SQL (Structured Query Language) (sql)
The output will be:

+------------------------+
| Tables_in_python_mysql |
+------------------------+
| authors                |
| book_author            |
| books                  |
+------------------------+
3 rows in set (0.01 sec)
