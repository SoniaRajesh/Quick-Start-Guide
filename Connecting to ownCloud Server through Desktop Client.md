

# Connecting to ownCloud Server through Desktop Client

For synchronizing files with your desktop computer, we recommend using the  [ownCloud Sync Client](https://owncloud.com/desktop-app/)  for Windows, Mac OS X and Linux.

The ownCloud Desktop Sync Client enables you to connect to your private ownCloud Server. You can create folders in your home directory, and keep the contents of those folders synced with your ownCloud server. Simply copy a file into the directory and the ownCloud desktop client does the rest. Make a change to the files on one computer, it will flow across the others using these desktop sync clients. You will always have your latest files with you wherever you are.

You must complete a two-step process to use ownCloud Desktop Client:
- Download and Install
- Configuration

### Downloading and installing the ownCloud Desktop Client?
To download and install the ownCloud Desktop Client, review the <a  alt='Desktop Client installation guide' href='https://doc.owncloud.com/desktop/2.8/installing.html'>Desktop Client installation guide</a>.

### Configuring the ownCloud Desktop Client?

 1. Launch the ownCloud Desktop Client.
 2. In **Server Address** field, enter the IP address for your server (for example, http(s)://10.10.10.10), and click **Next**.
    ![enter image description here](https://docs.bitnami.com/images/img/apps/owncloud/configure-client-1.png) 
  >You must review the IP address that you enter.
 3. In the **Username** and **Password** field, enter your username and password respectively, and then click **Next**.
    ![enter image description here](https://docs.bitnami.com/images/img/apps/owncloud/configure-client-2.png) 
 4. Select an appropriate sync option.

    | Option | Description |
    |--|--|
    | Sync everything from server |Indicates that the system syncs everything from the server |
    | Choose what to sync |Indicates that you can choose what you which to download from the server|
    | Keep Local Data |Indicates that while syncing you do not want the system to delete your local data |
    | Start a clean sync |Indicates that while syncing you want the system to delete your local data |

    ![enter image description here](https://docs.bitnami.com/images/img/apps/owncloud/configure-client-3.png) <br/>
 5. Click **Connect**, and then click **Finish**. The system displays a success message indicating that you have successfully configured the ownCloud desktop client
