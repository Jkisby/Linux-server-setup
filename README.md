# Linux-server-setup
Linux server configuration for book app hosted on AWS
---
## Server details
Server is hosted at 35.167.154.195 on port 2200

Complete URL: http://ec2-35-167-154-195.us-west-2.compute.amazonaws.com/

Runs bookalot python app through Flask framework, using postresql database. 

## Configuration Changes

### Users
Add 'grader' user with sudo and block root access

### Login
Password login disabled and SSH key added for grader

### Fix sudo: unable to resolve host error
Solution from <a href="http://askubuntu.com/questions/59458/error-message-when-i-run-sudo-unable-to-resolve-host-none">here</a>

### TimeZone
Set timezone to UTC

### Firewall configuration
SSH port changed to 2200

UFW configured to allow incoming connections for SSH on port 2200, HTTP on port 80, NTP on port 123

### Apache
Install Apache2 with mod-wsgi

Install Postresql, Flask, SQLAlchemy

### Install git
Bookalot app cloned from github and uses virtual environment

bookalot.wsgi created

### Login Authentication
Client_id and client_secret updated for google and facebook login

### System monitoring

<a href="https://pypi.python.org/pypi/Glances">Glances</a> installed for system monitoring

