# Python - Object-relational mapping

# Before you start…
Please make sure your MySQL server is in 8.0 -> <a href = "https://alx-intranet.hbtn.io/projects/272">How to install MySQL 8.0 in Ubuntu 20.04</a>

# Background Context
In this project, you will link two amazing worlds: Databases and Python!
In the first part, you will use the module MySQLdb to connect to a MySQL database and execute your SQL queries.
In the second part, you will use the module SQLAlchemy (don’t ask me how to pronounce it…) an Object Relational Mapper (ORM).
The biggest difference is: no more SQL queries! Indeed, the purpose of an ORM is to abstract the storage to the usage. With an ORM, your biggest concern will be “What can I do with my objects” and not “How this object is stored? where? when?”. You won’t write any SQL queries only Python code. Last thing, your code won’t be “storage type” dependent. You will be able to change your storage easily without re-writing your entire project.

# Resources
* <a href = "https://www.fullstackpython.com/object-relational-mappers-orms.html">Object-relational mappers</a>
* <a href = "https://mysqlclient.readthedocs.io/">mysqlclient/MySQLdb documentation </a> please don't pay attention to msql
* <a href = "https://www.mikusa.com/python-mysql-docs/index.html">MySQLdb tutorial</a>
* <a href = "https://docs.sqlalchemy.org/en/13/orm/tutorial.html">SQLAlchemy tutorial</a>
* <a href = "https://docs.sqlalchemy.org/en/13/">SQLAlchemy</a>
* <a href = "https://github.com/PyMySQL/mysqlclient">mysqlclient/MySQLdb</a>
* <a href = "https://www.youtube.com/watch?v=woKYyhLCcnU">Introduction to SQLAlchemy</a>
* <a href = "https://www.youtube.com/playlist?list=PLXmMXHVSvS-BlLA5beNJojJLlpE0PJgCW">Flask SQLAlchemy</a>
* <a href "http://alextechrants.blogspot.com/2013/11/10-common-stumbling-blocks-for.html">10 common stumbling blocks for SQLAlchemy newbies</a>
* <a href = "https://www.pythonsheets.com/notes/python-sqlalchemy.html">Python SQLAlchemy Cheatsheet</a>
* <a href = "https://auth0.com/blog/sqlalchemy-orm-tutorial-for-python-developers/">SQLAlchemy ORM Tutorial for Python Developers</a>Warning: This tutorial is with PostgreSQL, but the concept of SQLAlchemy is the same with MySQL
* <a href = "https://overiq.com/sqlalchemy-101/">SQLAlchemy Tutorial</a>

# Learning Objectives
At the end of this project, you are expected to be able to <a href = "https://fs.blog/feynman-learning-technique/">explain to anyone</a>without the help of Google:

# General
* Why Python programming is awesome
* How to connect to a MySQL database from a Python script
* How to SELECT rows in a MySQL table from a Python script
* How to INSERT rows in a MySQL table from a Python script
* What ORM means
* How to map a Python Class to a MySQL table

# Requirements

#General
* Allowed editors: vi, vim, emacs
* All your files will be interpreted/compiled on Ubuntu 20.04 LTS using python3 (version 3.8.5)
* Your files will be executed with MySQLdb version 2.0.x
* Your files will be executed with SQLAlchemy version 1.4.x
* All your files should end with a new line
* The first line of all your files should be exactly #!/usr/bin/python3
* A README.md file, at the root of the folder of the project, is mandatory
* Your code should use the pycodestyle (version 2.8.*)
* All your files must be executable
* The length of your files will be tested using wc
* All your modules should have a documentation (python3 -c 'print(__import__("my_module").__doc__)')
* All your classes should have a documentation (python3 -c 'print(__import__("my_module").MyClass.__doc__)')
* All your functions (inside and outside a class) should have a documentation (python3 -c 'print(__import__("my_module").my_function.__doc__)' and python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)')
* A documentation is not a simple word, it’s a real sentence explaining what’s the purpose of the module, class or method (the length of it will be verified)
* You are not allowed to use execute with sqlalchemy

# Tasks
# Get all states
Write a script that lists all states from the database hbtn_0e_0_usa:
* Your script should take 3 arguments: mysql username, mysql password and database name (no argument validation needed)
* You must use the module MySQLdb (import MySQLdb)
* Your script should connect to a MySQL server running on localhost at port 3306
* Results must be sorted in ascending order by states.id
* Results must be displayed as they are in the example below
* Your code should not be executed when imported

# Filter states
Write a script that lists all states with a name starting with N (upper N) from the database hbtn_0e_0_usa:
* Your script should take 3 arguments: mysql username, mysql password and database name (no argument validation needed)
* You must use the module MySQLdb (import MySQLdb)
* Your script should connect to a MySQL server running on localhost at port 3306
* Results must be sorted in ascending order by states.id
* Results must be displayed as they are in the example below
* Your code should not be executed when imported

# Filter states by user input
Write a script that takes in an argument and displays all values in the states table of hbtn_0e_0_usa where name matches the argument.
* Your script should take 4 arguments: mysql username, mysql password, database name and state name searched (no argument validation needed)
* You must use the module MySQLdb (import MySQLdb)
* Your script should connect to a MySQL server running on localhost at port 3306
* You must use format to create the SQL query with the user input
* Results must be sorted in ascending order by states.id
* Results must be displayed as they are in the example below
* Your code should not be executed when imported

# SQL Injection...
Wait, do you remember the previous task? Did you test "Arizona'; TRUNCATE TABLE states ; SELECT * FROM states WHERE name = '" as an input?

# Cities by states
Write a script that lists all cities from the database hbtn_0e_4_usa
* Your script should take 3 arguments: mysql username, mysql password and database name
* You must use the module MySQLdb (import MySQLdb)
* Your script should connect to a MySQL server running on localhost at port 3306
* Results must be sorted in ascending order by cities.id
* You can use only execute() once
* Results must be displayed as they are in the example below
* Your code should not be executed when imported

# All cities by state
Write a script that takes in the name of a state as an argument and lists all cities of that state, using the database hbtn_0e_4_usa
* Your script should take 4 arguments: mysql username, mysql password, database name and state name (SQL injection free!)
* You must use the module MySQLdb (import MySQLdb)
* Your script should connect to a MySQL server running on localhost at port 3306
* Results must be sorted in ascending order by cities.id
* You can use only execute() once
* The results must be displayed as they are in the example below
* Your code should not be executed when imported


