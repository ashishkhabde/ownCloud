---
layout: default
title:  "Configuring Apache 2 site configuration file for ownCloud"
nav_order: 6
parent: "Installation Prerequisites"
---


### Configuring Apache 2 site configuration file for ownCloud

*** To configure Apache 2 site configuration file for ownCloud:***
1.	Run the following command to create a new **ownCloud.conf** configuration file: <br>`sudo nano /etc/apache2/sites-available/ownCloud.conf`
2.	Paste the following in the **ownCloud.conf** configuration file and **Save**. Paste the below content in the file and **Save** and **Exit**: <br> **Note:** Enter your domain name and directory root location. <br>
	`<VirtualHost *:80>` <br>
	`ServerAdmin admin@example.com` <br>
	`DocumentRoot` `/var/www/html/ownCloud/` <br>
	`ServerName example.com` <br>
	`ServerAlias www.example.com` <br>
	`Alias /ownCloud "/var/www/html/ownCloud/"` <br>
	`<Directory /var/www/html/ownCloud/>` <br>
	`Options +FollowSymlinks` <br>
	`AllowOverride All` <br>
	`Require all granted` <br>
	`<IfModule mod_dav.c>` <br>
		`Dav off` <br>
	`</IfModule>`
	`SetEnv HOME /var/www/html/ownCloud` <br>
	`SetEnv HTTP_HOME /var/www/html/ownCloud` <br>
	`</Directory>` <br>
	`ErrorLog ${APACHE_LOG_DIR}/error.log` <br>
	`CustomLog ${APACHE_LOG_DIR}/access.log combined` <br>
	`</VirtualHost>` <br>
