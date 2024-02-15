# WEB STACK IMPLIMENTATION (LAMP STACK)

First of, what is web stack? it is the collection of software used for web development that incoperates, at a minimum, an operating system (OS), a programming language, database software and aweb server. it is also a type of solution stack.
There are different web servers that can be used to implement a web stack
  - Nginx
  - Apache tomcat
  - Lighttpd
  - Jetty
  - Caddy

This project will be done using a number of tools such as 
Nginx, Git bash, AWS,

First step is to install the various tools, then open your git bash terminal,next CD downloads and run this command to switch from your local host
ssh -i <Your-private-key.pem> ubuntu@<EC2-Public-IP-address>

![alt text](images/mintty_qtj0k0IJBc.png)

## Installing NGINX Web server

NGINX is an opensource high performance HTTP server and reverse proxy, installing nginx can be done using this command

- sudo apt update
- sudo apt install nginx

![uh](images/msedge_fXWsgW2oqG.png)

to check the installation suceeded and to know the status, use this command
- sudo systemctl status nginx

OPpen a TCP port 80. to achieve this we will have to use our EC2 on our aws, by defult we have TCP port 22 running on our EC2, we will have to add a rule to the configuration to open inbound connection through port 80

![yg](images/msedge_n4CaW4ZqMR.png)

once this i done, we will need to test to see how it will respond to request from the internet,
to confirm this run the following command

http://<Public-IP-Address>:80
curl -s http://169.254.169.254/latest/meta-data/public-ipv4
 
both commands practically do thesame thing

![ca](images/msedge_1ubHnzbpCA.png)

## Installing MYSQL

Installing mysql which is a client/server system that consist of a multithreaded SQL server that supports different back ends, several client programs and libraries, administrative tools and a whole range of applications-programining interfaces.

the command used to install mysql
- $ sudo apt install mysql-server

after installing the command used to log into it is
- $ sudo mysql

![rw](images/msedge_IRqIWLZQRW.png)

Running a security script that comes pre-installed will remove some incure defult settings.first setup a password using this command
- ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';

After following the process of instalation, you can test if you are able to log into mysql by running this command, password will be required.
- $ sudo mysql -p

After login is successful, its time to logout, to achieve that, run the following command 
- mysql> exit

## INSTALLING PHP

PHP will be installed to process codes and generate dynamic content for the web server. two installations will come in handy 
 - PHP-PFM
 - PHP-MYSQL

 To run both instalations at once run this command
 $ sudo apt install php-fpm php-mysql

After installing both php-pfm and php-mysql, you will then configure nginx to use php processor.

## CONFIGURING NGINX TO USE PHP PROCESSOR

We can use NGINX to create server blocks to encapsulate configration details and host more than one domain on a single server. By defult, nginx 20.04 has one server block /var/www/html. it is difficult using it to host multiple sites, lets create a drictory structure within www/html.

To achieve that we will use this command
 - $ sudo mkdir /var/www/projectLEMP

next is to assigne ownership of the directory using this command
 - $ sudo chown -R $USER:$USER /var/www/projectLEMP

use this command to open a new configration file in NGINX
 - $ sudo nano /etc/nginx/sites-available/projectLEMP




