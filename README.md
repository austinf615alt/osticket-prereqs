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

- Internet Information Services (IIS): Hosted the osTicket web application on the Windows Server Environment.
- PHP Manager for IIS: Configured and managed PHP integration within IIS.
- Rewrite Module: Enabled URL handling and web application routing functionality for osTicket
- PHP: Powered the backend functionality of the osTicket application.
- VC Redistributable: Installed required runtime dependencies for PHP and related components.
- MySQL: Stored osTicker user, ticket, and configuration data.
- HeidiSQL: Managed and configured the MySQL database used by osTicket.

<h2>High-level Overview</h2>

- 1. Created an Azure resource group and deployed a Windows Server 2025 virtual machine to host the osTicket environment.
- 2. Connected to the VM using Remote Desktop and prepared the environment for web application hosting.
- 3. Installed and configured Internet Information Services, PHP, CGI, and required dependencies for osTicket functionality.
- 4. Configured MySQL and created a database for ticket storage and management.
- 5. Deployed and configured the osTicket help desk platform within the IIS web server environment.
- 6. Enabled required PHP extensions and adjusted file permissions to complete application setup.
- 7. Verified successful installation by accessing the osTicket admin and end-user web portals.

## Step 1: Virtual Machine Creation:

<p>
<img width="1624" height="971" alt="RG Creation" src="https://github.com/user-attachments/assets/ee5b6967-5219-4fad-ad2c-8d669de3d9f8" />
</p>
<p>

- Placeholder

</p>
<br />

<p>
<img width="1624" height="971" alt="VM Nav" src="https://github.com/user-attachments/assets/096f3d9a-8299-432a-b931-a716c4d52cf6" />
</p>
<p>

- Placeholder

</p>
<br />

<p>
<img width="1624" height="971" alt="osTicket-VM Creation 1" src="https://github.com/user-attachments/assets/e31f000a-d7ca-425d-86a4-089136655fcf" />
</p>
<p>

- Placeholder

</p>
<br />

<p>
<img width="1624" height="971" alt="osTicket-VM Creation 2" src="https://github.com/user-attachments/assets/413ba0ae-a74c-4bb5-91f3-6edc798f3d9d" />
</p>
<p>

- Placeholder

</p>
<br />

<p>
<img width="1624" height="971" alt="osTicket-VM Creation VNet" src="https://github.com/user-attachments/assets/a2e7e947-2b20-411e-9c7d-acd5c7a17fef" />
</p>
<p>

- Placeholder

</p>
<br />

<p>
<img width="1624" height="971" alt="osTicket-VM Creation End" src="https://github.com/user-attachments/assets/350ae0e5-7f1f-450a-b973-0721430dc8e0" />
</p>
<p>

- Placeholder

</p>
<br />

<p>
<img width="1624" height="974" alt="VM Verify" src="https://github.com/user-attachments/assets/cd333343-56fd-4d2f-a924-33f05a275c3a" />
</p>
<p>

- Placeholder

</p>
<br />
