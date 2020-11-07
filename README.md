# Email Exchange
- Check out the 'exchangelib' python package.  It can send/receive mail with your exchange mailbox.  
-	The first thing to do is test that autodiscover actually works for your account. You can do this at https://testconnectivity.microsoft.com
-	If that works, you'll need to enable debug logging in exchangelib and compare the autodiscover steps in the debug output with the steps
-	performed in the report you get from https://testconnectivity.microsoft.com, to see where we're failing.
-	Testing inbound SMTP mail flow for domain 'lee19856@gmail.com'. Inbound SMTP mail flow was verified successfully.
-	Or if you try with company email, then select ‘Outlook Autodiscover’ and run test.
-	pip install beautifulsoup4

# Flask
-	C:\work\flask
-	Set flask_app=hello.py
-	Flask run

# Django
- Folder - C:\work\caseview
-	mailauth.txt @ c:\Users\yjunlee (don't use this way)

- Python manage.py makemigrations
- Python manage.py migrate
- Python manage.py runserver
- add this to supported IP list in setting file - case.qualcomm.com:8000
-	python manage.py runserver case.qualcomm.com:8000

- You have to make sure
-	python path is properly set in window path
-	mysqlclient is installed (if you set default DB as mysql), create database <make db name same as foler name>

# Apache + PHP + MySQL
-	C:\Apache
-	C:\Apache\htdocs
-	C:\php
-	C:\MySQL à Mysql -u root -p
-	type localhost in browser
# MYSQL
- If you use MySQL 5.7.6 and later:
- ALTER USER 'root'@'localhost' IDENTIFIED BY 'MyNewPass';
- If you use MySQL 5.7.5 and earlier:
- SET PASSWORD FOR 'root'@'localhost' = PASSWORD('MyNewPass');

# phpMyAdmin
-	C:\Apache\bin\ApacheMonitor.exe
-	type localhost in browser
-	click phpMyAdmin-4.8.3-all-languages/
-	ID: root
-	PW: <your password>

# Changing Domain
-	C:\Windows\System32\drivers\etc
-	Edit hosts
```
Copy to somewhere else since it won’t allow changing it directly
Edit
127.0.0.1 case.com
127.0.0.1 www.case.com
Copy back to original folder
```
-	C:\Apache\conf\extra
-	Open httpd-vhosts.conf
-	Add this at the bottom..(but not sure this is taking an effect or not)
```
<VirtualHost *:80>
    ServerName www.case.com
    ServerAlias case.com
    DocumentRoot C:/work/djangoproject/posts
</VirtualHost>
```
-	Restart apache server

# C Compile Setup
-	Nano input file name.cpp
-	GNU nano 2.2.6 window will pop up
-	Start typing the code
-	After writing the code, press ctrl+O and hit enter to save the file
-	To exit, ctrl+x
-	To compile, g++ hello.cpp -0 hello
-	To execute program, ./hello
