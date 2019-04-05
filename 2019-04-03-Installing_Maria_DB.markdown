---
layout: default
title:  "Installing Maria DB"
nav_order: 2
parent: "Installation Prerequisites"
---



### Installing Maria DB

***To install Maria DB:***
1.	Run the following command: <br>`sudo apt-get install mariadb-Server mariadb-client`
2.	Run the following command to and enable Maria DB service during server Start, Stop, and reboot: <br>`sudo systemctl stop mariadb.service` <br>`sudo systemctl start mariadb.service` <br>`sudo systemctl enable mariadb.service`
3.	Run the following command to secure Maria DB Server:
4.	Run the following command to restart MariaDB Server: <br>`sudo systemctl restart mariadb.service`

