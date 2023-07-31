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

- Enable IIS in Windows with CGI        
- PHP manager for IIS
- Install Rewrite mod.
- Install C++ redist.
- My SQL-setup Username and Password

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/11R5yIS.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a Virtual Machine(VM) in Azure using Windows 10.
Be sure to create a VM with 2-4 virtual CPUs.
</p>
<br />

<p>
<img src="https://i.imgur.com/w9hddSR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Using a Remote Desktop Connection, connect your virtual machines IP address into Remote Desktop.
</p>
<br />

<p>
<img src="https://i.imgur.com/R79J6Qj.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Inside the VM, right click the Windows menu and type run->control.
</p>
<br />

<p>
<img src="https://i.imgur.com/RPivZNV.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click Programs->
</p>
<br />

<p>
<img src="https://i.imgur.com/xU2nclO.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>
</p>
<p>
Turn Windows feat.on or off-> Internet Information Services(IIS)-> World Wide Web Service->Application Development features->CGI
</p>
<br />

<p>
<img src="https://i.imgur.com/0boBWyx.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
CGI allows you to host a webpage on youe own Network. Test this by typing 127.0.0.1 in your google search barin your VM.
The webpage should look like this.
</p>
<br />

<p>
<img src="https://i.imgur.com/MvxduS9.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install PHP Manager for IIS.
</p>
<br />

<p>
<img src="https://i.imgur.com/M46Dnai.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install the Rewrite Module.
</p>
<br />

<p>
<img src="https://i.imgur.com/TjAe57R.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a folder on the C drive and name it PHP. Next, download and extract PHP 7.3.8 and unzip the content into the PHP folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/4vYJCvB.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install VC redist.x86.exe
</p>
<br />

<p>
<img src="https://i.imgur.com/UX0Vdm2.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install My SQL 5.5.62
</p>
<br />

<p>
<img src="https://i.imgur.com/0aXcU49.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click->Typical-> Standard Configuration-> Password1
</p>
<br />

<p>
<img src="https://i.imgur.com/ykxHWQo.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, Open IIS as an Admin.
</p>
<br />

<p>
<img src="https://i.imgur.com/hRCYA9V.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Register PHP from within IIS. Open PHP Manager, Register new PHP: C:-PHP-php-cgi.exe. Restart the server.
</p>
<br />

<p>
<img src="https://i.imgur.com/Zwzj5ya.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open osTicket-> upload. Extract the upload file into C:->Inetpub-> wwwroot. Remane the "upload" folder to "osTicket". Return to to IIs and restart the sever.
</p>
<br />

<p>
<img src="https://i.imgur.com/j1ltoGO.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Inside IIS->sites->default Web Services->osTicket->*80 to open osTicket in your browser.
</p>
<br />

<p>
<img src="https://i.imgur.com/bt0l24t.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/x2R7zeZ.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Some extensions are not enabled. So we need to enable these extensions so that osTicket can operate. In IIS, open sites->osTicket->PHP Manager-> Enable or disable extensions. Enable these extensions: php_opcache.dll, php_intl.dll, php_imap.dll. Refresh the osTicket tab in the browser.
</p>
<br />

<p>
<img src="https://i.imgur.com/rtkrjNZ.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Remane the file "Ostsampleconfig.php" to "Ost-config.php". Located in wwwroot->include->Ostsampleconfig.php
</p>
<br />

<p>
<img src="https://i.imgur.com/J4STVpi.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
  
<img src="https://i.imgur.com/C0T8ElJ.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we need to assign permissions for ost-config.php. First, open properties->security->advanced->disable->->remove all permissions. Then select "everyone" and apply.
</p>
<br />

<p>
<img src="https://i.imgur.com/OsSt6MT.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install Heidi SQL
</p>
<br />

<p>
<img src="https://i.imgur.com/fJRVMHS.png" height="50%" width="50%" alt="Disk Sanitization Steps"/> 
<IMG SRC="https://i.imgur.com/yIoMt7U.png" height="50%" width="50%" alt="Disk Sanitization Steps"/> 
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/SDaSM6R.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/lNf84lm.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/GpAyUrO.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


