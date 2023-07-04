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

- Have an Azure Cloud Subscription
- Create an Azure Virtual Machine (Windows 10 OS)
- Acquire the Installation Files for osTicket


<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/7U9wBib.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First I used 'Remote Destop Connection' to gain access to my VM, then I went to the windows control panel and installed IIS. Once installed, I navigated through the management console to enable both CGI and Common HTTP Features. 
</p>
<br />

<p>
<img src="https://i.imgur.com/1ka2l7v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here I first created the directory C:\PHP then I went into the installation files and downloaded and installed the files in this order: PHP Manager for IIS, Rewrite Module, PHP-7.3.8(unzip the contents into C:\PHP), VC_redist.x86.exe, MySQL-5.5.62. After that I reopened IIS as an admin, registered PHP from within IIS and installed osTIcket v1.15.8. 
</p>
<br />

<p>
<img src="https://i.imgur.com/zkSL2Tx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After osTicket installed I reloaded IIS and went to Sites ->Default ->osTicket and clicked on "Browse *:80". Then to enabled some neccesary extensions I went to Sites ->Default ->osTicket, double-clicked PHP Manager, clicked "Enable or disable an extension" and enabled php_imap.dll, php_intl.dll, and php_opcache.dll. Next I assigned permissions to everyone in the file ost-config.php and further setup osTicket. Finally I installed HeidiSQL from the installation files, created a new session, connected to that session and created a database called "osTicket" and used that database to finish setting up osTicket in the browser.
</p>
<br />
