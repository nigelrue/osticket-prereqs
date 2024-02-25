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
<img src="https://i.imgur.com/B7tJd5T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 1. Create a new Resource Group in Azure Cloud and name it RG-osticket.
</p>
<br />

<p>
<img src="https://i.imgur.com/qeQxiIP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 2. Create a new Virtual Machine and name it VM-osticket. Select the resource group, "RG-osticket" and Windows 10 Pro, Version 21H2 as the image.
</p>
<br />

<p>
<img src="https://i.imgur.com/oMA1INJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 3. Use Microsoft Remote Desktop to connect to the virtual machine using the public IP address displayed.
</p>
<br />

<p>
<img src="https://i.imgur.com/tYXwfMF.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 4. In the control panel menu, select the option "Turn Windows Features On or Off".
</p>
<br />    

<p>
<img src="https://i.imgur.com/3ahwDiK.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/cBSoSIj.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 5. Enable Internet Information Services (IIS) and CGI.
</p>
<br />    

<p>
<img src="https://i.imgur.com/sk5APck.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 6. Download and install PHP Manager For ISS.
</p>
<br />    

<p>
<img src="https://i.imgur.com/sZB6OZS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 7. Download and install URL Rewrite Module.
</p>
<br />    

<p>
<img src="https://i.imgur.com/h8KzTZs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 8. Navigate to Local Disk (C:) and create a new folder named "PHP".
</p>
<br />    

<p>
<img src="https://i.imgur.com/Hi3H7uB.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 9. Download PHP 7.3.8 (php-77.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP.
</p>
<br />    

<p>
<img src="https://i.imgur.com/sU7ka44.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 10. Download and install VC_redist.x86.exe.
</p>
<br />    

<p>
<img src="https://i.imgur.com/fBD1brx.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/WTLqyju.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>  
</p>
<p>
Step 11. Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi). Choose Typical Setup->Launch Config Wizard->Choose Standard Config->Use password of your choice (Password1).
</p>
<br />    

<p>
<img src="https://i.imgur.com/lAwP17x.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/GPCgpUE.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>  
</p>
<p>
Step 12. Open Internet Informstion Services (IIS) as an admin, register PHP from within IIS and then reload IIS (Open IIS, stop and start the server).
</p>
<br />    

<p>
<img src="https://i.imgur.com/2HKpOgQ.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/CGztnBy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/wwSy7nL.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 13. Download osTicket v1.15.8. Extract and copy "upload" folder to C:\inetpub\wwwroot. Inside of C:\inetpub\wwwroot, rename the folder "upload" to "osTicket".
</p>
<br />    

<p>
<img src="https://i.imgur.com/YoBsusK.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/PzGoprt.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 14. Navigate to IIS, sites->Default->osTicket. Open PHP Manager and select "Enable or Disable an Extension". Enable: "php_imap.dll", "php_intl.dll" and "php_opcache.dll". Refresh the osTicket site on the browser.
</p>
<br />    

<p>
<img src="https://i.imgur.com/Jr6f4Qz.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 15. Rename ost-config.php from C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to C:\inetpub\wwwroot\osTicket\include\ost-config.php.
</p>
<br />    

<p>
<img src="https://i.imgur.com/NFa4LOU.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Rppi1jb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 16. Assign Permissions :ost-config.php. Disable inheritance->Remove All. Then add New Permissions->Everyone->All.
</p>
<br />

<p>
<img src="https://i.imgur.com/1uX4PXN.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 17. Setup osTicket in the browser, name the helpdesk and choose default email (from where you will receive emails from customers).
</p>
<br />

<p>
<img src="https://i.imgur.com/T4tuaxx.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/ZGPAmHr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/qFaItIy.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/3z3jCZY.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 18. Download and install HeidiSQL. Create a new session using "root/Password1". Connect to the session and create database called osTicket. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJ04Flr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 19. In the browser, continue setting up osTicket. MySQL Datebase: osTicket. MySQL Username: root. MySQL Password: Password1. Click install.
</p>
<br />

<p>
<img src="https://i.imgur.com/OoMJVXZ.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 20. Browse to the help desk login page: "http://localhost/osTicket/scp/login.php"
</p>
<br />

<p>
<img src="https://i.imgur.com/zMKu7BG.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 21. Clean up the installation files by deleting "C:\inetpub\wwwroot\osTicket\setup". Set the permissions to "Read" only for C:\inetpub\wwwroot\osTicket\include\ost-config.php.
</p>
<br />
