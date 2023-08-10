<p align="center">
   
![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/9f54090c-2ac9-42f9-9ea2-ad7252719fe8)


</p>

<h1>osTicket - Prerequisites and Installation</h1>
In this guide, we're diving into the complete setup process for osTicket, along with all the stuff you need to have in place before you get started. I'll be walking you through how to set up osTicket on an Azure VM (Virtual Machine). Now, assuming you've already got a VM up and running and you're connected to it using a remote desktop, we're good to go.<br/>
<br/>
If you haven't sorted out your VM yet, make sure to do that before you move on to the next steps. Ready to start? Just hit the ground running by clicking right over here! To get started, click here for files:  <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">INSTALLATION FILES!</a>


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Internet Information Services (ISS)
- MySQL

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- Internet Information Services (IIS)
- PHP Manager
- Rewrite Module
- VC Redist
- MySQL
- Heidi SQL
- osTicket v1.15.8
- [osTicket Installation Documentation](https://docs.osticket.com/en/latest/Getting%20Started/Installation.html) (to explain the function of each installation file)

<h2>Installation Steps</h2>

## How to Install osTicket

To start: Click your osTicket virtual machine and copy the Public IP address. Your Virtual Machine should already be created. If not, I have a tutorial to do so.

### Step 1: Connect to Your Virtual Machine

1. Go to the start menu on your computer, type **Remote Desktop Connection** in your search bar.
2. PASTE your Virtual Machine's IP address in the computer text input.
3. Click **Connect**.

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/e7600f67-f608-44c6-9aa7-bf36bfbac786)


### Step 2: Provide Login Credentials

1. Go ahead and input the log-in credentials you used for your virtual machine.

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/86241c57-07c0-43cf-a37c-d7b88ea9dba5)


### Step 3: Accept Certificate Errors

1. You should see something like this. Click **Yes** to proceed despite these certificate errors.

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/1ec19e9a-e512-4fd2-b765-1fc0b0ef6ba5)



### Step 4: Open Virtual Machine

1. Your virtual machine should open. Make sure you have the installation files open and available for use.

### Step 5: Install / Enable IIS

1. Right-click the start menu and click **Run**.
2. Type **control** and select **Control Panel**.
3. Click **Programs**, then click **Turn Windows features on or off**

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/dc091017-bb52-487c-8bf6-2aea87e8339f)

4. Look for **Internet Information Services**, check the box, and expand.
5. Check **World Wide Web Services**, expand it.
6. Go to **Application Development Features**, expand, select **CGI**, then collapse.
7. Expand **Common HTTP Features** and ensure everything is selected.
8. Click **OK**.

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/fcff0c71-c6e2-41de-a34e-5e61a0950382)


### Step 6: Test IIS Installation

1. Make sure all **Common HTTP Features** are checked.
2. In your browser, visit `127.0.0.1` to verify that IIS is installed and enabled.
   
![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/1dbe42a0-ab5e-4b8e-91b2-9f7f28cb6132)


### Step 7: Download and Install Required Installation Files

Note: This step is the longest and is broken down for convenience.

### Step 8: Install PHP Manager for IIS

1. From the Installation Files, download and install **PHP Manager for IIS** (`PHPManagerForIIS_V1.5.0.msi`).

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/f3423aea-0691-4fdb-b656-ff568bf26737)


### Step 9: Install Rewrite Module

1. Download/Install **Rewrite Module** (`rewrite_amd64_en-US.msi`) from the Installation Files.

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/635c83a1-25c0-463d-93f3-d45f5ff1b360)

### Step 10: Create the Directory C:\PHP

1. Open File Explorer > This PC > Windows (C:) Drive.
2. Right-click to add a new folder and name it "PHP".
3. 
![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/841302fe-185e-440d-b94d-29b975929b5e)


### Step 11: Download and Install PHP 7.3.8

1. From the Installation Files, download **PHP 7.3.8** (`php-7.3.8-nts-Win32-VC15-x86.zip`) and unzip the contents into C:\PHP.

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/ff38cd02-df70-418b-8780-b5da0db69575)


### Step 12: Install Visual C++ Redistributable
![13](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/a109c829-c1a4-4d3a-a537-23713da77277)

### From the installation files, install `VC_redist.x86.exe`.
![12](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/b1ad7ea8-8678-44f5-b582-665d44e36108)



### Step 13: Install MySQL 5.5.62

1. From the installation files, install **MySQL 5.5.62** (`mysql-5.5.62-win32.msi`).
2. Choose **Typical Setup**.
3. Launch the **Configuration Wizard** after installation.
4. Select **Standard Configuration**.
5. Set the password as **Password1**.
6. Click **Next**, then click **Execute**, and finally click **Finish**.

![14](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/3cd6347a-151a-4d10-8de2-818655e8d244)

### Step 14: Configure PHP Manager in IIS

