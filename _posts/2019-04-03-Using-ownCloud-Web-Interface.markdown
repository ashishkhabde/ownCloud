---
layout: page
title:  "Using ownCloud Web Interface"
nav_order: 5
---

# Using ownCloud Web Interface

The ownCloud Web Interface (Web UI) allows you to connect to ownCloud Server using a Web Browser. For more information on Supported Web browsers, see,  System Requirement
Once you open the ownCloud web interface, you must enter the username and password to access the ownCloud client.
This chapter includes the following information:
- Overview of ownCloud Web Interface
- Synchronizing files in ownCloud
- Synchronizing Calendars and Contacts using ownCloud Clients

## Overview of ownCloud Web Interface

The ownCloud Web Interface (Web UI) consist of Header, Left, and Right navigation pane.
Once you logon to ownCloud Web UI, you can add, remove, and share files, and make changes based on the access privileges.
![ownCloud Web UI Home page](/assets/images/1.jpg "aa")

### Using ownCloud Web Interface
ownCloud Web interface helps you to add, remove, and share files, and make changes based on the access privileges set by the Server administrator. In the ownCloud Web interface, you can configure the ownCloud client and select the directory to save and synchronize the files in any local directory. 
You can synchronize the files placed on ownCloud on your:
- Desktop
- Mobile client

## Synchronizing files in ownCloud

### Accessing ownCloud Files Using WebDAV

You can connect and synchronize your files placed on ownCloud over WebDAV, as ownCloud supports the WebDAV protocol. Web Distributed Authoring and Versioning (WebDAV) is a Hypertext Transfer Protocol (HTTP) extension that makes it much easier to create, read, and edit files on Web Servers. With WebDAV you can access your ownCloud shares on Linux, Mac OS X and Windows in the same way as any remote network share, and stay synchronized.
You may also connect your desktop PC to your ownCloud Server by using the WebDAV protocol instead of using another client application. 

### Synchronizing files with Desktop and Mobile Clients 

ownCloud helps you to synchronize the files from the ownCloud server to your local desktop and mobile. The ownCloud client displays the current connection status and keeps track of all the activities in a log file. This helps to identify if the remote files are downloaded to your local desktop. Once the files are downloaded you can update them on your local desktop and synchronize with the Server.

### Synchronizing files with Delta Sync

The Deltasync method of synchronizing files helps to reduce the volume of data transmission of files. During Deltasync, only the updated files are synchronized and not the complete list of file set. The client only uploads or downloads the modified sections of the files which improves the data transfer rate and reduces the connectivity period.  

## Synchronizing Calendars and Contacts using ownCloud Clients

Calendar and contacts always need to be properly managed on devices, when calendars and contacts are different on different devices like home computer, office computer, or smartphones. ownCloud helps you to manage all your calendar entries at one place. ownCloud uses CalDAV and CardDAV to keep all the calendar and contact information updated and synchronized. CalDAV and CardDAV are open standard applications which is used to send and receive calendar and contact information from one device to other.
ownCloud allows you to access, update and synchronize calendars and contacts from other remote system. You need to use thunderbird as it is a cross platform email client and it works properly with CalDAV and CardDAV
Prerequisites to synchronize calendars and contacts with CalDav and CardDAV
Following are the required prerequisites to synchronize calendars and contacts.
•	Download and Install the latest version of Thunderbird. For more information on downloading thunderbird, see, http://www.mozilla.org/thunderbird/
•	Download and Install the following plugins:
•	Lightning 
•	Sogo Connector
These plugins are used to add a remote calendar and address book to thunderbird. For more information on downloading thunderbird, see, http://www.sogo.nu/english/downloads/frontends.html

## Synchronizing calendars with CalDAV

***To synchronize calendars with CalDAV
1.	Click Events and Tasks from the menu, and then click Calendar Book , to activate Thunderbird calendar.
2.	Click File from the menu, and then click New and select Calendar from the options, to create a New Calendar.
