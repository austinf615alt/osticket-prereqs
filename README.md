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

- Internet Information Services (IIS): Provides the web server environment used to host the osTicket web application.
- PHP Manager for IIS: Enables configuration and integration of PHP within IIS to support server-side processing for osTicket
- Rewrite Module: Handles URL routing and rewriting to support proper navigation and functionality within the web application. 
- PHP: Server-side scripting language used to run the osTicket application logic.
- VC Redistributable: Provides required runtime libraries needed for PHP and related components to function correctly.
- MySQL: Relational database used to store osTicket data such as tickets, users, and system configurations.
- HeidiSQL: Database management tool used to create and manage the MySQL database for osTicket.

<h2>High-level Overview</h2>

- Section 1: Virtual Machine Creation - Covers the configuration and deployment of a Windows Server virtual machine in Microsoft Azure.
  
- Section 2: Web Server and osTicket prerequisites setup. - Installed and configured Internet Information Services (IIS) and osTicket dependencies for web app hosting.

- Section 3: Database Configuration - Installed and configured MySQL, creating and connecting a database used by osTicket for ticket and user data storage.
  
- Section 4: osTicket Deployment and Configuration - Deployed the osTicket application into the IIS web root, configured file permissions, enabling required PHP extensions, and completed the web-based setup process.

---

## Section 1: Virtual Machine Creation:

---

### Step 1: Resource Group Creation

 <p> 
<img width="1624" height="971" alt="RG Creation" src="https://github.com/user-attachments/assets/ee5b6967-5219-4fad-ad2c-8d669de3d9f8" />
</p>
<p>

- Created an Azure Resource Group called "osTicket-RG" to organize and manage all resources associated with the osTicket deployment environment.

</p>
<br />

---

### Step 2: Virtual Machine Configuration 

<p>
<img width="1624" height="971" alt="VM Nav" src="https://github.com/user-attachments/assets/096f3d9a-8299-432a-b931-a716c4d52cf6" />
</p>
<p>

- Navigated to the Azure Virtual Machine creation portal to begin creating the virtual machine for osTicket.

</p>
<br />

---

<p>
<img width="1624" height="971" alt="osTicket-VM Creation 1" src="https://github.com/user-attachments/assets/e31f000a-d7ca-425d-86a4-089136655fcf" />
</p>
<p>

- Configured the virtual machine within the "osTicket-RG" resource group, naming it "osTicket-VM" and setting it in the "(US) East US" region.
  
</p>
<br />

---

<p>
<img width="1624" height="971" alt="osTicket-VM Creation 2" src="https://github.com/user-attachments/assets/413ba0ae-a74c-4bb5-91f3-6edc798f3d9d" />
</p>
<p>

- Configured the virtual machine by selecting the "Windows Server 2025 Datacenter X64 Gen2" image, allocating 2 VCPUs and 16GiB of memory for performance, and created the local administrator account "labuser" with a secure password.

</p>
<br />

---

<p>
<img width="1624" height="971" alt="osTicket-VM Creation VNet" src="https://github.com/user-attachments/assets/a2e7e947-2b20-411e-9c7d-acd5c7a17fef" />
</p>
<p>

- Verified the automatically generated Azure virtual network and subnet configuration to ensure the proper internal connectivity for the VM environment. 

</p>
<br />

---

<p>
<img width="1624" height="971" alt="osTicket-VM Creation End" src="https://github.com/user-attachments/assets/350ae0e5-7f1f-450a-b973-0721430dc8e0" />
</p>
<p>

- Reviewed all virtual machine and networking configurations prior to deployment to ensure correct settings and successful provisioning.

</p>
<br />

---

<p>
<img width="1624" height="974" alt="VM Verify" src="https://github.com/user-attachments/assets/cd333343-56fd-4d2f-a924-33f05a275c3a" />
</p>
<p>

- Verified successful creation and deployment of the "osTicket-VM" virtual machine and associated Azure resources within the "osTicket-RG" resource group.

</p>
<br />

---

## Section 2: Web Server and osTicket prerequisites setup

---

### Step 1: Connected to the osTicket Windows VM via Remote Desktop

