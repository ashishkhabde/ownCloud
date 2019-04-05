---
layout: default
title:  "Downloading ownCloud"
nav_order: 5
parent: "Installation Prerequisites"
---



### Downloading ownCloud 

*** To download latest version of ownCloud:**
1.	Run the following command to extract latest version of ownCloud downloaded file in the Apache 2 root directory: <br>`cd /tmp && wget https://download.ownCloud.org/community/ownCloud-10.0.10.zip` <br> <br>`unzip ownCloud-10.0.10.zip` <br>`sudo mv ownCloud /var/www/html/ownCloud/`
2.	Run the following command to set the correct permissions for ownCloud: <br>`sudo chown -R www-data:www-data `/var/www/html/ownCloud/`` <br>`sudo chmod -R 755 /var/www/html/ownCloud/`