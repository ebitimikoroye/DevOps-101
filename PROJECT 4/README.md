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