<p>
<img width="1624" height="971" alt="VM RDC Info" src="https://github.com/user-attachments/assets/05651b9c-ac99-4d3d-9633-000eee108379" />
</p>
<p>

- Noted Virtual Machine's public IP address to use for Remote Desktop.

</p>
<br />

---
<p>
<img width="1624" height="974" alt="RD-Windows-Server" src="https://github.com/user-attachments/assets/190e5a3f-4293-4819-91f9-d3a6ee173efe" />
</p>
<p>

- Used the VM's public IP address and local administrator credentials in Remote Desktop to access the VM Windows environment. 

</p>
<br />

---

### Step 2: Download and Prepare osTicket Installation Files

<p>
<img width="1624" height="971" alt="osTicket File Download" src="https://github.com/user-attachments/assets/b7ff2c18-d537-404d-a95e-1dc3065b9197" />
</p>
<p>

- Downloaded the osTicket installation package containing the required dependencies and setup files for the environment.

</p>
<br />

---
<p>
<img width="1624" height="971" alt="osTicket File Extract" src="https://github.com/user-attachments/assets/075c6a15-df4d-4ed8-be75-70eb845f4626" />
</p>
<p>

- Extracted the zipped osTicket Installation Files to prepare for setup.

</p>
<br />

---
<p>
<img width="1624" height="974" alt="osTicket File Contents" src="https://github.com/user-attachments/assets/5d3cb071-b5e0-4160-a31c-b831e5e1f586" />
</p>
<p>

- Verified the extracted installation directory contents, including HeidiSQL, MySQL, PHP, PHP Manager, Rewrite Module, and VC Redistributable.

</p>
<br />

---

### Step 3: Configure Web Server Environment

<p>
<img width="1624" height="974" alt="Add Roles and Features" src="https://github.com/user-attachments/assets/d031c62e-76d6-4e63-8963-459d67672f60" />
</p>
<p>

- Opened Server Manager and navigated to "Add Roles and Features" to begin configuring the web server environment.

</p>
<br />

---
<p>
<img width="1624" height="974" alt="Enable IIS" src="https://github.com/user-attachments/assets/16b4a25e-1f14-400f-8973-cc45bf3c2d33" />
</p>
<p>

- Enabled Internet Information Services (IIS) and required web server features.

</p>
<br />

---
<p>
<img width="1624" height="974" alt="Enable App Dev and CGI" src="https://github.com/user-attachments/assets/bd6c2e75-b266-4aab-8c1b-d323728787e8" />
</p>
<p>

- Enabled CGI support within IIS and Application Development to support PHP processing for osTicket

</p>
<br />

---
<p>
<img width="1624" height="974" alt="Loopback: IIS Disabled" src="https://github.com/user-attachments/assets/09df39d0-b073-4aba-ab34-aeb3fb87478f" />
</p>
<p>

- Accessed the loopback address "127.0.0.1" in a web browser to verify that the web server was not active prior to IIS installation.

</p>
<br />

---
<p>
<img width="1624" height="974" alt="Feature Confirmation" src="https://github.com/user-attachments/assets/7e2de233-752a-47a9-ac1b-c0e9a9d4ced8" />
</p>
<p>

- Successfully installed IIS and associated web server features required for osTicket hosting.

</p>
<br />

---
<p>
<img width="1624" height="976" alt="IIS Enabled" src="https://github.com/user-attachments/assets/fd6bcb81-80c6-4cb9-a464-b9fc2410a275" />
</p>
<p>

- Accessed the loopback address 127.0.0.1 after IIS installation to verify that web server was now active after successfully installing IIS and associated web server features.

</p>
<br />

---

### Step 4: Install osTicket Dependencies

<p>
<img width="1624" height="979" alt="Install PHP Manager" src="https://github.com/user-attachments/assets/73cc7512-1a9f-4122-b3f8-2f29dc9db2cb" />
</p>
<p>

- Opened and successfully installed "PHP Manager for IIS" from the osTicket Installation package to support PHP configuration within IIS.

</p>
<br />

