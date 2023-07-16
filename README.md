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
- Internet Information Services (IIS) with CGI

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- PHP Manager for IIS 
- Rewrite Module
- PHP
- Visual C++
- MySQL (using HeidiSQL)

<h2>Installation Steps</h2>

<p>
Internet Information Services (ISS) with CGI features must be added to windows for the installation of osTicket.
</p>

<p>
<img src="https://i.imgur.com/x3Jiap7.jpg" height="30%" width="30%" alt="Windows Search Bar"/>
</p>
<p>
Type or copy and paste "C:\Windows\System32\OptionalFeatures.exe" into the Window's search bar. This will bring up an option to turn Windows features on or off.
</p>
<br />

<p>
<img src="https://i.imgur.com/bsMDewg.png" height="30%" width="30%" alt="Windows Features"/>
</p>
<p>
The Window should look like the above screen shot.
</p>
<br />

<p>
<img src="https://i.imgur.com/ucI5Ja2.png" height="30%" width="30%" alt="IIS"/>
</p>
<p>
Check the box for Internet Information Services shown above.
</p>

<p>
<img src="https://i.imgur.com/Nyl2vhO.png" height="30%" width="30%" alt="CGI  "/>
</p>

<p>
Check the CGI Box under Expand Internet Information Services > World Wide Webs Services > Application Development Feature > CGI show above.
</p>

<p>
<img src="https://i.imgur.com/gcIg8L5.png" height="50%" width="50%" alt="Common HTTP Features"/>
</p>
<p>
Also Check all the Common HTTP Features shown above.
</p>

<p>
<img src="https://i.imgur.com/9EgdWl4.png" height="30%" width="30%" alt="ISS check"/>
</p>
<p>
Check if IIS has setup correctly by typing a loopback address into your browser "127.0.0.1". The page above should load.  
</p>