1. Click the Start menu, type **IISAdmin**, right-click it, and select **Run as administrator**.
2. Double-click **PHP Manager**.
3. Select **New PHP Version**.
4. Browse to the C drive, navigate to the PHP folder, and select **php-cgi**.
5. Click the file, open it, and then click **OK**.

![15](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/d0e40d2c-611c-4985-8f77-4f6296a0d9ed)

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/b14773b6-7fc8-49f9-94a1-1ac954a796a3)


### Step 15: Install osTicket v1.15.8

1. Download **osTicket** from the Installation Files Folder.
2. Extract and copy the **"upload"** folder to `c:\inetpub\wwwroot`.
3. Within `c:\inetpub\wwwroot`, rename the copied **"upload"** folder to **"osTicket"**.
4. Reload IIS again by stopping and starting the server. (Click restart)

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/1565b7e7-00df-49aa-b331-72d329af2b77)

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/af801360-ca35-416d-9f70-b40d65b40787)

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/7c590b5b-3754-44d6-9090-45ac0ef27d0b)


### Step 16: Check Your osTicket Site on IIS

1. **Navigate to Your osTicket Site:** In IIS, go to **Sites** > **Default** > **osTicket**.
2. On the right, click **"Browse *:80"** to open your osTicket site.

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/2196a8ec-8ad0-4bab-a34f-f4bae7b06f73)



### Step 17: Verify Site Appearance

1. Your site should resemble the image above. If there's an error, revisit the previous steps to ensure you haven't missed anything.

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/45dd212c-1b68-457b-8ab0-bb9d567d00c7)


### Step 18: Enable Required Extensions

1. Some extensions might not be enabled in the osTicket browser. To enable them:
2. Return to IIS, navigate to **Sites** > **Default** > **osTicket**.
3. Double-click **PHP Manager**.
4. Click **"Enable or disable an extension"**.
5. Enable: `php_imap.dll`.
6. Enable: `php_intl.dll`.
7. Enable: `php_opcache.dll`.

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/b4f901c4-ba76-47cb-8f1d-693c8775a78d)



### Step 19: Refresh osTicket

1. Refresh the osTicket site in your browser to see the changes you made.

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/fe10ca92-89b2-4578-86bf-e55d5c985951)


### Step 20: Rename Configuration File

1. In File Explorer, search for `C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php`.
2. Rename `ost-sampleconfig.php` to `ost-config.php`.

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/9e346e3d-a412-4307-b4a9-665b1291fed8)


### Step 21: Adjust File Permissions

1. Right-click on the `ost-config.php` file > click **Properties**.
2. Click **Security** > **Advanced** > **Disable Inheritance**.
3. In the pop-up window, select **Remove all permissions inherited from this object**.

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/a79c73d3-bd49-41ab-a5dc-dbfb29085e05)

      
### Step 22: Assign Permissions

1. Click **Select a principal** > Type: `EVERYONE` > Click **Check Names** > Click **OK** > Select all permissions and give **full control** > Click **OK**

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/976bc4bf-2f54-48d1-a543-51b76cbb65a9)


### Step 23: Configure Help Desk Information

1. Fill out your help desk information. Remember, the MySQL username is "root" and the password is the one you previously set.
2. Download and install **HeidiSQL** from the Installation Files.
3. Open HeidiSQL, follow the installation steps, and create a new session using **root/Password1**.
4. Connect to the session and create a database called **"osTicket"**.

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/075d1010-14da-4dbd-a35e-7c924491ff37)

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/c2a8443b-2f71-462b-9ee3-c85962e750ce)

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/04408fa9-44bd-4995-8aee-a30f84343791)


### Step 24: Complete osTicket Setup

1. Continue setting up osTicket in the browser.
2. Enter these MySQL database details:
   - MySQL Database: `osTicket`
   - MySQL Username: `root`
   - MySQL Password: `Password1`
3. Click **"Install Now!"**.

Congratulations, you're almost there!

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/e479d876-bb60-4b68-a27f-7ab91eb4c8ba)


### Step 25: Clean Up

1. Delete **C:\inetpub\wwwroot\osTicket\setup** (NOTE: Only delete the setup folder).
2. Set permissions to "Read" only for **C:\inetpub\wwwroot\osTicket\include\ost-config.php**. Select **Apply** and **OK** to finish.

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/c758ce5b-c2fa-459e-8000-3a6643c57477)

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/d67c718a-a5e0-43f3-a837-eb851d5f60aa)

### Step 26: URLs for Projects

1. Admin URL: [http://localhost/osTicket/scp/login.php](http://localhost/osTicket/scp/login.php)
2. Client Ticket Submission URL: [http://localhost/osTicket/](http://localhost/osTicket/)

Finally, let's ensure everything works. Let’s log in to our admin page: [http://localhost/osTicket/scp/login.php](http://localhost/osTicket/scp/login.php).

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/1f595070-9f2b-4e3f-8195-8c2b6d6475ed)

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/21e1081b-9e0d-4dd6-9506-a8a7c0266c9d)
