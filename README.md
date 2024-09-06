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


Install MySQL. (*** Remember the login credentials***)

![image](https://github.com/user-attachments/assets/60967c23-9990-488a-99a7-c3cf4adcee02)
Using MySQL for database in this osTicket project


Register PHP from within IIS
  1. Create the directory C:\PHP
  2. Unzip php-7.3.8-nts-Win32-VC15-x86 into C:\PHP

     ![image](https://github.com/user-attachments/assets/53b4575c-e9e0-422d-8372-1fc26031587a)


  4. Run IIS as an Admin
  5. Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)

     ![image](https://github.com/user-attachments/assets/ef76fe41-3e6e-49da-9207-377f810f93d5)


Install osTicket
  1. Unzip osTicket-v1.15.8 and copy the "upload" folder into "C:\inetpub\wwwroot"
  2. Within "c:\inetpub\wwwroot", rename "upload" to "osTicket"
     
     ![image](https://github.com/user-attachments/assets/f502ba12-f049-40ad-bca8-be24ce496feb)

  4. Reload IIS. On the right, click "Browse *80"
     
     ![image](https://github.com/user-attachments/assets/b052fe5e-865e-40ee-bb05-1b9245d0d0c7)

     ![image](https://github.com/user-attachments/assets/61c22b67-86dd-4b85-b0c5-bc90e80a5ede)

  6. Enable extensions through PHP Manager. (php_imap.dll, php_intl.dll, php-opache.dll)
     
     ![image](https://github.com/user-attachments/assets/5fce2a8c-d8be-4d6d-917b-ac449a0cee8c)

  8. Rename "ost-config.php" to "ost-config.php". File is found in C:\inetpub\wwwroot\osTicket\include\ost-config.php
     
     ![image](https://github.com/user-attachments/assets/bf021062-8bc1-486c-b582-e4248f3dfe70)

  10. Assign permissions: ost-config.php. Diable inheritance and add new permission. Everyon -> All.

      ![image](https://github.com/user-attachments/assets/e28b9088-0f34-4d6c-8194-2baee3144c6a)
      
Setup osTicket
  1. Continue Setting up osTicket in browser (click continue)
     - Fill out credentials (and remember them/write it down)
       
       ![image](https://github.com/user-attachments/assets/b34cc90c-3ddd-4723-816e-5e101084db60)

  2. Install HeidiSQL

     ![image](https://github.com/user-attachments/assets/84043978-e059-4003-ab99-64808550374c)

  4. Open HeidiSQL
     - Create a new session
     - Connect to the sessoin
     - Create a database called "osTicket"
       
       ![image](https://github.com/user-attachments/assets/359f0ad8-cda2-435d-b56e-2b4a722725e6)

  5. Finish setting up osTicket in the browser:
     - MySQL Database: osTicket
     - MySQL Username: root
     - MySQL Password: (whatever you used when installing MySQL)
     - Install!
       
       ![image](https://github.com/user-attachments/assets/2c104074-9fcd-4ce2-9174-1616be684e79)

The Final Step is to Clean Up:
  1. Delete: C:\inetpub\wwwroot\osTicket\setup
  2. Set "C:\inetpub\wwwroot\osticket\include\ost-config.php" permission to read only. 

<br />
