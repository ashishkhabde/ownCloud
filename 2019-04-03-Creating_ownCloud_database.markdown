---
layout: default
title:  "Creating ownCloud database"
nav_order: 4
parent: "Installation Prerequisites"
---


### Creating ownCloud database

*** To create ownCloud database:**
1.	Run the following command to login to the Database Server, and enter the root password provided during Maria DB installation: <br>`sudo mysql -u root -p`
2.	Run the following command to create ownCloud Database: <br>`CREATE DATABASE ownCloud`
3.	Run the following command to create **ownClouduser** database user with a new password: <br>`CREATE USER 'ownClouduser'@'localhost' IDENTIFIED BY ‘new_password_here'`
4.	Run the following command to grant full access to the database: <br>`GRANT ALL ON ownCloud.* TO 'ownClouduser'@'localhost' IDENTIFIED BY 'user_password_here' WITH GRANT OPTION`
5.	Run the following command to **Save** and **Exit**: <br>`FLUSH PRIVILEGES` <br>	`EXIT`

