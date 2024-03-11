# Understanding Client Server Architecture With MySQL As RDBMS

## Introduction

 What is client-server architecture?

it's a computing model that divides the functionality of a system into two distinct roles: clients and servers. The client-server architecture refers to a system that hosts, delivers, and manages most of the resources and services that the client requests.    Requests and services are delivered over a network, and it is also referred to as the networking computing model or client server network. Alternatively called a client-server model, is a network application that breaks down tasks and workloads between clients and servers that reside on the same system or are linked by a computer network.

Client-server architecture typically features multiple users’ workstations, PCs, or other devices, connected to a central server via an Internet connection or other network. The client sends a request for data, and the server accepts and accommodates the request, sending the data packets back to the user who needs them. 

![OIDVF](images/client-ser.png)

## Prerequisites

1 - Basic knowledge of at least one programming language.
2 - A server infrastructure to host the MySQL server and the client application.
3 - Familiarity with SQL.
4 - Know t basic Linux commands and knowledge of Linux server management
5 - Install and set up MySQL on your Linux server.

a quick example of client server

![gfhgfh](images/WindowsTerminal_lpFxJqUBF8.png)

## Deploying a Client-Server using MySQL

Follow the below steps to implement a basic client-server architecture using MySQL RDBMS.

Create and configure two Linux-based virtual servers (EC2 instances in AWS). This involves creating two security groups that allow SSH connections on port 22. These instances will be launched in the default VPC. 

## Implementing MySQL as a Client Server Architecture

Step 1: Launch 2 EC2 Instances on AWS

i. Each instance should be named

Instance 1 - mysql server

Instance 2 - mysql client

ii. Open 2 terminals and ssh into both "mysql server" "mysql client"

For windows users, open command prompt, powershell or git bash
For mac and linux users, open a terminal and ssh into the instance

Step 2: Updating and Upgrading Package Lists and Apt Repositories
On both mysql server and mysql client update and upgrade package lists

sudo apt update -y && sudo apt upgrade -y
Note: The command above should be executed for mysql server and mysql client instances

Step 3: Installing MySQL Server Software
On mysql server instance install MySQL Server software.

sudo apt install mysql-server -y

![yffgh](images/mintty_X9RBfbiw17.png)


