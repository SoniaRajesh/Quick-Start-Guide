
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
