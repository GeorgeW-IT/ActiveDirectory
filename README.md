# Active Directory on Azure

## Overview
This project demonstrates an Active Directory lab setup on Azure. It includes configuring domain services, creating users and groups, and applying Group Policy Objects (GPOs) to simulate a small network environment.

## Technologies Used
- Azure Virtual Machines
- Windows Server
- Active Directory Domain Services (AD DS)
- PowerShell (basic scripts)

## Lab Setup
Steps to build the lab:
1. Deployed an Azure Virtual Machine with Windows Server.
2. Installed Active Directory Domain Services.
3. Configured domain users and groups.
4. Created and applied Group Policy Objects (GPOs).
5. Verified domain functionality and connectivity.

## Screenshots
All screenshots are stored in the `AD_Screenshots` folder.

### Users
![AD Users](AD_Screenshots/AD_Users.png)
[Create a User](AD_Screenshots/copy_users.png)

### Groups
![AD Groups](AD_Screenshots/User_Roles.png)

### Group Policies
In this first GPO i created a password policy where users must follow a certain set of requirements for thier password
![AD GPO](AD_Screenshots/Group_Policy_Password.png)

### Domain Structure
![AD Domain](AD_Screenshots/)

## Scripts (Optional)
Any scripts used to automate setup can be found in the `Scripts` folder. Example:
- `Create_AD_Users.ps1` – PowerShell script to create domain users

## Lessons Learned / Notes
- Gained practical experience with Active Directory domain setup on Azure.
- Learned to configure users, groups, and GPOs effectively.
- Improved understanding of basic networking and system administration.

## Project Links
- GitHub Repository: [Link to repo]
