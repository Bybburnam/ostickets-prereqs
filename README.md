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



