Active Directory Domain Services (AD DS) – Departmental Access Control Lab

Project Overview

This project demonstrates the deployment and administration of a Windows Server 2016 Active Directory environment with a Windows 11 domain client.

The objective was to create a small business network where employees from different departments could access only the shared resources assigned to their departments.

The lab demonstrates practical experience with Active Directory, user and group management, Group Policy, SMB file sharing, NTFS permissions, and access-control testing.

Lab Environment

Component

Configuration

Domain Controller

Windows Server 2016

Client Machine

Windows 11

Domain Name

zamani.local

Server Name

AD-DC01

Domain Controller IP

192.168.0.4

Shared Folder

ZAMANI-SHARED

Virtualisation

VirtualBox and VMware Workstation

Departments

The Active Directory environment contains four departments:

IT Department

Financial Department

HR Department

Security Department

Each department has its own user accounts and security group.

Security Groups and Access Control

Departmental security groups were used to manage access to shared resources.

Department

Security Group

Shared Folder

IT

IT Administrator

IT

Finance

Finance-Team

Finance

HR

HR-Team

HR

Security

Security-Team

Security

Group Policy Configuration

A domain password policy named ZAMANI-Domain-Password-Policy was configured.

The policy included:

Minimum password length: 10 characters

Password complexity: Enabled

Password history: 5 passwords

Maximum password age: 90 days

Minimum password age: 1 day

Account lockout threshold: 5 attempts

Account lockout duration: 15 minutes

Reset account lockout counter: 15 minutes

The policy was applied and verified on the Windows 11 domain client.

File Sharing and NTFS Permissions

A shared folder named ZAMANI-SHARED was created on the Domain Controller.

Four departmental folders were created:

C:\ZAMANI-SHARED
│
├── IT
├── Finance
├── HR
└── Security

SMB sharing was enabled to allow network access from the Windows 11 client.

NTFS permissions were configured so that each departmental security group could access its corresponding folder.

Broad permissions that allowed unintended departmental access were reviewed and corrected.

Access Control Testing

The configuration was tested using employee accounts from the different departments.

Test Account

Department

Own Department Folder

Other Department Folders

Henry Babel

IT

Allowed

Denied

Pretty Ability

Finance

Allowed

Denied

HR Employee

HR

Allowed

Denied

Security Employee

Security

Allowed

Denied

All four departmental access tests were successful.

Skills Demonstrated

Windows Server 2016 administration

Active Directory Domain Services

Domain Controller deployment

Active Directory user management

Security group management

Group Policy configuration

Password and account lockout policies

SMB network file sharing

NTFS permissions

Role-Based Access Control (RBAC)

Windows 11 domain joining

Access-control testing and troubleshooting

Project Outcome

Successfully deployed a functional Active Directory domain environment with four departments and tested departmental access restrictions.

This project provided practical experience in Windows domain administration, identity and access management, and enterprise security fundamentals.

Project Evidence

The following folders contain screenshots documenting the lab configuration and testing.

1. Active Directory Setup

View Active Directory Setup Screenshots

2. Group Policy Configuration

View Group Policy Screenshots

3. Departmental Access Control

View Access Control Screenshots

Disclaimer

This project was completed in a controlled virtual lab environment for educational and cybersecurity training purposes.

## Project Evidence

The following folders contain screenshots documenting the lab configuration and testing.

### 1. Active Directory Setup

[View Active Directory Setup Screenshots](project-evidence/setup/)

### 2. Group Policy Configuration

[View Group Policy Screenshots](project-evidence/group-policy/)

### 3. Departmental Access Control

[View Access Control Screenshots](project-evidence/access-control/)