---
<p>
<img width="1624" height="979" alt="Install Rewrite" src="https://github.com/user-attachments/assets/b03a22a9-d202-482c-bf8f-29ea97cc5a13" />
</p>
<p>

- Opened and successfully installed the "rewrite-amd64" module from the osTicket Installation package to support web application URL routing and functionality.

</p>
<br />

---
<p>
<img width="1624" height="979" alt="Extract into PHP" src="https://github.com/user-attachments/assets/42b74aef-4ea6-49c2-8046-caa69812463f" />
</p>
<p>

- Created a "C:\PHP" directory and extracted the "PHP-7.3.8" installation files into the "C:\PHP" directory for IIS integration and osTicket support.

</p>
<br />

---
<p>
<img width="1624" height="979" alt="PHP Folder" src="https://github.com/user-attachments/assets/dfb4b61e-a361-44ee-b929-72a294cd7158" />

</p>
<p>

- Verified that the PHP installation files were successfully extracted to the "C:\PHP" directory.

</p>
<br />

---
<p>
<img width="1624" height="979" alt="Install VC" src="https://github.com/user-attachments/assets/63550acc-8450-4c49-aacd-391214b25293" />
</p>
<p>

- Opened and successfuly installed "VC-redist_x86" from the osTicket Installation package, providing the required runtime libraries needed for PHP and related components to function correctly.

</p>
<br />

---

## Section 3: Database Configuration

---

### Step 1: Install and Configure MySQL

<p>
<img width="1624" height="979" alt="Install MySQL" src="https://github.com/user-attachments/assets/4586eff9-472a-45ee-9282-d2dc958b0356" />
</p>
<p>

- Successfully installed "mysql-5.5.62" and launched the MySQL Instance Configuration Wizard to configure the database server environment.

</p>
<br />

---
<p>
<img width="1624" height="979" alt="MySQL Config 1" src="https://github.com/user-attachments/assets/e0a72cbb-c233-411b-93f0-df25d18d587c" />
</p>
<p>

- Configured the MySQL server instance using the "Standard Configuration" option.

</p>
<br />

---
<p>
<img width="1624" height="976" alt="MySQL Config 2" src="https://github.com/user-attachments/assets/36d8986f-5fb2-479d-864f-67434b6a3bff" />
</p>
<p>

- Configured MySQL root account credentials required for osTicket database integration.

- Note: Credentials used in this lab environment were simplified for instructional purposes. In production environments, least privilege principles and secure credential management practices should be implemented.

</p>
<br />

---
<p>
<img width="1624" height="985" alt="MySQL Config Finish" src="https://github.com/user-attachments/assets/8c44590e-0391-4968-ad9c-f310f8c0fd2f" />
<p>

- Completed the MySQL Server Instance Configuration Wizard, enabling the database environment needed for osTicket integration.

</p>
<br />

---

## Section 4: osTicket Configuration and Deployment

---

### Step 1: Configure PHP Manager within IIS

<p>
<img width="1624" height="974" alt="IIS Manager" src="https://github.com/user-attachments/assets/e156aa88-b87a-43d0-bf37-7f9f4d95323f" />
</p>
<p>

- Opened Server Manager and navigated to "Internet Information Services (IIS) Manager" to begin configuring PHP integration for the osTicket environment.

</p>
<br />

---
<p>
<img width="1624" height="974" alt="Add PHP Exec" src="https://github.com/user-attachments/assets/a03f496d-630a-4c42-b2aa-6ebc369c7ef2" />
</p>
<p>

- Registered a new PHP version within PHP Manager, using the previously made PHP folder to provide a path to the PHP executable file as "C:\PHP\php-cgi.exe".

</p>
<br />

---

### Step 2: Install and configure osTicket files

<p>
<img width="1624" height="976" alt="Extract osTicket" src="https://github.com/user-attachments/assets/82161d92-d15b-4238-845b-4232c7ce3680" />
</p>
<p>

- Opened and extracted the "osTicket-v1.15.8" file within the osTicket Installation package to the desktop.

</p>
<br />

---
<p>
<img width="1624" height="976" alt="Renamed Upload" src="https://github.com/user-attachments/assets/3edb333a-5c9b-44a1-ac02-45caa3f809d9" />
</p>
<p>

