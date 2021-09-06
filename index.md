# ownCloud - Overview

ownCloud is an open source software that enables private cloud services on your own servers and environments. oneCloud lets you perform all the functions of any other cloud storage software Like DropBox, free of cost. It also provides file synchronization and sharing solutions along with other cloud storage services.

ownCloud works on client-server model. This includes the following:
  - The ownCloud server that runs on Linux. 
  - Client applications for Microsoft Windows, Mac OS X and Linux
  - Mobile clients for the Android and Apple iOS operating systems
 
 The ownCloud server is available in three editions:
  - The free community-supported Server. This is the core server for all editions.
  - The Standard Subscription for customers who want paid support for the core Server, without   Enterprise applications. 
  - The Enterprise Subscription provides paid support for the Enterprise Edition. This includes the core Server and Enterprise apps.
 	> See What’s New for Admins in ownCloud  for more information on the different ownCloud editions.
 

## Document Overview
This ownCloud Quick Start Guide takes you through the software prerequisites for installing ownCloud server, and steps to install, configure, and connect to ownCloud server.

For administrators:
- Installing and configuring an Owncloud server
-  Managing user account
-- Adding user account
-- Enabling users to to connect to the Owncloud server

 For users:
 - connect to the Owncloud server using a desktop or mobile client?
## Resources

 - See the official [ownCloud channel](https://www.youtube.com/channel/UC_4gez4lsWqciH-otOlXo5w) and [ownClouders community channel](https://www.youtube.com/channel/UCA8Ehsdu3KaxSz5KOcCgHbw) on YouTube for tutorials, overviews, and conference videos. 
 - Visit [ownCloud Planet](https://owncloud.org/news/) for news and developer blogs.

# Prerequisites
This section explains the basic environment, database, and memory requirements for installing ownCloud server.

 ## Environment Requirements
 We recommend the following component requirements:
|Component|Requirement|  
| ----------- | ----------- |  
| Memory| 512 MB|  
|Operating System | Ubuntu 20.04 LTS
|Database| MariaDB 10+ |
|Web server|Apache 2.4 with  [`prefork and mod_php`](https://doc.owncloud.com/server/admin_manual/installation/system_requirements.html#installation/manual_installation.adoc#multi-processing-module-mpm)|
|  PHP Runtime| 7.4 |

We also support the following:
##### Operating System	
-   Debian 10
    
-   Fedora 32 and 33
    
-   Red Hat Enterprise Linux/Centos 7.5 and 8
    
-   SUSE Linux Enterprise Server 12 with SP4/5 and 15
    
-   Ubuntu 18.04 and 20.04
    
-   openSUSE Leap 15.2 
##### Database
-   MySQL 8+ or MariaDB 10+ (**Recommended**)
    
-   Oracle 11 and 12
    
-   PostgreSQL 9 and 10
    
-   SQLite (**Not for production**)
##### Webserver
-   Apache 2.4 with  [`prefork`  and  `mod_php`](https://doc.owncloud.com/server/admin_manual/installation/system_requirements.html#installation/manual_installation.adoc#multi-processing-module-mpm)

 ##### PHP Runtime
-   7.3 and 7.4
##### Hypervisors

-   Hyper-V
    
-   VMware ESX
    
-   Xen
    
-   KVM
    

##### [](https://doc.owncloud.com/server/admin_manual/installation/system_requirements.html#web-browser)Web Browser

-   Edge (current version on Windows 10)
    
-   IE11 or newer (except Compatibility Mode)
    
-   Firefox 60 ESR+
    
-   Chrome 66+
    
-   Safari 10+
    

##### Desktop Sync Client

We always recommend to use the newest sync client with the latest server release.

You can find  [detailed system requirements](https://doc.owncloud.com/desktop/installing.html#system-requirements)  in the documentation for the Desktop Synchronization Client.

##### Mobile Apps

We always recommend to use the newest mobile apps with the latest server release.

You can find detailed system requirements in the documentation for the mobile apps.

-   [iOS system requirements](https://doc.owncloud.com/ios-app/ios_faq.html)
    
-   [Android system requirements](https://doc.owncloud.com/android/faq.html)
    

You can find out more in the  [changelog](https://owncloud.com/changelog).

## [](https://doc.owncloud.com/server/admin_manual/installation/system_requirements.html#database-requirements)Database Requirements

The following database settings are currently required if you’re running ownCloud together with a MySQL or MariaDB database:

-   Disabled or  `BINLOG_FORMAT = MIXED`  or  `BINLOG_FORMAT = ROW`  configured Binary Logging (See:  [MySQL / MariaDB with Binary Logging Enabled](https://doc.owncloud.com/server/admin_manual/configuration/database/linux_database_configuration.html#mysql-mariadb-with-binary-logging-enabled))
    
-   InnoDB storage engine (The MyISAM storage engine is not supported, see:  [MySQL / MariaDB storage engine](https://doc.owncloud.com/server/admin_manual/configuration/database/linux_database_configuration.html#mysql-mariadb-storage-engine))
    
-   `READ COMMITED`  transaction isolation level (See:  [MySQL / MariaDB  `READ COMMITED`  transaction isolation level](https://doc.owncloud.com/server/admin_manual/configuration/database/linux_database_configuration.html#mysql-mariadb-read-commited-transaction-isolation-level))
    

## [](https://doc.owncloud.com/server/admin_manual/installation/system_requirements.html#memory-requirements)Memory Requirements

Memory requirements for running an ownCloud server are greatly variable, depending on the numbers of users and files, and volume of server activity. ownCloud officially requires a minimum of 128MB RAM. But, we recommend a minimum of 512MB.

Next: Installing ownCloud Server 
