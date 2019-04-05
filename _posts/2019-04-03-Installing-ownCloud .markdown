---
layout: default
title:  "Installing ownCloud"
nav_order: 2
---



# Installing ownCloud 

This chapter includes the following information:
- Installation Prerequisites
- Installing ownCloud
**Note:** 
Before you start installing ownCloud <latest version>, ensure all the system requirements and deployment recommendations are considered. For more information, see, System Requirement and Deployment Recommendations

## Installation Prerequisites

Following are the prerequisites for installing ownCloud:
1.	Install Apache 2 to use ownCloud on a Web server. For more information, see, Installing Apache 2 on Ubunto
2.	Install Maria DB. For more information, see, Installing Maria DB
3.	Install PHP and its related modules. For more information, see, Installing PHP and related modules.
4.	Create ownCloud database, to store the required files on ownCloud. For more information, see, Creating ownCloud database
5.	Download the latest version of ownCloud in the Apache 2 directory: /var/www/html/ownCloud/.
 For more information, see, Downloading ownCloud.
6.	Configure Apahce2 site configuration file for ownCloud. For more information, see, Configuring Apache 2 site configuration file for ownCloud
7.	Enable the ownCloud and rewritable module after configuring the Virtual Host. For more information, see, Enabling ownCloud and Rewriting the module.
8.	Restart Apache 2 to apply all the settings. For more information, see, Restarting Apache 2.

## Installing ownCloud

The ownCloud installer is available in the Apache 2 root directory /var/www/html/ownCloud/. You must run the installation wizard and accept the end user license agreement to proceed with the ownCloud installation.
***To install ownCloud:
1.	Open the browser and browse the **Server domain name**.
2.	Click **Install ownCloud** <latest version> setup.
3.	Follow the instruction of ownCloud setup wizard to complete the ownCloud installation.

### Installing Apache 2 on Ubunto

***To install Apache 2 on Ubunto:
1.	Run the following command to install Apache 2:
sudo apt install apache2
2.	Run the following command to disable the directory listing:
sudo sed -i "s/Options Indexes FollowSymLinks/Options FollowSymLinks/" /etc/apache2/apache2.conf
3.	Run the following command to enable Apache 2 Service during server Start and Stop, and reboot:
sudo systemctl stop apache2.service
sudo systemctl start apache2.service
sudo systemctl enable apache2.service

### Installing Maria DB

***To install Maria DB:
1.	Run the following command:
sudo apt-get install mariadb-Server mariadb-client
2.	Run the following command to and enable Maria DB service during server Start, Stop, and reboot:
sudo systemctl stop mariadb.service
sudo systemctl start mariadb.service
sudo systemctl enable mariadb.service
3.	Run the following command to secure Maria DB Server:
4.	Run the following command to restart MariaDB Server:
sudo systemctl restart mariadb.service


### Installing PHP and related modules

***To install PHP and related modules:
- Run the following command to install PHP and related modules:
sudo apt install php libapache2-mod-php php-common libapache2-mod-php php-mbstring php-xmlrpc php-soap php-apcu php-smbclient php-ldap php- redis php-gd php-xml php-intl php-json php-imagick php-mysql php-cli php-mcrypt php-ldap php-zip php-curl


### Creating ownCloud database

*** To create ownCloud database:
1.	Run the following command to login to the Database Server, and enter the root password provided during Maria DB installation:
sudo mysql -u root -p
2.	Run the following command to create ownCloud Database:
CREATE DATABASE ownCloud
3.	Run the following command to create **ownClouduser** database user with a new password:
CREATE USER 'ownClouduser'@'localhost' IDENTIFIED BY ‘new_password_here'
4.	Run the following command to grant full access to the database:
GRANT ALL ON ownCloud.* TO 'ownClouduser'@'localhost' IDENTIFIED BY 'user_password_here' WITH GRANT OPTION
5.	Run the following command to **Save** and **Exit**:
FLUSH PRIVILEGES
EXIT


### Downloading ownCloud 

*** To download latest version of ownCloud:
1.	Run the following command to extract latest version of ownCloud downloaded file in the Apache 2 root directory:
cd /tmp && wget https://download.ownCloud.org/community/ownCloud-10.0.10.zip
unzip ownCloud-10.0.10.zip
sudo mv ownCloud /var/www/html/ownCloud/
2.	Run the following command to set the correct permissions for ownCloud:
sudo chown -R www-data:www-data /var/www/html/ownCloud/
sudo chmod -R 755 /var/www/html/ownCloud/


### Configuring Apache 2 site configuration file for ownCloud 

*** To configure Apache 2 site configuration file for ownCloud:
1.	Run the following command to create a new **ownCloud.conf** configuration file:
sudo nano /etc/apache2/sites-available/ownCloud.conf
2.	Paste the following in the **ownCloud.conf** configuration file and **Save**. Paste the below content in the file and **Save** and **Exit**:
	**Note:**
	Enter your domain name and directory root location.
<VirtualHost *:80>
ServerAdmin admin@example.com
DocumentRoot /var/www/html/ownCloud/
ServerName example.com
ServerAlias www.example.com

Alias /ownCloud "/var/www/html/ownCloud/"

<Directory /var/www/html/ownCloud/>
Options +FollowSymlinks
AllowOverride All
Require all granted
  <IfModule mod_dav.c>
     Dav off
 </IfModule>
SetEnv HOME /var/www/html/ownCloud
SetEnv HTTP_HOME /var/www/html/ownCloud
</Directory>
ErrorLog ${APACHE_LOG_DIR}/error.log
CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
Enabling ownCloud and Rewriting the module
To enable ownCloud and rewriting the module:
- Run the following command, once the virtual host is configured:
sudo a2ensite ownCloud.conf
sudo a2enmod rewrite
sudo a2enmod headers
sudo a2enmod env
sudo a2enmod dir
sudo a2enmod mime
For more information on configuring virtual host, refer, Configuring Apache 2 site configuration file for ownCloud


### Restarting Apache 2
*** To restart apache 2:
- Run the following command to apply all the settings:
sudo systemctl restart apache2.service