- Copied the “upload” folder from the extracted osTicket package into “c:\inetpub\wwwroot”, renaming it to "osTicket" within the wwwroot folder to prepare the application for IIS hosting.

</p>
<br />

---
<p>
<img width="1624" height="974" alt="osTicket Site" src="https://github.com/user-attachments/assets/c13593bd-10ac-4adb-9bcc-9990f847496a" />
</p>
<p>

- Navigated to the osTicket site within IIS Manager and verified that the web server is successfully hosting the osTicket application.

</p>
<br />

---
<p>
<img width="1624" height="976" alt="PHP Extensions" src="https://github.com/user-attachments/assets/32016979-b42d-4e69-ac5c-46f48b17185d" />
</p>
<p>

- Within PHP Manager in IIS Manager, enabled required PHP extensions, including php_imap and php_intl, to support full osTicket functionality. Verified the changes were reflected in the osTicket web interface.

</p>
<br />

---
<p>
<img width="1624" height="979" alt="Rename ostsampleconfig" src="https://github.com/user-attachments/assets/6bb1bee3-bb5f-4d4a-b3be-cbdb9ffbc730" />
</p>
<p>

- Navigated to "C:\inetpub\wwwroot\osTicket\include" in File Explorer and renamed "ost-sampleconfig.php" to "ost-config.php".

</p>
<br />

---
<p>
<img width="1624" height="979" alt="Permissions ostsampleconfig" src="https://github.com/user-attachments/assets/6edbf598-6e56-4ee1-b7c2-60691065ebf5" />
</p>
<p>

- Opened the security properties for "ost-config.php", disabled permission inheritance, and removed existing inherited permissions. Assigned full control permissions to Everyone to allow osTicket to write configuration data during setup.

- Note: Granting full control to Everyone is only for lab installation purposes only. In production environments, file permissions should be restricted using the principle of least privilege to prevent unauthorized access or modification.

</p>
<br />

---
<p>
<img width="1624" height="979" alt="osTicket Setup" src="https://github.com/user-attachments/assets/9ff116e6-213c-42f9-80e6-3cb16cbc528c" />
</p>
<p>

- Continued osTicket setup through the web interface by configuring administrative account settings. Database configuration fields remained uncompleted at this stage, as the MySQL database had not yet been fully created and connected via HeidiSQL.

</p>
<br />

---

### Step 3: Install and Configure HeidiSQL Database

<p>
<img width="1624" height="979" alt="Install HeidiSQL" src="https://github.com/user-attachments/assets/1e82d9a8-569b-487b-946f-aadd0bc507ab" />

</p>
<p>

- Opened and installed HeidiSQL in the osTicket Installation package, launching HeidiSQL to configure database. 

</p>
<br />

---
<p>
<img width="1624" height="979" alt="MySql Credentials" src="https://github.com/user-attachments/assets/a109885b-2370-436d-a709-9354c85c1a1f" />
</p>
<p>

- Created a new HeidiSQL session using MySQL root credentials (root/root), connecting to the database server.

</p>
<br />

---
<p>
<img width="1624" height="979" alt="Creating osTicket Database" src="https://github.com/user-attachments/assets/4459e969-d2de-499e-a775-09bf758b3320" />
</p>
<p>

- Created a new databse called "osTicket", allowing application data to be stored.

</p>
<br />

---

### Step 4: Finalizing osTicket deployment

<p>
<img width="1624" height="979" alt="Setup Finish" src="https://github.com/user-attachments/assets/35531f61-8a5e-4797-85ca-ee356d6b1097" /> 
</p>
<p>

- Completed osTicket setup through the web interface by configuring the MySQL database name and credentials, finalizing the installation of the application.

</p>
<br />

---
<p>
<img width="1624" height="979" alt="Setup Success" src="https://github.com/user-attachments/assets/64c0534b-63b2-46aa-ab69-3f9ac30983f8" />
</p>
<p>

- Successfully completed the osTicket installation process, confirmed by the “Congratulations” page indicating full deployment of the application.

</p>
<br />

---
