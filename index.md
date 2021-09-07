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
[Installing Owncloud server](/C:\Users\rajes\OneDrive\Documents\GitHub\ownCloud-Quick-Start-Guide\Installing ownCloud Server)
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
 
 - Memory: 512 MB 
 - Operating System: Ubuntu 20.04 LTS
 - Database: MariaDB 10+
 - Web server: Apache 2.4 with  [`prefork and mod_php`](https://doc.owncloud.com/server/admin_manual/installation/system_requirements.html#installation/manual_installation.adoc#multi-processing-module-mpm)|
 - PHP Runtime: 7.4 

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
﻿
# Installing ownCloud Server
There are different ways to install the ownCloud Server. This Quick Start Guide explains how to quickly install ownCloud.
> Ensure that ownCloud prerequisites are fulfilled and all ownCloud files are installed before beginning the installation process.

To install the ownCloud Server:
  1. Open your Web browser and type  http://localhost/owncloud 
  
  ![enter image description here](https://doc.owncloud.org/server/9.1/admin_manual/_images/install-wizard-a.png)
  
  2. To create an admin account, type a username and password in the respective fields. 
  > **Note**: Although you can now choose to click **Finish Setup** and start using your new ownCloud server, we highly recommend you to also set up Storage and database for better performance and security.
  > To setup storage and database, follow instructions provided in the section that follows.

  4.  Click **Finish Setup**. 


### Setting up storage and database
 -  Expand  **Storage and Database**. The system displays the Data folder and Configure the database sections.
 -  In the **Data Folder** field, Enter your ownCloud data directory (for example,  `/var/oc_data`)
 The Data Folder indicates the ownCloud data directory (for example, /var/oc_data). For HTTP servers other than Apache, it should be outside of your Web root directory. For other scenarios, you can store your ownCloud data in a different location (for example, storage server).  
**Recommendation:**  We recommend that you must configure your data directory location during the installation process.
    3. In the 	**Configure the database** section, select and configure the database for ownCloud Server (for example, SQLite, MySQL/MariaDB, and PostgreSQL). For ownCloud Server, the system by default selects the SQLite server. However, we recommend that you must select the MySQL/MariaDB server.    

>**Note**:  We do not provide and support for the SQLite server in the ownCloud Enterprise subscription. For ownCloud Server, the system by default selects the SQLite server. However, we recommend that you must select the MySQL/MariaDB server. For ownCloud database user and password, review the  `config.php`  file:

> ‘dbuser’ => ‘oc_molly’,  

> ‘dbpassword’ => ‘pX65Ty5DrHQkYPE5HRsDvyFHlZZHcm’,Blockquote
﻿
# Enabling Users to Connect to ownCloud Server

You can access the ownCloud server by browsing to the default route, that is, `/owncloud` (for example, <https://test.com/owncloud>). Optionally, you can change the default route by updating the URL from <https://test.com/owncloud> to <https://test.com/> in your web server configuration.  

### Config.php Parameters 
To control server operations, ownCloud uses the **config/config.php**. file. The **config/config.sample.php** file lists all the configurable parameters within ownCloud, along with example or default values.

>The installer creates a configuration file that contains all the essential parameters. Therefore, if you need to use a special value for a parameter, you should only add configuration parameters to the **config/config.php** file. You must resist copying everything from the **config/config.sample.php** file, copy only those parameters you need to modify.

For changes in the Debian/Ubuntu Linux operating systems, edit the following files:
-	/etc/apache2/sites-enabled/owncloud.conf  
-	/var/www/owncloud/config/config.php  

### Default Parameters   
You can update the default values of the given parameters after the ownCloud server configures the **config.php** file.

The ownCloud installer configures the following default parameters. 

    'instanceid' => '',

The ownCloud installer auto-generates a valid **instanceid** after you install it.  

    'passwordsalt' => '',

The ownCloud installer auto-generates **passwordsalt** and is used to hash all passwords. Do remember, if you lose this salt you lose all your passwords.  

>You must write-down the **passwordsalt** value to ensure you do not lose it.

    'trusted_domains' =>
      array (
        'demo.example.org',
        'otherdomain.example.org',
      ),
    
A list of trusted domains that you can log into. You must not remove it since it conducts security checks.

    'datadirectory' => '/var/www/owncloud/data',

Indicates the location of the user files **data/** in the ownCloud directory.

    'version' => '',

Indicates the current version of the ownCloud installed on your system.

    'dbtype' => 'mysql',

Indicates the database on which you installed ownCloud.  

    'dbhost' => '',  

Indicates the host server name, for example **localhost**, **hostname**, **hostname.example.com**, or the **IP address**. To specify a port use **hostname:####**  
For example, <i>'dbhost' => 'x.x.x.x:8080', </i><br/>
<i>x.x.x.x</i> = The server’s IP address.
                 
    'dbname' => 'owncloud',
         
Indicates the database name that you set when installing ownCloud. 

    'dbuser' => '',

Indicates the user that ownCloud uses to write to the database.
>You must keep it distinct across all ownCloud instances that use the same SQL database." %}

    'dbpassword' => '',

Indicates the database user password that you set when installing ownCloud. .
  
    'dbtableprefix' => '',

Indicates the <i>prefix</i> the ownCloud tables uses in the database.

    'installed' => false,

Indicates status of the ownCloud installation
>**true** indicates a successful installation and **false** indicates an unsuccessful installation."  

### Example of Default Config.php
The following is an example of your **config.php** file after you install ownCloud on a MySQL database.

    <?php
    $CONFIG = array (
      'instanceid' => 'oc8c0fd71e03',
      'passwordsalt' => '515a13302a6b3950a9d0fdb970191a',
      'trusted_domains' =>
      array (
        0 => 'localhost',
        1 => 'studio',
        2 => '192.168.10.155'
      ),
      'datadirectory' => '/var/www/owncloud/data',
      'dbtype' => 'mysql',
       'version' => '7.0.2.1',
      'dbname' => 'owncloud',
      'dbhost' => 'localhost',
      'dbtableprefix' => 'oc_',
      'dbuser' => 'oc_carla',
      'dbpassword' => '67336bcdf7630dd80b2b81a413d07',
      'installed' => true,
    );  
    
After you are done updating the **config.php** file, save it, and restart the Apache server. You may now access ownCloud by using http://test.com/> or http://localhost/>.



