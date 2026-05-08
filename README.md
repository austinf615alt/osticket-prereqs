<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This project outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows Server 2025 Datacenter X64 Gen2</b>

<h2>List of Prerequisites</h2>

- Internet Information Services (IIS)
- PHP Manager for IIS
- Rewrite Module
- PHP 7.3.8 
- MySQL 5.5.62
- HeidiSQL

<h2>Installation Steps</h2>

<p>
<img width="2560" height="1277" alt="image" src="https://github.com/user-attachments/assets/5ad5484c-f8f2-45e6-acad-7293e4d15511" />
</p>
<p>

- Configured and deployed a Windows Virtual Machine within Azure named osTicketSys using a Windows Server 2025 Datacenter X64 Gen2 image. Used Remote Desktop Connection to remote into Virutal Machine using VM public IP address and administrator account.

</p>
<br />

<p>
<img width="2191" height="1115" alt="LAB2-osTicketSetup" src="https://github.com/user-attachments/assets/cf651302-331d-4178-898e-b19a7cd51dca" />
</p>
<p>

- Installed Internet Information Services (IIS) with required components such as World Wide Web Services and Application Development Features with CGI enabled. Verfified IIS functionality using loopback address in browser.

</p>
<br />

<p>
<img width="2403" height="1216" alt="LAB2-osTicketSetup3" src="https://github.com/user-attachments/assets/30254f76-f097-4bb6-863d-b088caece245" />
</p>
<p>
  
- Installed and configured the required components to host osTicket on a web server:
  - PHP Manager for IIS
  - Rewrite Module
  - PHP 7.3.8 (extracted to a newly made directory: C:\PHP)
  - Visual C++ Redistributable (x86)
  - MySQL 5.5.62
 
- Configured PHP within IIS and restarted IIS services to apply changes.

- Deployed and configured osTicket v.1.15.8 on IIS by placing application files in the IIS web server directory (C:\inetpub\wwwroot) for hosting, renaming and organizing application files in appropriate directories, and configuring IIS to allow web access to osTicket.

- Enabled required PHP extensions for full application compatibility and configured file permissions to support osTicket functionality.

</p>
<br />

<p>
<img width="2403" height="1216" alt="Lab2-osTicketSetupEnd" src="https://github.com/user-attachments/assets/ab1234a0-3e69-4947-8d81-128a83ee0440" />
</p> 
<p>

- Installed HeidiSQL and created a new database for osTicket, then setting up osTicket with database credentials and fully installed osTicket on system.
