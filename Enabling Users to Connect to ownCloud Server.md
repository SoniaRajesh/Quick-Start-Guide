
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