These shared [Installation files](https://drive.google.com/drive/folders/1Zy6qPGc7fs0zD8q6cXMNQ7H7uAZB2yYK?usp=sharing) will be downloaded and installed.
<p>
<img src="https://i.imgur.com/TVqHEYY.png" height="60%" width="60%" alt="Google Drive"/>
</p>
<p> Click the "Download all" button in the top right </p>
<p>
<img src="https://i.imgur.com/otYdqIi.png" height="60%" width="60%" alt="osTicketIntallationFiles"/>
</p>
<p> Navigate to the folder just downloaded "C:\...\Downloads\osTicketInstallationFiles-20230712T220757Z-001.zip\osTicketInstallationFiles" (your path maybe for a different user) and 
<p>
<img src="https://i.imgur.com/NW5k1hv.png" height="60%" width="60%" alt="Google Drive"/>
</p>
<p> Extract the content of the zip file to the downloads folder, you should be redirected to the folder extracted to.</p>
<p>
Install PHP Manager for IIS, "PHPManagerForIIS_V1.5.0.msi"  
</p>
<p>
Install Rewrite Module, "rewrite_amd64_en-US.msi" 
</p>
<br>
<p>
<img src="https://i.imgur.com/SCA128Z.png" height="60%" width="60%" alt="Google Drive"/>
</p>
<p> Create the directory C:\PHP (to copy PHP to) </p>
<p>
<img src="https://i.imgur.com/THJIdpD.png" height="65%" width="65%" alt="Google Drive"/>
</p>
<p> Copy contents of "php-7.3.8-nts-Win32-VC15-x86.zip" to "C:\PHP"  </p>

<p> Install Visual C++, VC_redist.x86.exe </p>
<p> Install MySQL 5.5.62, mysql-5.5.62-win32.msi and follow setup below </p>

<p> Typical Setup ->
<p>
<img src="https://i.imgur.com/t8D4JqE.png" height="40%" width="40%" alt="Google Drive"/>
</p>
Launch Configuration Wizard (after install) ->
<p>
<img src="https://i.imgur.com/fcmcBmZ.png" height="40%" width="40%" alt="Google Drive"/>
</p>
Click next until the below image is reached
<br>
Standard Configuration ->
<p>
<img src="https://i.imgur.com/DGgJaNj.png" height="40%" width="40%" alt="Google Drive"/>
</p>
Enter Password (remeber password for later) </p>
<p>
<img src="https://i.imgur.com/wfHeaI6.png" height="40%" width="40%" alt="Google Drive"/>
</p>
<p>Click Next and Execute </p>

Install osTicket v1.15.8
<br/>
<p>
<img src="https://i.imgur.com/0i0YEjw.png" height="65%" width="65%" alt="extract osTicket"/>
</p>  
<p>
<img src="https://i.imgur.com/Fd2YXRU.png" height="65%" width="65%" alt="PHP Manager"/>
</p>
Extract and copy “upload” folder to "c:\inetpub\wwwroot"
<br/>
<p>
<img src="https://i.imgur.com/a0oGBKg.png" height="65%" width="65%" alt="Rename osTicket"/>
</p>
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”
</p>
<p>
<img src="https://i.imgur.com/1YM5Fnz.png" height="65%" width="65%" alt="rename ost-sampleconfig"/>
</p>
</p>
Browse to "C:\inetpub\wwwroot\osTicket\include\" and rename "ost-sampleconfig.php" to "ost-config.php"
 <br/>
</p>
<p>
<img src="https://i.imgur.com/aBh1RRJ.png" height="65%" width="65%" alt="disable inheritence of ost-config"/>
</p>
</p>
Change the permissions of ost-config.php to everyone and disable inheritance.
<br/>
Right click on  ost-config.php and go to Properties -> Security -> Advanced -> Disable Inheritance -> Remove All Inherited Permissions
<br/>
<p>
<img src="https://i.imgur.com/HHs7XKB.png" height="30%" width="30%" alt="permissions ostconfig"/>
</p>
<p>
<img src="https://i.imgur.com/mysEJfs.png" height="30%" width="30%" alt="permissions ostconfig"/>
</p>
<p>
Add -> Select a principal -> enter "Everyone" into object name and click Okay
</p>
<p>
<img src="https://i.imgur.com/bIdEKaH.png" height="65%" width="65%" alt="PHP Manager"/>
</p>
<p>
Click "Full Control" -> Okay -> Okay
</p>

<p>
From the downloaded osTicket Installation Files, download and install HeidiSQL.
<p/>
<p>
<img src="https://i.imgur.com/k8lcXMZ.png" height="30%" width="30%" alt="PHP Manager"/>
</p>
<p>
Download, Install, and Launch HeidiSQL </p>
<p>
<img src="https://i.imgur.com/LThY6sr.png" height="30%" width="30%" alt="PHP Manager"/>
</p>
<p>
Create a new session 
</p>
<p>
<img src="https://i.imgur.com/8zQhxDK.png" height="65%" width="65%" alt="PHP Manager"/>
</p>
<p>
Type in password used to create MySQL database
<p>
<p>
<img src="https://i.imgur.com/av8TIQR.png" height="65%" width="65%" alt="PHP Manager"/>
</p>
<p>
Right click "Unamed" > Create > Database</p>
<p>
<p>
<img src="https://i.imgur.com/1soNcVG.png" height="30%" width="30%" alt="PHP Manager"/>
</p>
<p>
Name the database "osTicket" 
</p>
<p>
<img src="https://i.imgur.com/x3Jiap7.jpg" height="30%" width="30%" alt="Windows Search Bar"/>
</p>
<p>
<p> In the Windows Search bar type or copy and paste  "Internet Information Services (IIS) Manager" and click open as administrator shown below </p>
<p>
<img src="https://i.imgur.com/N5bUV6v.png" height="65%" width="65%" alt="Windows Search Bar"/>
</p>
<p>
<img src="https://i.imgur.com/x1QhYUh.png" height="65%" width="65%" alt="PHP Manager"/>
</p>
<p> Click on PHP Manager </p>
<p>
<img src="https://i.imgur.com/VhB5qzb.png" height="65%" width="65%" alt="PHP Manager Reg"/>
</p>
<p> Click on Register new PHP version </p>
<p>
<img src="https://i.imgur.com/j75FrES.png" height="65%" width="65%" alt="CGI"/>
</p>
<p> Provide the path "C:\PHP\php-cgi.exe" when prompted and click Okay</p>
<br/>
<p> 
<p>
<img src="https://i.imgur.com/2JFTEeJ.png" height="65%" width="65%" alt="PHP extensions"/>
</p>
Click “Enable or disable an extension”
<br/>
<p>
<img src="https://i.imgur.com/3KXN2kY.png" height="65%" width="65%" alt="PHP enable/disable extensions"/>
</p>
Enable: php_imap.dll by clicking on the extension and then clicking enable on upper right
<br/>
Enable: php_intl.dll
<br/>
Enable: php_opcache.dll
<br/>
</p>
<p>
<p>
<img src="https://i.imgur.com/uVtIesv.png" height="75%" width="75%" alt="PHP Manager"/>
</p>
<p>
Go to sites -> Default -> osTicket
<br/>
<img src="https://i.imgur.com/3QiYtkz.png" height="65%" width="65%" alt="PHP Manager"/>
</p>
<p>
Fill out the infromation, use the SQL username and password created when installing MySQL, use the database name "osTicket" created through HeidiSQL (keep note of usernames and passwords)</p>
<p>
<img src="https://i.imgur.com/FWeRlRm.png" height="65%" width="65%" alt="PHP Manager"/>
</p>
<p>
Fill out the infromation, use the SQL username and password created when installing MySQL, use the database name "osTicket" created through HeidiSQL (keep note of usernames and passwords) and install now
</p>
<p>
<img src="https://i.imgur.com/PT3X5to.png" height="65%" width="65%" alt="PHP Manager"/>
</p>
<p>
For security reasons  Delete: C:\inetpub\wwwroot\osTicket\setup and
<br/>
<p>
<img src="https://i.imgur.com/4rtCqwA.png" height="65%" width="65%" alt="PHP Manager"/>
</p> 
Set Permissions to “Read” and "Read and Execute" only for: C:\inetpub\wwwroot\osTicket\include\ost-config.php
 <br/>
</p>
<p>
<img src="https://i.imgur.com/rtm229j.png" height="50%" width="50%" alt="oTicket Loginscreen"/>
</p>
<p>
Browse to local help desk login page http://localhost/osTicket/scp/login.php and login with user name and password created 
</p>
<p>
