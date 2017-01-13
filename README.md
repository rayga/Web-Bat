# Web-Bat

Download DVWA
apt-get install mysql-server
apt-get install unzip apache2 php5 php5-mysql php-pear
Copy DVWA file to /var/www/html
nano dvwa/config/config.inc.php
change database password $_DVWA[ 'db_password' ] = 'p@ssw0rd';
Change allow_url_include = Off become On
in /etc/php5/apache2/php.ini

chmod -R 777 /var/www/html/dvwa to make file Writeable

root@ubuntu:~# mysql -u root -p

Enter Password: [your mysql password]

root@ubuntu:~# create database dvwa;

root@ubuntu:~# exit

root@ubuntu:~# nano /etc/apache2/apache2.conf

add in the bottom line "ServerName localhost"
service apache2 start
http://192.168.0.20/dvwa/setup.php

http://192.168.0.20/dvwa/setup.php
