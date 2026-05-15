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

- Internet Information Services (IIS): Hosted the osTicket web application within the Windows Server Environment.
- PHP Manager for IIS: Configured and managed PHP integration within IIS.
- Rewrite Module: Enabled URL handling and web application routing functionality for osTicket
- PHP: Powered the backend functionality of the osTicket application.
- VC Redistributable: Installed required runtime dependencies for PHP and related components.
- MySQL: Stored osTicket user, ticket, and configuration data.
- HeidiSQL: Managed and configured the MySQL database used by osTicket.

<h2>High-level Overview</h2>

- Step 1: Created an Azure resource group and deployed a Windows Server 2025 virtual machine to host the osTicket environment
- Step 2: Connected to the VM using Remote Desktop and prepared the environment for web application hosting.
- Step 3: Installed and configured Internet Information Services, PHP, CGI, and required dependencies for osTicket functionality.
- Step 4: Configured MySQL and created a database for ticket storage and management.
- Step 5: Deployed and configured the osTicket help desk platform within the IIS web server environment.
- Step 6: Enabled required PHP extensions and adjusted file permissions to complete application setup.
- Step 7: Verified successful installation by accessing the osTicket admin and end-user web portals.

---

## Step 1: Virtual Machine Creation:

<p>
<img width="1624" height="971" alt="RG Creation" src="https://github.com/user-attachments/assets/ee5b6967-5219-4fad-ad2c-8d669de3d9f8" />
</p>
<p>

- Created an Azure Resource Group called "osTicket-RG" to organize and manage all resources associated with the osTicket deployment environment.

</p>
<br />

---

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

- Continued configuring the virtual machine by selecting the  "Windows Server 2025 Datacenter X64 Gen2" image, allocating 2 VCPUs and 16GiB of memory for performance, and creating the local administrator account "labuser" with a secure password.

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

## Step 2: Remoting into VM and preparing the environment.

<p>
<img width="1624" height="971" alt="VM RDC Info" src="https://github.com/user-attachments/assets/05651b9c-ac99-4d3d-9633-000eee108379" />
</p>
<p>

- PH

</p>
<br />

---
<p>
<img width="1624" height="974" alt="RD-Windows-Server" src="https://github.com/user-attachments/assets/190e5a3f-4293-4819-91f9-d3a6ee173efe" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="971" alt="osTicket File Download" src="https://github.com/user-attachments/assets/b7ff2c18-d537-404d-a95e-1dc3065b9197" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="971" alt="osTicket File Extract" src="https://github.com/user-attachments/assets/075c6a15-df4d-4ed8-be75-70eb845f4626" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="974" alt="osTicket File Contents" src="https://github.com/user-attachments/assets/5d3cb071-b5e0-4160-a31c-b831e5e1f586" />
</p>
<p>

- ph

</p>
<br />

---

## Step 3: Installing required osTicket dependencies

<p>
<img width="1624" height="974" alt="Add Roles and Features" src="https://github.com/user-attachments/assets/d031c62e-76d6-4e63-8963-459d67672f60" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="974" alt="Enable IIS" src="https://github.com/user-attachments/assets/16b4a25e-1f14-400f-8973-cc45bf3c2d33" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="974" alt="Enable App Dev and CGI" src="https://github.com/user-attachments/assets/bd6c2e75-b266-4aab-8c1b-d323728787e8" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="974" alt="Loopback: IIS Disabled" src="https://github.com/user-attachments/assets/09df39d0-b073-4aba-ab34-aeb3fb87478f" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="974" alt="Feature Confirmation" src="https://github.com/user-attachments/assets/7e2de233-752a-47a9-ac1b-c0e9a9d4ced8" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="976" alt="IIS Enabled" src="https://github.com/user-attachments/assets/fd6bcb81-80c6-4cb9-a464-b9fc2410a275" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="979" alt="Install PHP Manager" src="https://github.com/user-attachments/assets/73cc7512-1a9f-4122-b3f8-2f29dc9db2cb" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="979" alt="Install Rewrite" src="https://github.com/user-attachments/assets/b03a22a9-d202-482c-bf8f-29ea97cc5a13" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="979" alt="Extract into PHP" src="https://github.com/user-attachments/assets/42b74aef-4ea6-49c2-8046-caa69812463f" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="979" alt="PHP Folder" src="https://github.com/user-attachments/assets/dfb4b61e-a361-44ee-b929-72a294cd7158" />

