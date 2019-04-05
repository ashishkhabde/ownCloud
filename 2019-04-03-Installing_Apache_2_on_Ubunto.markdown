---
layout: default
title:  "Installing Apache 2 on Ubunto"
nav_order: 1
parent: "Installation Prerequisites"
---


### Installing Apache 2 on Ubunto

***To install Apache 2 on Ubunto:***
1.	Run the following command to install Apache 2: <br>`sudo apt install apache2`
2.	Run the following command to disable the directory listing: <br>`sudo sed -i "s/Options Indexes FollowSymLinks/Options FollowSymLinks/" /etc/apache2/apache2.conf`
3.	Run the following command to enable Apache 2 Service during server Start and Stop, and reboot: <br>`sudo systemctl stop apache2.service` <br>`sudo systemctl start apache2.service` <br>`sudo systemctl enable apache2.service`

