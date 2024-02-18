# WEB STACK IMPLIMENTATION

## Introduction to web stack

*What is web stack*, a web stack which is also known as a web application is a type of solution stack, or a compilation of software applications. it is used for performing special tasks when developing and implementing websites.

### *Some components of web stack are*
   - Operating system
   - Web server
   - Data base
   - Programing language

The operating system is the central interface between the hardware and the software components
Web wserver delivers the required documents requested for by the cliant
Database is used to store volumes of data needed for the project
The programing language provides the cliant with dynamic web application websites.

## Types of Web Stack

   - JavaScript
   - CSS
   - HTML
   - Python
   - Frameworks
   - Lemp stack

   ## LAMP STACK

   ### *What is lamp stack*? 
   it is a combination of 4 software technologies used to build websites and web application.
   - MySQL (managesa and stores data)
   - Apache (a web server that handles HTTP and deliver content to client)
   - Linux (provides the operating system)
   - PHP  (a server-side scripting language)

## WORKING WITH LEMP STACK

1) Lunch an Ubuntu Instance on AWS console and SSH into from your terminal

![ols](images/mintty_xY40ElqG4m.png)

ssh into ubuntu Ec2 instance
   - ssh -i path/to/.pem ubuntu@public_ip address

2)  Install Apache2

### Updatu local package list

it is important to first update the server, and if there are any upgrades required, they also should be attended to. the commands needed are
  - sudo apt update
  - sudo apt upgrade

### Install Apache2 web server

What is apache2 ? it is a free and open-source cross-platform web server software, it is responsible for accepting HTTP requests from visitors and sending them back the requested information in the form of web pages or in simpiler terms. it allows visitors to view content on your website. the command used to install apache2 is,
  - sudo apt install apache2

once the installation is done, you can confirm if it is up and running by running this command,
  - sudo systemctl status apache2

At this point you can test to see if your ip adderess is functional by opening a web page of choice and type in the ip adderess
- http://public ip address:80

![y](images/msedge_bxfQIrEhrg.png)

this should be the result you get after searching the web using your IP adderess

## Installing mysql

 MySql is a cliant/server system that consists of a multithreaded SQL server that supports different back ends. several different cliant programs and libraries, administrative tools, and a wide rang of application-programimng interface

here are the commands used to setup MySqlserver on aws ec2

   - update the system
      "sudo apt update"
   - Install MySql
      "sudo apt install mysql-server
   - check status
      "sudo systemctl status mysql
   - login as root user
      "sudo mysql
   - Update password
      "ALTER USER "root"@"localhost" IDENTIFIED WIH mysql native password BY "insert password";

   ![oafj](images/mintty_Kn69NIZl9O.png)

## Installing PHP

First of what really is php? it isa general purpose scripting language geared towards web development. It was originally created in 1993 and released in 1995. it is used in various veb applications like e-commerce websites to crm systems like hubspot and salesforce

install php-fpm, and tell Nginx to pass PHP requests to this software for processing. then we need php-mysql to communicate with MySQL-based databases. Core PHP packages will automatically be installed as dependencies.

    sudo apt install php-fpm php-mysql -y

To confirm the version of php, run this command
 - php -v

 ![ij](images/mintty_gHupyyzcNi.png)

   Configuring Nginx to Use PHP Processor

configuring Nginx to use PHP as a processor, set up the FastCGI process manager (PHP-FPM) then configure Nginx to send PHP requests to PHP-FPM.
create a folder called projectLEMP for our webserver. Create the root web directory for your_domain in /var/www/ folder as follows:

sudo mkdir /var/www/projectLEMP
Next, assign ownership of the directory with the $USER environment variable, which will reference your current system user:

  $ sudo chown -R $USER:$USER /var/www/projectLEMP
Open a new configuration file in Nginx’s sites-available directory

  $ sudo nano /etc/nginx/sites-available/projectLEMP

  After editing, save and close the file.

Lets activate the configuration by linking the config file from Nginx’s sites-enabled directory, This will tell Nginx to use the configuration next time it is reloaded:

  $ sudo ln -s /etc/nginx/sites-available/projectLEMP /etc/nginx/sites-enabled/


## php, nginx, mysql
All at this point have been installed sucessfully.

### Lets enable php on the website

disable default Nginx host that is currently configured to listen on port 80, for this run:

  sudo unlink /etc/nginx/sites-enabled/default
reload NGINX to apply these changes.

  sudo systemctl reload nginx
Create an index.html file in the location /var/www/projectLEMP so that we can test that your new server block works as expected:

sudo echo 'Hello LEMP from hostname' $(curl -s http://169.254.169.254/latest/meta-data/public-hostname) 'with public IP' $(curl -s http://169.254.169.254/latest/meta-data/public-ipv4) > /var/www/projectLEMP/index.html

try to open your website URL from the browser using IP address or DNS name:

The LEMP stack is now fully configured. In the next step, we’ll create a PHP script to test that Nginx is in fact able to handle .php files within our newly configured website.

   Testing Nginx With PHP

we can do this by creating a test PHP file in our document root. let's open a new file called info.php:

![ouh](images/msedge_AJWgLaI2fO.png)