</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="979" alt="Install VC" src="https://github.com/user-attachments/assets/63550acc-8450-4c49-aacd-391214b25293" />
</p>
<p>

- ph

</p>
<br />

---

## Step 4: Configured MySQL and created database

<p>
<img width="1624" height="979" alt="Install MySQL" src="https://github.com/user-attachments/assets/4586eff9-472a-45ee-9282-d2dc958b0356" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="979" alt="MySQL Config 1" src="https://github.com/user-attachments/assets/e0a72cbb-c233-411b-93f0-df25d18d587c" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="976" alt="MySQL Config 2" src="https://github.com/user-attachments/assets/36d8986f-5fb2-479d-864f-67434b6a3bff" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="985" alt="MySQL Config Finish" src="https://github.com/user-attachments/assets/8c44590e-0391-4968-ad9c-f310f8c0fd2f" />
<p>

- ph

</p>
<br />

---

## Step 5: Deployed and configured the osTicket help desk platform within the IIS web server environment.

<p>
<img width="1624" height="974" alt="IIS Manager" src="https://github.com/user-attachments/assets/e156aa88-b87a-43d0-bf37-7f9f4d95323f" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="974" alt="Add PHP Exec" src="https://github.com/user-attachments/assets/a03f496d-630a-4c42-b2aa-6ebc369c7ef2" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="976" alt="Extract osTicket" src="https://github.com/user-attachments/assets/82161d92-d15b-4238-845b-4232c7ce3680" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="976" alt="osTicket Extracted" src="https://github.com/user-attachments/assets/6789440f-e101-4e6a-a29e-1120dec4f7c0" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="976" alt="Copied Upload" src="https://github.com/user-attachments/assets/3c9ba4e4-1c63-4748-975f-1631b4808fed" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="976" alt="Renamed Upload" src="https://github.com/user-attachments/assets/3edb333a-5c9b-44a1-ac02-45caa3f809d9" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="974" alt="osTicket Site" src="https://github.com/user-attachments/assets/c13593bd-10ac-4adb-9bcc-9990f847496a" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="976" alt="PHP Extensions" src="https://github.com/user-attachments/assets/32016979-b42d-4e69-ac5c-46f48b17185d" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="979" alt="Rename ostsampleconfig" src="https://github.com/user-attachments/assets/6bb1bee3-bb5f-4d4a-b3be-cbdb9ffbc730" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="979" alt="Permissions ostsampleconfig" src="https://github.com/user-attachments/assets/6edbf598-6e56-4ee1-b7c2-60691065ebf5" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="979" alt="osTicket Setup" src="https://github.com/user-attachments/assets/9ff116e6-213c-42f9-80e6-3cb16cbc528c" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="979" alt="Install HeidiSQL" src="https://github.com/user-attachments/assets/1e82d9a8-569b-487b-946f-aadd0bc507ab" />

</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="979" alt="MySql Credentials" src="https://github.com/user-attachments/assets/a109885b-2370-436d-a709-9354c85c1a1f" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="979" alt="Creating osTicket Database" src="https://github.com/user-attachments/assets/4459e969-d2de-499e-a775-09bf758b3320" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="979" alt="osTicket Database" src="https://github.com/user-attachments/assets/30ee25eb-b247-4265-8b2b-17b1fa84ec0b" />
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="979" alt="Setup Finish" src="https://github.com/user-attachments/assets/35531f61-8a5e-4797-85ca-ee356d6b1097" /> 
</p>
<p>

- ph

</p>
<br />

---
<p>
<img width="1624" height="979" alt="Setup Success" src="https://github.com/user-attachments/assets/64c0534b-63b2-46aa-ab69-3f9ac30983f8" />
</p>
<p>

- ph
</p>
<br />

---
