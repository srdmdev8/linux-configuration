# FSWD Linux Configuration Project


## Linux Configuration Overview
I used Amazon's Lightsail Web Services to deploy my application. I had to configure
the server from scratch and did the following:
- Updated all currently installed packages
- Configured the Uncomplicated Firewall (UFW):
  - SSH (Port 22)
  - TCP (Port 2200)
  - HTTP (Port 80)
  - UDP/NTP (Port 123)
- Created a new user named "grader" and provided them with sudo permissions
- Created an SSH key pair for "grader" using `ssh-keygen`
- Installed and configured PostgreSQL
- Installed Git
- Installed Apache
  - Configured apache's config file in order for my application to deploy
- Installed `pip` in order to install several modules needed for my
application to run properly
- Installed `mod-wsgi` in order to use WSGI to run my application
  - Had to re-configure some code in my "gameCatalog.py" file in order to successfully
  run my application

## App Overview
This project utilizes the Flask microframework to run my console and game catalog
and the SQLAlchemy toolkit to connect to my database. The initial database
was created from scratch. This catalog displays all the available consoles and
provides options to view games from each console, add a new console, and
edit/delete consoles. If you select to view the games of a specific console, you
will see a list of all applicable games for that console. You will also have
options to add a new game and edit/delete games.  

A login/logout authentication process has also been implemented using Google's
OAuth 2.0 API. There will be two ways to login: Facebook and Google. The provided
Python script has logic to prevent access to certain features if you are not
logged in. For example, the modification options mentioned above will be
unavailable until you have been successfully logged in, providing more of a
"read-only" type view.

## Accessing the Server
To access the server of my project you will need the following information:
- Static IP Address: **34.218.2.98**
- SSH Port: **22**

## Running the Program
Using your favorite web browser, go to this URL: http://34.218.2.98

Now you are ready to navigate through my console and game catalog. Thank you for
checking out my Linux Configuration Project!

## Third-Party Resources Used
- Amazon Lightsail to host my applications server and deploy it on the Web
- PuTTY and PuTTYgen to convert the .pem file of my private key to a .ppk file as
well as remote login to my server
