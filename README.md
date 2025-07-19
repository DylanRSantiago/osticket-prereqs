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

 -  Check Internet Information Services -> WWW services  -> App Development Features -> CGI

- Step 3: Inside osTicket Folder install required software

&emsp; - PHP Manager for IIS (`PHPManagerForIIS_V1.5.0.msi`)
 
 &emsp; - Rewrite Module (`rewrite_amd64_en-US.msi`)
 

  - Step 4: Create a folder in C drive called "PHP"
    
   - Step 5:  In osTicket folder extract  `php-7.3.8-nts-Win32-VC15-x86.zip` into `C\PHP` folder

- Step 6: install VC Redist (`VC_redist.x86.exe`)
    
- Step 7: Install MYSQL

  &emsp; - Run `mysql-5.5.62-win32.msi`
  
  &emsp; - Choose **Typical Setup**
   
 &emsp; - Launch Configuration Wizard (after install)
 
 &emsp; -  Use **Standard Configuration**
   
 &emsp; - Set credentials:
 &emsp;Username: `root`
 &emsp;Password: `root`

- Step 8: Configure PHP in IIS

 &emsp; - Open IIS Manager as an administrator.

 &emsp; - Go to PHP Manager.

  &emsp; - Register new php version -> browse to php folder inside get “php-cgi”

 &emsp;- Reload IIS (Stop and Start the server).

- Step 9: Install osTicket  

 &emsp;- Unzip osTicket v1.15.8 (`osTicket-v1.15.8.zip`).

 &emsp;- Copy the upload folder into C:\inetpub\wwwroot.

 &emsp;- Rename upload to osTicket.

 &emsp;- Reload IIS (Stop and Start the server).

 &emsp;- Open IIS, go to Sites -> Default -> osTicket.

 &emsp;- Click *Browse :80 to verify the installation.
 
- Step 10: Enable  required PHP Extensions
  
  &emsp;- ISS -> Sites -> Default sites -> osTicket
  
  &emsp;&emsp;&emsp;- double click PHP manager (icon)

  &emsp;&emsp;&emsp;- click "enable or disable an extension" 

  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;- Enable: php_imap.dll

  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;- Enable: php_intl.dll

  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;- Enable: php_opcache.dll

  &emsp;- Refresh osTicket browser and see they are enabled

- Step 11: Configure osTicket
  
&emsp;- Rename ost-sampleconfig.php to ost-config.php:

&emsp;- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php

&emsp;- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

&emsp;- Assign permissions to ost-config.php:

&emsp; - Right click-> properties -> security -> advancted -> Disable inheritance -> remove all

&emsp;- Add - Select Principle- Type Everyone- Check Full Control.

&emsp;- Continue setting up osTicket in the browser:

&emsp;- Name your Helpdesk.
 
   &emsp; - username : Itprofessional

   &emsp; - Password: Password1

&emsp;- Set the default email (receives emails from customers).

- Step 12: Set Up MySQL Database

&emsp;- Install and open HeidiSQL.

&emsp;- Create a new session with:

&emsp;- Username: root

&emsp;- Password: root

&emsp;- Connect to the session and create a database named osTicket.

&emsp;- Continue setting up osTicket in the browser:

&emsp;- MySQL Database: osTicket

&emsp;- MySQL Username: root

&emsp;- MySQL Password: root

&emsp;- Click Install Now!

- Step 14: Access osTicket

 &emsp;- login page: http://localhost/osTicket/scp/login.php

  &emsp;&emsp;- Username: Itprofessional

  &emsp;&emsp;- Password: Password1

  &emsp;- Enter Tickets: http://localhost/osTicket/
