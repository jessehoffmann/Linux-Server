# Linux-Server
This project took a base configuration of Linux and transformed it into a working server running Apache and PostgreSQL. The server is running the Catalog application that can be found here:
https://github.com/jessehoffmann/Catalog
## Requirements
A bash terminal is needed to ssh into the server
## Deployment
URL to the application is http://52.10.225.111.xip.io/  
IP address is 52.10.225.111  
SSH port is 2200  
Server can only be accessed with SSH key
## Configuration
Firewall was enable to only allow incoming connections for SSH (port 2200), HTTP (post 80), and NTP (port 123).  
Password authentication disabled and key based authentication forced.  

The following software was installed on the server:
* Apache2
  * Modified 000-default.conf, apache2.conf
* Flask
* libapache2-mod-wsgi
* PostgreSQL
  * Added user and modified permissions for web app
* Git
* SQLAlchemy
* python-pip
* httplib2
* oauth2client

## Resources
The following third-party resources were used to complete this project:
* Amazon Lightsail
