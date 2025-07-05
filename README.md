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

- osTicket v1.15.8 (osTicket-v1.15.8.zip)

- PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)

- Rewrite Module (rewrite_amd64_en-US.msi)

- PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip)

- VC Redistributable (VC_redist.x86.exe)

- MySQL 5.5.62 (mysql-5.5.62-win32.msi)


<h2>Installation Steps</h2>

- Step 1: download the osTicket-Installation-Files.zip and unzip/extract

 - link -> https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD

- Step 2: Install / Enable IIS in Windows WITH CGI

 - Control panel -> Programs -> Uninstall Programs -> Turn Windows features onoff

 - Check Internet Information Services

 - www services -> App Dev Features -> CGI

- Step 3: Inside osTicket Folder install required software

&emsp; - PHP Manager for IIS (`PHPManagerForIIS_V1.5.0.msi`)
 
 &emsp; - Rewrite Module (`rewrite_amd64_en-US.msi`)
 
 &emsp; - VC Redist (`VC_redist.x86.exe`)

  - Step 4: Create a folder in C drive called "PHP"
    
  - In osTicket folder extract  `php-7.3.8-nts-Win32-VC15-x86.zip` into `C\PHP` folder
    
  - Step 5: Install MYSQL

  &emsp; - Run `mysql-5.5.62-win32.msi`
  
  &emsp; - Choose **Typical Setup**
   
 &emsp; - Launch Configuration Wizard (after install)
 
 &emsp; -  Use **Standard Configuration**
   
 &emsp; - Set credentials:
 &emsp;Username: `root`
 &emsp;Password: `root`

- Step 6: Configure PHP in IIS

 &emsp; - Open IIS Manager as an administrator.

 &emsp; - Register PHP:

 &emsp; - Go to PHP Manager.

 &emsp;- Register C:\PHP\php-cgi.exe.

 &emsp;- Reload IIS (Stop and Start the server).

  
