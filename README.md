# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Microsoft Azure Account
- Remote Desktop Access
- IIS Basic Knowledge
- oSTicket Installation Files
- HeidiSQL

<h2>Installation Steps</h2>



1. Create A VM (Virtual MAchine) 
  - In Azure, create a VM and add it to a new resource group 
  - Virtual Machine Name:
  - Image:
  - Size:

Now, navigate to the (VM) tab and select "Azure Virtual Machine"
<img width="1366" height="664" alt="image" src="https://github.com/user-attachments/assets/b0d398ca-91a6-464a-b102-e685b2838b33" />
<img width="1366" height="665" alt="image" src="https://github.com/user-attachments/assets/27d2498c-8c13-4f3d-9916-fd7cd19a6a48" />
Create a new resource group and name the VM - select region -} image -} size -} operating system.
- Select the desired CPU size, enter your username and password, check the licensing box, and then review and create the virtual machine.

2. LOG INTO THE (VM) VIRTUAL MACHINE
1. Locate the Public IP Address
- Go to your virtual machine’s overview page and copy the Public IP Address.
2. Open Remote Desktop
- Launch the Remote Desktop application on your computer.
3. Add a New Connection
- Select “Add PC.”
- Paste the Public IP Address into the “PC Name” field.
4. Save and Connect
- Click “Add” to save the connection.
5. Log In
- Enter the username and password you created during the virtual machine setup to sign in.

3. Download and Prepare Installation Files
-Within the virtual machine, download the osTicket installation files. Extract the contents of the zipped folder to your desktop.

4.Installing IIS and Enabling the Required Features
1. Open the Control Panel and navigate to Programs - Turn Windows features on or off.
2. In the list of Windows features, locate and enable Internet Information Services (IIS).
3. Under World Wide Web Services, expand Application Development Features and ensure the following components are selected: CGI

5. INSTALL THE REQUIRED COMPONENTS
- This will be from the OsTicket INSTALLATION Files Folder
- Install PHP Manager for IIS:
- Install Rewrite Module

6. SETUP "PHP"
- Go to C: Drive & Create the Directory C:
- Unzip PHP into the folder
- Install VC

7. INSTALL MYSQL
- From the osTicket Installation Files Folder | Install MYSQL
- Then select Typical Setup
- Launch the configuration wizrd
- Standard Configuration
- Input a username and password.

8. CONFIGURE IIS
- Open ISS as an admin.
- Register the PHP
- Then go to PHP manager, register PHP path
- Reload ISS

9. INSTALL THE OS TICKET
1. Unzip the Ticket
2. Copy the upload folder into the folder:\inetpub\wwwroot
3. Rename the upload folder to osTicket
4. Reload ISS

10. CONFIGURING OSTICKET
1. Open IIS
2. Navigate to sites - Default - osTicket
3. On the right click Browse:80

11. UPDATE THE CONFIG. FILES
- Rename ost-config.php
- Assign permissions
- Disable inheritance
- Add new permissions - Full Control

12. COMPLETE OSTICKET SETUP
- Continue the osTicket setup in the browser
- Set your helpdesk name
- set your default email. - This will allow you to recieve emails from customers

13. INSTALL HEIDISQL & CONFIGURE DATABASE
1. Install HeidiSQL from the osTicket Installation Files Folder
2. Then open HeidiSQL
3. Create a new session
4. Connect to the Session
5. Now Create a database entitled osTicket

14. COMPLETE THE INSTALLATION (SQL)
- MySQL Database
- Username
- Password
- Hit "Install Now"
- Finally, verify the installation - login to the helpdesk page.
