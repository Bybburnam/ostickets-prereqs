<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
In this guide, we're diving into the complete setup process for osTicket, along with all the stuff you need to have in place before you get started. I'll be walking you through how to set up osTicket on an Azure VM (Virtual Machine). Now, assuming you've already got a VM up and running and you're connected to it using a remote desktop, we're good to go.<br/>

If you haven't sorted out your VM yet, make sure to do that before you move on to the next steps. Ready to start? Just hit the ground running by clicking right over here! To get started, click here for files: https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 <br />


<h2>Video Demonstration</h2>
Coming Soon!

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- osTicket (Help Desk Ticketing System)
- Remote Desktop
- PHP Manager
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
Link to downloads: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

<h2>Installation Steps</h2>

<p>
Before we delve into the osTicket tutorial, it's essential to set up the foundation. We'll begin by creating a virtual machine using Microsoft Azure. This step is crucial as it forms the platform on which we'll build the osTicket system. By establishing a solid groundwork through the virtual machine setup, we'll be ready to seamlessly proceed with the osTicket installation and configuration process. Let's get started by crafting the ideal environment for a smooth osTicket experience.
</p>
<br />


<h2>Part 1 (Create a Resource Group in Azure)</h2>

<h2>Step 1:** Create a Resource Group to organize your virtual machine and its resources.</h2>
 ![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/693d54a2-01e7-4354-a447-e9b06e38092c) <br />
<br />
![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/e290ebd8-80be-423e-bd12-94d7c2c8fe27) <br />
<br />
![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/30150b47-027f-421c-b09a-a8bad532a8ca) <br />

<br />
<br />
<br />
<br />
<br />
<br />
<h2>Creating Virtual Machine</h2>
**We will set up a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPUs, optimizing performance. Note that fewer CPUs may affect connection speed. During VM setup, ensure it creates a new Virtual Network (Vnet) for smooth connectivity**

Note: This guide assists you through the lab, with no need for strict memorization.

<h2>Step 1</h2>: Forge an Azure Virtual Machine, opting for Windows 10 and embracing 4 vCPUs for optimal performance.

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/8fb96362-cafe-441d-9519-07f650146c47)  <br />


![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/9160735d-37dd-4a79-a3ea-08af3ec00110) <br />

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/976f60b0-fa6a-40e0-9059-a3d77eec7b66) <br />

<h2>Step 2</h2>: Designate a username (e.g., labuser) and establish a robust password (e.g., osTicketPassword1!) for your VM.

By favoring 4 vCPUs in Step 2, you strike a balance between performance and connection speed, enhancing your overall experience throughout the tutorial.</p>
<br />

**COPY THE FOLLOWING SETTINGS AND INPUT TEXT FROM PICTURES BELOW. Please use login details above for later.
![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/895f5d91-d9f5-41b5-b232-d682b2451c28) ![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/aed77136-6ee1-4a6f-886a-2704b0c6f461)


<h2>CLICK NEXT UNTIL NETWORKING, ALLOW IT TO AUTOMATICALLY CREATE A NETWORK FOR THE VIRTUAL MACHINE</h2>
![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/3bfd89d3-38ca-4404-aaa4-63d42c3f6658)
<br />
<br />

<h2>CLICK REVIEW + CREATE, AND THEN CREATE</h2>
![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/4931b4ac-6244-4901-837b-765004d280b5)<br />
<br />
<br />

<h2>YOU SHOULD SEE THIS CONFIRMATION PAGE</h2>

![image](https://github.com/Bybburnam/ostickets-prereqs/assets/102566114/7b908088-9212-4a8f-ac10-733f7326266b)

<br />
<br />

</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
