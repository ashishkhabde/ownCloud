---
layout: default
title:  "Enabling ownCloud and Rewriting the module"
nav_order: 7
parent: "Installation Prerequisites"
---


### Enabling ownCloud and Rewriting the module

***To enable ownCloud and rewriting the module:**
- Run the following command, once the virtual host is configured: <br>
	`sudo a2ensite ownCloud.conf` <br>
	`sudo a2enmod rewrite` <br>
	`sudo a2enmod headers` <br>
	`sudo a2enmod env` <br>
	`sudo a2enmod dir` <br>
	`sudo a2enmod mime` <br>
	
For more information on configuring virtual host, refer, [Configuring Apache 2 site configuration file for ownCloud](2019-04-03-Configuring_Apache_2_site_configuration_file_for_ownCloud)
