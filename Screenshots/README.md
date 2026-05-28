# Hybrid-On-Prem-Azure-Work
# Active Directory Domain Controller with GPO and Azure AD Sync Project
## Project Overview
 This Project demonstrates the deployment of a Windows Server Active Directory environment including:
 Configuration of a Domain Controller
 Joining a client machine to the domain
Implementation of Group Policy Objects (GPOs)
Integration with Microsoft Entra ID (Azure Active Directory) using Azure Ad Connect

This simulates a real-world hybrid identity infrastructure used in entraprise environments.
### Technologies Used

Windows Server 2022 (Domain Controller)

Windows 10 Pro Client Machine

Active Directory Domain Services (AD DS)

DNS Server Role

Group Policy Management (GPO)

Microsoft Entra ID (Azure AD)

Azure AD Connect

### Archirecture Overview
-------------------
Windows Server (Domain Controller)
        │
        ├── DNS Server
        ├── Active Directory Domain
        ├── Group Policies
        │
        └── Client Machine (Domain Joined)

        │
        ▼
Azure Cloud
-------------------
Microsoft Entra ID (Azure AD)
Azure AD Connect Syn

## Step-by-Step Deployment Guide

### Step1: Setup Domain Controller

 Install Windows Server 2022
 
 Set Static IP address
 
 Install role: 
 
    : Active Directory Domain Services (AD DS)
    
 Promote server to DOmain Controller
 
    : Create new forest (fatimazahrauzmasami.pk)
    
 Install and configure DNS Server
 
### Step2: Create Active Directory Structure

 Open Active Directory Users and Computers (ADUC)
 
 Create:
 
   : Organization Unite (OUs)
   
   : Users
   
   : Computers
   
   : Groups
   
 Create test user accounts
 
### Step3: Configure Client Machine

 Install Windows 10 Pro
 
 Set DNS to Domain Controller IP
 
 Join system to domain:
 
   : System Properties --> Computer Name --> Domain
   
 Restart Machine
 
 Login using Domain Credentials
 
### Step 4: Configure Group Policies (GPOs)

 Open Group Policy Management Concole
 
 Create new GPO 
 
 Link to OU
 
 Configure policies such as:
 
   : Password policy
   
   : Account lockout policy
   
   : Disable Control Panel
   
   : Desktop restrictions

 Apply Policy:
 
    gpupdate /force
    
### Step 5: Azure AD Integration

 Install Azure AD Connect
 
 Sign in with Azure admin account
 
 Select: 
 
     : Password Hash Synchronization
     
 Connect:
 
     : On-prem Active Directory --> Azure AD
     
 Start synchronization
 
Verify in Microsoft Entra Admin Center

### Step 6: Verify Sync

   : Check users appear in Azure AD
   
   : Confirm sync status is "Healthy"

   :Enable MFA
   
# Author
# Uzma Shabbir

