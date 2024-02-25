<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Installation and Needed Prerequisites</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Microsoft Remote Desktop

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>
- Enable Internet Information Services (IIS) and CGI.<br>
- Install PHP Manager for IIS.<br>
- Install URL Rewrite Module.<br>
- Extract PHP into a new folder on Local Disk (C:) and register it in IIS.<br>
- Install Microsoft Visual C++ Redistributable.<br>
- Install MySQL and set up a password for root.<br>
- Extract osTicket into the "wwwroot" folder.<br>
- Enable php_imap.dll, php_opcache.dll, and php_intl.dll in IIS.<br>
- Install HeidiSQL and create a new database.<br>

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 1. Create a new Resource Group in Azure Cloud and name it RG-osticket.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 2. Create a new Virtual Machine and name it VM-osticket. Select the resource group, "RG-osticket" and Windows 10 Pro, Version 21H2 as the image.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 3. Use Microsoft Remote Desktop to connect to the virtual machine using the public IP address displayed.
</p>
<br />

<p>
<img>
</p>
<p>
Step 4. In the control panel menu, select the option "Turn Windows Features On or Off".
</p>
<br />    

<p>
<img>
</p>
<p>
Step 5. Enable Internet Information Services (IIS) and CGI.
</p>
<br />    

<p>
<img>
</p>
<p>
Step 6. Download and install PHP Manager For ISS.
</p>
<br />    

<p>
<img>
</p>
<p>
Step 7. Download and install URL Rewrite Module.
</p>
<br />    

<p>
<img>
</p>
<p>
Step 8. Navigate to Local Disk (C:) and create a new folder named "PHP".
</p>
<br />    

<p>
<img>
</p>
<p>
Step 9. Download PHP 7.3.8 (php-77.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP.
</p>
<br />    

<p>
<img>
</p>
<p>
Step 10. Download and install VC_redist.x86.exe.
</p>
<br />    

<p>
<img>
</p>
<p>
Step 11. Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi). Choose Typical Setup->Launch Config Wizard->Choose Standard Config->Use password of your choice (Password1).
</p>
<br />    

<p>
<img>
</p>
<p>
Step 12. Open Internet Informstion Services (IIS) as an admin, register PHP from within IIS and then reload IIS (Open IIS, stop and start the server).
</p>
<br />    

<p>
<img>
</p>
<p>
Step 13. Download and install osTicket v1.15.8. Extract and copy "upload" folder to C:\inetpub\wwwroot. Inside of C:\inetpub\wwwroot, rename the folder "upload" to "osTicket".
</p>
<br />    

<p>
<img>
</p>
<p>
Step 14. Navigate to IIS, sites->Default->osTicket. Open PHP Manager and select "Enable or Disable an Extension". Enable: "php_imap.dll", "php_intl.dll" and "php_opcache.dll". Refresh the osTicket site on the browser.
</p>
<br />    

<p>
<img>
</p>
<p>
Step 15. Rename ost-config.php from C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to C:\inetpub\wwwroot\osTicket\include\ost-config.php.
</p>
<br />    

<p>
<img>
</p>
<p>
Step 16. Assign Permissions :ost-config.php. Disable inheritance->Remove All. Then add New Permissions->Everyone->All.
</p>
<br />

<p>
<img>
</p>
<p>
Step 17. Setup osTicket in the browser, name the helpdesk and choose default email (from where you will receive emails from customers).
</p>
<br />

<p>
<img>
</p>
<p>
Step 18. Download and install HeidiSQL. Create a new session using "root/Password1". Connect to the session and create database called osTicket. 
</p>
<br />

<p>
<img>
</p>
<p>
Step 19. In the browser, continue setting up osTicket. MySQL Datebase: osTicket. MySQL Username: root. MySQL Password: Password1. Click install.
</p>
<br />

<p>
<img>
</p>
<p>
Step 20. Browse to the help desk login page: "http://localhost/osTicket/scp/login.php"
</p>
<br />

<p>
<img>
</p>
<p>
Step 21. Clean up the installation files by deleting "C:\inetpub\wwwroot\osTicket\setup". Set the permissions to "Read" only for C:\inetpub\wwwroot\osTicket\include\ost-config.php.
</p>
<br />
