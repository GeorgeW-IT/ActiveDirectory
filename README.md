# Active Directory on Azure

## Project Overview

I deployed and configured a Windows Server Active Directory environment on Azure to practice enterprise identity and access management. This lab simulates a small business network with organizational structure, user management, security groups, and Group Policy enforcement.

## Technologies Used
- Azure Virtual Machines
- Windows Server
- Active Directory Domain Services (AD DS)
- PowerShell

## Lab Setup

Here's how I built the lab:

1. Deployed an Azure Virtual Machine with Windows Server
2. Installed Active Directory Domain Services
3. Configured domain users and groups
4. Created and applied Group Policy Objects (GPOs)
5. Verified domain functionality and connectivity

## Screenshots

All screenshots are stored in the [AD_Screenshots](AD_Screenshots) folder.

### Users

This screenshot shows the user accounts I created in Active Directory. I placed them in a dedicated Users Organizational Unit (OU) to keep things organized.

![AD Users](AD_Screenshots/AD_Users.png)

There are multiple ways to create users in Active Directory. You can create a new user directly in the OU when you need a completely fresh profile. Another method is copying an existing user from the same department, which lets the new user inherit settings like group memberships so they get the right permissions automatically. You can also use PowerShell for automation and bulk user creation in larger environments.

![Create a User](AD_Screenshots/copy_user.png)

This screenshot shows the Active Directory search function, which you can use to quickly find user accounts, computers, groups, and other objects. While I only have a few users in this lab, this tool would be essential in larger environments with hundreds or thousands of objects.

![Find an existing user](AD_Screenshots/Find_Users.png)

This screenshot shows how to reset a user's password in Active Directory - a common helpdesk task.

![Reset a Users Password](AD_Screenshots/password_reset.png)

### Groups

I created custom security groups and organized them in the Groups OU for role-based access management.

![AD Groups](AD_Screenshots/User_Roles.png)

### Group Policies

For this first GPO, I created a password policy where users must follow certain requirements for their passwords.

![AD GPO](AD_Screenshots/Group_Policy_Password.png)

In this next one, I created an account lockout policy that limits the number of password attempts users can make.

![AD_GPO](AD_Screenshots/Group_Account_Lockout_Policy.png)

This Group Policy sets a screen timeout for users who leave their screens on too long without activity.

![AD_GPO](AD_Screenshots/Screen_Timeout_Policy.png)

### Auditing

I set up audit settings to track what happens in the system.

This first screenshot shows me creating a test user for the audit.

![AD_Auditing](AD_Screenshots/Audit_user_created.png)

This second one shows me deleting that same user.

![AD_Auditing](AD_Screenshots/Audit_user_deleted.png)

This screenshot shows the audit page confirming the user account was "enabled".

![AD_Auditing](AD_Screenshots/Audit_of_user_created.png)

And this one shows where the user account was "deleted".

![AD_Auditing](AD_Screenshots/Audit_of_user_deleted.png)

I enabled auditing through GPO to track logon events and account management. The Event Viewer logs show successful auditing of the test user creation and deletion.

![AD_Auditing](AD_Screenshots/Audit_Settings.png)

### Domain Structure

This shows the Active Directory domain structure with the OU hierarchy and user organization.

![AD Domain](AD_Screenshots/domain_structure.png)

## Skills Demonstrated

### Technical Skills
- Active Directory Domain Services deployment and configuration
- Azure Virtual Machine setup and management
- Organizational Unit design and implementation
- User account management (creation, modification, password resets)
- Security group creation and role-based access control
- Group Policy Object configuration and enforcement
- Password policy implementation
- Active Directory search and navigation
- Windows Server administration

### Concepts Applied
- Principle of least privilege through security groups
- Role-based access control for managing permissions
- Hierarchical organizational structure using OUs
- Group-based policy enforcement
- Identity and access management best practices
