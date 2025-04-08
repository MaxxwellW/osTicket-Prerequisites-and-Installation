<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket -Installation from A to Z </h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- An able CPU (Windows 10) or use of a Virtual Machine
- extract zip files from Doc 
- Attempt to launch through various steps of coniguration

- Will have to use control panel and file explorer to ensure success

  - https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD to be downloaded and extracted

  - PHPManagerForIIS_V1.5.0.msi to Install

  - rewrite_amd64_en-US.msi to Install
  
  - php-7.3.8-nts-Win32-VC15-x86.zip to Unzip
  
  - VC_redist.x86.exe to Install
  
  - mysql-5.5.62-win32.msi to Install
  
  - osTicket-v1.15.8.zip to Unzip

  - HeidiSQL to install
  
- Attempt to Launch URL  http://localhost/osTicket/scp/login.php

<h2>Installation Steps</h2>

<p>
<img src=https://i.imgur.com/teQ7FSV.png 
</p>
<p>
Download osTicket files

</p>
<img 
</p>
<p>
Downloaded osTicket files

<p>
<img 
</p>
<p>
Extract osTicket-v1.15.8.zip from the desktop
  
</p>
<img 
</p>
<p>
Use Loopback to try the webserver

<p>
<img 
</p>
<p>
Enable IIS in Windows WITH CGI
World Wide Web Services -> Application Development Features -> [X] CG
<br />

<p>
<img 
</p>
<p>
Create Directory for PHPManagerForIIS_V1.5.0.msi 

</p>
<img 
</p>
<p>
Extract PHPManagerForIIS_V1.5.0.msi into Directory to Install

<p>
<img 
</p>
<p>
Download PHPManagerForIIS_V1.5.0.msi

<p>
<img 
</p>
<p>
Download rewrite_amd64_en-US.msi

<p>
<img 
</p>
<p>
Install VC_redist.x86.exe

</p>
<img
</p>
<p> 
Install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
Typical Setup -> Launch Configuration Wizard (after install) -> Standard Configuration ->
Username: root
Password: root

</p>
<img 
</p>
<p> 
Open IIS as an Admin -> Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe) -> Reload IIS (Open IIS, Stop and Start the server)

</p>
<img  
</p>
<p> 
Install osTicket v1.15.8 -> From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” -> copy the “upload” folder into “c:\inetpub\wwwroot” -> Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
Reload IIS (Open IIS, Stop and Start the server)
  
</p>
<img 
</p>
<p> 
Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

</p>
<img 
</p>
<p>
Some extensions are not enabled
  - Go back to IIS, sites -> Default -> osTicket
  - Double-click PHP Manager
  - Click “Enable or disable an extension”
  - Enable: php_imap.dll
  - Enable: php_intl.dll
  - Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes
<img 

<img 

</p>
<img 
</p>
<p>
Rename: ost-config.php From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

</p>
<img  
</p>
<p>
Assign Permissions: ost-config.php -> Disable inheritance -> Remove All New Permissions -> Everyone -> All

</p>
<img 
</p>
<p>
Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)

</p>
<img 
</p>
<p>
From the “osTicket-Installation-Files” folder -> install HeidiSQL -> Open Heidi SQL -> Create a new session, root/root -> Connect to the session -> Create a database called “osTicket”

</p>
<img 
</p>
<p>
Continue Setting up osTicket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: root
Click “Install Now!”

</p>
<img 
</p>
<p>
Congratulations, hopefully it is installed with no errors!
Browse to your help desk login page: http://localhost/osTicket/scp/login.php

<img src=:https://i.imgur.com/teQ7FSV.png>

</p>
Clean up: Delete: C:\inetpub\wwwroot\osTicket\setup -> Set Permissions to “Read” only -> C:\inetpub\wwwroot\osTicket\include\ost-config.php


https://i.imgur.com/0Op1O96.png
https://i.imgur.com/30BKJ1L.png
https://i.imgur.com/XUoPVNY.png
https://i.imgur.com/P5tB1LR.png
https://i.imgur.com/7lXgyVV.png
https://i.imgur.com/Zl9sGYx.png
https://i.imgur.com/N4ciLXd.png
https://i.imgur.com/DQmnGcL.png
https://i.imgur.com/LjtxHZi.png
https://i.imgur.com/dz7Qt0w.png
https://i.imgur.com/ch3hQmf.png
https://i.imgur.com/ZcQwMhy.png
https://i.imgur.com/DKvBmhK.png
https://i.imgur.com/1pc5TC2.png
https://i.imgur.com/1pPCLoY.png
https://i.imgur.com/RE5F90P.png 
https://i.imgur.com/1tsNS1R.png
