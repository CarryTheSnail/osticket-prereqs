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

- Install/Enable IIS - CGI and Common HTTP Features 
- Install PHP Manager (PHPManagerForIIS_V1.5.0 and php-7.3.8-nts-Win32-VC15-x86 Files) 
- Install Rewrite Module (rewrite_amd64_en-US)
- Install C++ redistributable (VC_redist.x86)
- Install MySQL (mysql-5.5.62-win32)
- Install HeidiSQL (HeidiSQL_12.3.0.6589_Setup)
- Install osTicket-v1.15.8

![image](https://github.com/user-attachments/assets/5da7e2b8-594b-4e5a-a93e-7c1895c7a7e7)

The prerequisite files can be found on osTicket installation documentations

<h2>Installation Steps</h2>

Start by Installing IIS and enabling CGI and Common HTTP Features
<p>
  
![image](https://github.com/user-attachments/assets/6dedf93b-e6e6-46d8-bebc-f79d36ff9ec4)

</p>
<p>
Installing/Enabling IIS allows you to host osTicket. IIS is a web server built into Windows. oSTicket is a web-based application. Enabling IIS allows you to run PHP which is the server language that osTicket is written in. </p>
<br />

Install PHP Manager, Rewrite Module, and C++ Redistributable

![image](https://github.com/user-attachments/assets/93bb27d3-f6b4-4210-9b2d-fefcbf67f9e2)


<p>
</p>
<br />

Register PHP from within IIS
1. Create the directory C:\PHP
2. Unzip php-7.3.8-nts-Win32-VC15-x86 into C:\PHP
3. Open IIS
4. 
![image](https://github.com/user-attachments/assets/53b4575c-e9e0-422d-8372-1fc26031587a)

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
