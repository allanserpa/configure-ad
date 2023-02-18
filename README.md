<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1: Install Active Directory 
- Step 2: Create an Admin and Normal User Account in AD
- Step 3: Join Client-1 to your Domain
- Step 4: Setup Remote Desktop for Non-Administrative Users
- Step 5: Create Additional Users and Attempt to Log into Client-1 with One of the Users

<h2>Deployment and Configuration Steps</h2>

<p>
 <img src="https://i.imgur.com/qvW79bV.png" width="80%" alt="Disk Sanitization Steps"/>
 <br>
 <b>STEP 1A:</b> In Server Manager, click on "Add Roles and Features" then Install Active Directory Domain Services
 <br> 
 <b>STEP 1B:</b> In the notifications tab, click on "Promote this Server to a Domain Controller" and setup a new Forest
 <br>
 <b>STEP 1C:</b> Restart and then log back in as the Domain Contoller: "FORESTNAME\USERNAME"
</p>
<br />

<p>
 <b>STEP 2A:</b> In Active Directory Users and Computers (ADUC), create an Organizational Unit (OU) called “_EMPLOYEES”
 <br> 
 <b>STEP 2B:</b> Create a new OU named “_ADMINS”
 <br>
 <b>STEP 2C:</b> Create a new employee named “Jane Doe” with the username of “jane_admin”
 <img src="https://i.imgur.com/U1AFofa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br>
 <b>STEP 2D:</b> Add jane_admin to the “Domain Admins” Security Group
 <br> 
 <b>STEP 2E:</b> Log out/close the Remote Desktop connection to DC-1 and log back in as “mydomain.com\jane_admin”
 <br>
 <b>STEP 2F:</b> User jane_admin as your admin account from now on
</p>
<br />

<p>
  <img src="https://i.imgur.com/6PbpiTZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br>
  <b>STEP 3A:</b> From the Azure Portal, set Client-1’s DNS settings to the DC’s Private IP address
  <br> 
  <b>STEP 3B:</b> From the Azure Portal, restart Client-1
  <br>
  <b>STEP 2C:</b> Create a new employee named “Jane Doe” with the username of “jane_admin”
  <br>
  <b>STEP 2D:</b> Add jane_admin to the “Domain Admins” Security Group
  <br> 
  <b>STEP 2E:</b> Log out/close the Remote Desktop connection to DC-1 and log back in as “mydomain.com\jane_admin”
  <br>
  <b>STEP 2F:</b> User jane_admin as your admin account from now on
</p>
<br />
