<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
- Rewrite Module (rewrite_amd64_en-US.msi)
- PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip)
- VC_redist.x86.exe
- MySQL 5.5.62 (mysql-5.5.62-win32.msi)


<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/Yb3f3Mh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I. After creating a virtual machine, install/enable IIS in Windows with CGI. From the Control Panel>Programs and Features>Turn Windows features on or off>turn IIS on>expand IIS>expand World Wide Web Services>expand Application Development Features>check CGI
</p>
<br />

<p>
<img src="https://i.imgur.com/gRTus3z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
II. The next step necessary in order to install osTicket is to begin installing all of the prerequisites. Start with PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi).
</p>
<br />

<p>
<img src="https://i.imgur.com/YRF4xVD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
III. Next will be Rewrite Module (rewrite_amd64_en-US.msi).
</p>
<br />

<p>
<img src="https://imgur.com/kF0nor7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
IV. In this step, create the directory C:\PHP. Then install PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into the new directory.
</p>
<br />

<p>
<img src="https://imgur.com/PqiXNMx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
V. Now, VC_redist.x86.exe needs to be installed.
</p>
<br />

<p>
<img src="https://imgur.com/Zmiya0N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
VI. MySQL 5.5.62 (mysql-5.5.62-win32.msi) is downloaded and installed in this step. When installing, choose Typical Setup>Launch Configuration Wizard (after install)>Standard Configuration>create a password
</p>
<br />

<p>
<img src="https://i.imgur.com/ShftddU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
VII. Open IIS as an Admin>register PHP Manager>restart IIS *remember to restart IIS each time a new change is made*
</p>
<br />

<p>
<img src="https://i.imgur.com/VLbCPf8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
VIII. Download osTicket v1.15.8>extract and copy the "upload" folder to C:\inetpub\wwwroot>change the name of "upload" to osTicket>restart IIS
</p>
<br />

<p>
<img src="https://i.imgur.com/nEUTJ89.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
IX. In IIS, go to Sites>Default>osTicket>click Browse *:80 on the right hand side. There are some of the PHP extensions that have a red X next to them, indicating that they are not enabled.
</p>
<br />

<p>
<img src="https://i.imgur.com/wmoV7hw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
X. In this step, certain PHP extensions are being enabled in order to ensure full functionality of osTicket. From IIS>Sites>Default>osTicket>PHP Manager>click Enable or disable an extension>enable the extensions "php_imap.dll", "php_intl.dll", and "php_opcache.dll">refresh osTicket
</p>
<br />

<p>
<img src="https://i.imgur.com/8nskWHl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
XI. From C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php, rename ost-sampleconfig.php to ost-config.php
</p>
<br />

<p>
<img src="https://i.imgur.com/U7Puy6o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
XII. Here, Permissions need to be assigned to ost-config.php. Right click on ost-config.php>Permissions>Advanced Security Settings>Disable inheritance>Remove All. Now, go back to Permissions and add "Everyone" and assign all Permissions to "Everyone".
</p>
<br />

<p>
<img src="https://i.imgur.com/EVewG0A.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
XIII. Set up osTicket in browser. Fill in all of the required information up until the Database Settings.
</p>
<br />

<p>
<img src="https://i.imgur.com/HaiZtse.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
XIV. Download and install HeidiSQL>open and create a new session>create a password>connect to that session>right click>Create new>Database> name database "osTicket"
</p>
<br />

<p>
<img src="https://i.imgur.com/IuETfuA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
XV. Complete osTicket setup. MySQL Database- osTicket, MySQL Username- root, MySQL Password- (password that was created). Click Install Now.
</p>
<br />

<p>
<img src="https://i.imgur.com/O4gXcYg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
XVI. At this point, osTicket is fully installed and ready for work!
</p>
<br />
