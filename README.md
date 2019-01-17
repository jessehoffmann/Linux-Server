# Linux-Server
This project took a base configuration of Linux and transformed it into a working server running Apache and PostgreSQL. The server is running the Catalog application that can be found here:
https://github.com/jessehoffmann/Catalog

## Requirements
A bash terminal is needed to ssh into the server

## Deployment
URL to the application is http://52.10.225.111.xip.io/.  
IP address is 52.10.225.111.  
SSH port is 2200.  
Server can only be accessed with SSH key.

## Software Installed
The following software was installed on the server:
* Apache2
* Flask
* libapache2-mod-wsgi
* PostgreSQL
* Git
* SQLAlchemy
* python-pip
* httplib2
* oauth2client
* Virtualenv

## Configuration
The following configuration changes were made:

1. Server packages were updated
2. Firewall was enabled to only allow incoming connections for SSH (port 2200), HTTP (post 80), and NTP (port 123).  
3. User "grader" was created and granted sudo permissions. Root user access was blocked
4. Password authentication was disabled and key based authentication forced. SSH key pair generated and a key authorization file was added in user "grader" home directory.
5. PSQL database server was initialized. User "catalog" was created and granted permissions for modifyfing application data.
6. Time zone set to UTC
7. Handle requests configured to serve wsgi application. Files modified include 000-default.conf and apache2.conf.
8. Enabled Virtual Host by adding specially configured catalog.conf file in /sites-available. Linked file to /sites-enabled with command "sudo a2ensite catalog.conf".
9. Cloned Item Catalog project from github and configured app to run properly from server.

## Resources
The following third-party resources were used to configure the server:
* libapache2-mod-wsgi
* PostgreSQL
* Virtual Host  
The follow resources helped bring this project to fruition:
* Amazon Lightsail
* xip.io

## Credit
Thank you to everyone at Udacity for helping me get here!

## License
This project is public domain.
