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

Download osTicket files
<p>
<img src="https://i.imgur.com/0dKkroD.png" />
</p>

<p>
<img src="https://i.imgur.com/IU7xUFM.png" />
</p>
<p>
Downloaded osTicket files

<p>
<img src="https://i.imgur.com/H2oclwr.png" />
</p>
<p>

Extract osTicket-v1.15.8.zip from the desktop
<p>
<img src="https://i.imgur.com/8QCLhpT.png" />
</p>
<p>

Use Loopback to try the webserver  
<p>
<img src="https://i.imgur.com/vG5Twfr.png" />
</p>
<p>

Enable IIS in Windows WITH CGI
World Wide Web Services -> Application Development Features -> [X] CGI
<br />

<p>
<img src="https://i.imgur.com/0LTOeOE.png" />
</p>
<p>
Reload URL to show IIS is fucntional

<p>
<img src="https://i.imgur.com/H1dyL27.png" />
</p>
<p>

Now it is time to configure 
<p>
<img src="https://i.imgur.com/SIaViSc.png" />
</p>
<p>
Create Directory for PHPManagerForIIS_V1.5.0.msi 

<p>
<img src="https://i.imgur.com/O0w6DqJ.png" />
</p>
<p>
Extract PHPManagerForIIS_V1.5.0.msi into Directory to Install

<p>
<img src="https://i.imgur.com/MFFXo3c.png" />
</p>
<p>
Download PHPManagerForIIS_V1.5.0.msi

<p>
<img src="https://i.imgur.com/1qvb4DE.png" />
</p>
<p>
Download rewrite_amd64_en-US.msi

<p>
<img src="https://i.imgur.com/h7eL1CI.png" />
</p>
<p>
Install VC_redist.x86.exe

<p>
<img src="https://i.imgur.com/jwFSnLD.png" />
</p>
<p>
Install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
Typical Setup -> Launch Configuration Wizard (after install) -> Standard Configuration ->
Username: root
Password: root

<p>
<img src="https://i.imgur.com/Hl8DdVk.png" />
</p>
<p>
Open IIS as an Admin -> Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe) -> Reload IIS (Open IIS, Stop and Start the server)

<p>
<img src="https://i.imgur.com/slih0hM.png" />
</p>
<p>
<p>
<img src="https://i.imgur.com/cz6SFpm.png" />
</p>

Install osTicket v1.15.8 -> From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” -> copy the “upload” folder into “c:\inetpub\wwwroot” -> Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
Reload IIS (Open IIS, Stop and Start the server)
  
<p>
<img src="https://i.imgur.com/vY50wpY.png" />
</p>

<p>
<img src="https://i.imgur.com/NfrUfmv.png" />
</p>
<p>
Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

<p>
<img src="https://i.imgur.com/ARNeQKx.png" />
</p>
<p>
Some extensions are not enabled
  - Go back to IIS, sites -> Default -> osTicket
  - Double-click PHP Manager
  - Click “Enable or disable an extension”
  - Enable: php_imap.dll
  - Enable: php_intl.dll
  - Enable: php_opcache.dll

<img src="https://i.imgur.com/vTCrxI5.png" />
</p>
<p>
Refresh the osTicket site in your browser, observe the changes
<p>
<img src="https://i.imgur.com/3JpYdh7.png" />
</p>

Rename: ost-config.php From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
<p>
<img src="https://i.imgur.com/cuA9pIj.png" />
</p>
<p>

Assign Permissions: ost-config.php -> Disable inheritance -> Remove All New Permissions -> Everyone -> All
<p>
<img src="https://i.imgur.com/zu4yLoR.png" />
</p>
<p>

<p>
<img src="https://i.imgur.com/CROmhzg.png" />
</p>

Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)

<p>
<img src="https://i.imgur.com/niVHnN4.png" />
</p>
<p>


<p>
<img src="https://i.imgur.com/8i3Rkjg.png" />
</p>
<p>
From the “osTicket-Installation-Files” folder -> install HeidiSQL -> Open Heidi SQL -> Create a new session, root/root -> Connect to the session -> Create a database called “osTicket”

<p>
<img src="https://i.imgur.com/EmILzXn.png" />
</p>
<p>


<p>
<img src="https://i.imgur.com/cnBDV7u.png" />
</p>
<p>

Continue Setting up osTicket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: root
Click “Install Now!”

<p>
<img src="https://i.imgur.com/T4y7xRZ.png" />
</p>
<p>

</p>
<br />
Congratulations, hopefully it is installed with no errors!
Browse to your help desk login page: http://localhost/osTicket/scp/login.php

<p>
<img src="https://i.imgur.com/dmUReAE.png" />
</p>
</p>
