---
layout: page
title:  "Managing external storage support"
date:   2019-04-03 12:24:47 +0530
categories: jekyll update
---

# Managing external storage support

The External Storage Support application helps you to mount external storage services and devices as secondary ownCloud storage devices. The application allows you to mount the external storage services such as such as, Amazon S3, Google Drive, Open Stack Object Storage, ownCloud, SFTP, SMB/CIFS fileServers, and WebDAV Servers in ownCloud.
This chapter includes the following information:
- Configuring Storage
- Managing Users and Groups Accounts

## Configuring Storage

You can create and add new external storage mount; however, all the external storage must be first configured in the application.

*** To configure external storage in the support application:
1. Click **Storage** in the **Admin** section, on the **Settings** page.
2.	Select **Enable external storage**, on the **External Storage** page.
3.	Configure the following:

	| Field Name	| Description								|
	| ------------- | ----------------------------------------- |
	| Folder Name	| Enter the folder name.-	**Note:** Folder name does not accept alphanumeric characters. 				|				 
	| 				 |aJAT aSHI							        |

		|**Note:** Folder name does not accept alphanumeric characters.
-------------------------------------------------


|------------------|-----------------------|
|				   |					   |
|------------------|-----------------------|
|------------------|-----------------------|
|------------------|-----------------------|
|------------------|-----------------------|
|------------------|-----------------------|
|------------------|-----------------------|
|------------------|-----------------------|
4.	External storage details are saved automatically, once all the fields are entered. 
The following color dots are displayed against each storage row which indicates the following: 
- **Green dot:** Specifies the storage is ready to use.
- **Red or yellow dot:** Specifies ownCloud is unable to connect to the external storage.
In this case, you need to check the configuration and network connectivity.

**Note:**
If an error occurs on any of the external storage, the storage becomes unavailable within 10 minutes. Click the colored dot to identify the error and reload the page. 

## Managing Users and Groups Accounts

The ownCloud administrator can set up different user accounts and groups, and assign appropriate privileges and permissions, based on the functions the user accounts and groups need to perform.

### User and Group Permissions

An administrator configures a storage for a user or group and assigns permission to a single user or the list of users in the group to perform activity on that storage. 
There are two predefined user accounts in ownCloud:
-**admin:** The administrator account for ownCloud.
- **default:** A standard user account that can be used to perform various operations in ownCloud. 
	- Grant Privileges: You can restrict these default settings to users or groups. Specific privileges are granted to users and groups for the storage devices.

***To grant user and group privileges:
1.	Select the user or group from the list of **User list** or **Group list**.
2.	Click **Arrow** to grant permission.
	Users and groups granted permission are moved to **Available for** section, and the list is displayed.
