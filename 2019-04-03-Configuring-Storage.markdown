---
layout: default
title:  "Configuring Storage"
parent: "Managing external storage support"
nav_order: 1
---

## Configuring Storage

You can create and add new external storage mount; however, all the external storage must be first configured in the application.

***To configure external storage in the support application:***
1. Click **Storage** in the **Admin** section, on the **Settings** page.
2.	Select **Enable external storage**, on the **External Storage** page.
3.	Configure the following:

|Field Name|Description|
|---	|---	|
|Folder Name|Enter the folder name. <br > **Note:** Folder name does not accept alphanumeric characters|
|External Storage|Select the external storage from the available list in dropdown.|
|Authentication|Select the authentication method from the Authentication drop down list. The configuration fields for mounting external storage is based on the authentication method.<br> **Note:** ownCloud storage application accepts one or more authentication methods such as, user name and passwords, login credentials, or RSA- public key etc.|
|Configuration|The configuration parameters are displayed based on the Authentication mechanism.<br> For example, If the Authentication mechanism is set as Username and Password, in that case the fields displayed for Configuration parameters are: Host name, Root, Username and Password|

4.	External storage details are saved automatically, once all the fields are entered. 
The following color dots are displayed against each storage row which indicates the following: 
- **Green dot**: Specifies the storage is ready to use.
- **Red or yellow dot**: Specifies ownCloud is unable to connect to the external storage.
In this case, you need to check the configuration and network connectivity.

**Note:** If an error occurs on any of the external storage, the storage becomes unavailable within 10 minutes. Click the colored dot to identify the error and reload the page. 

