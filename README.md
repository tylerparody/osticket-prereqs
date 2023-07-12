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
<img src="https://i.imgur.com/gcIg8L5.png" height="30%" width="30%" alt="Common HTTP Features"/>
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
<img src="https://i.imgur.com/TVqHEYY.png" height="30%" width="30%" alt="Google Drive"/>
</p>
<p> Click the "Download all" button in the top right </p>
<p>
<img src="https://i.imgur.com/otYdqIi.png" height="30%" width="30%" alt="Google Drive"/>
</p>
<p> Navigate to the folder just downloaded </p>
<p> Install PHP Manager for IIS, PHPManagerForIIS_V1.5.0.msi </p>

<p> Download and Install Rewrite Module, rewrite_amd64_en-US.msi </p>

<p> Create the directory C:\PHP (to unzip PHP to) </p>

<p> Download and unzip to "C:\PHP" PHP 7.38, php-7.3.8-nts-Win32-VC15-x86.zip </p>

<p> Download and install Visual C++, VC_redist.x86.exe </p>

<p> Download and MySQL 5.5.62, mysql-5.5.62-win32.msi </p>
<p> Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration ->
Enter Password </p>

<p> Open IIS as an Admin </p>
<br />

