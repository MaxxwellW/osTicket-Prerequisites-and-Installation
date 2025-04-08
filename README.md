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
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> "C:\Users\dell\OneDrive\Pictures\osTicket Install Repo\Install osTicket Files.png" 
</p>
<p>
Download osTicket files

</p>
<img "C:\Users\dell\OneDrive\Pictures\osTicket Install Repo\Installed osTicket Files.png"
</p>
<p>
Downloaded osTicket files

<p>
<img "C:\Users\dell\OneDrive\Pictures\osTicket Install Repo\Extract osTicket-v1.15.8.zip Action.png"  "C:\Users\dell\OneDrive\Pictures\osTicket Install Repo\osTicket-v1.15.8.zip completed.png"
</p>
<p>
Extract osTicket-v1.15.8.zip from the desktop
  
</p>
<img "C:\Users\dell\OneDrive\Pictures\osTicket Install Repo\visual that IIS isnt working.png"
</p>
<p>
Use Loopback to try the webserver

<p>
<img "C:\Users\dell\OneDrive\Pictures\osTicket Install Repo\CGI config.png"
</p>
<p>
Enable IIS in Windows WITH CGI
World Wide Web Services -> Application Development Features -> [X] CG
<br />

<p>
<img "C:\Users\dell\OneDrive\Pictures\osTicket Install Repo\Create PHP Directory.png"
</p>
<p>
Create Directory for PHPManagerForIIS_V1.5.0.msi 

</p>
<img "C:\Users\dell\OneDrive\Pictures\osTicket Install Repo\Extraxt to Directory.png"
</p>
<p>
Extract PHPManagerForIIS_V1.5.0.msi into Directory to Install

<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
