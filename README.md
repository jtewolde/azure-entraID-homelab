# Microsoft Entra ID Virtual Homelab

## Overview

This repository documents my hands-on experience learning **Microsoft Entra ID (formerly Azure Active Directory)** by building a cloud identity administration homelab using a **Microsoft Entra ID Free** tenant.

The goal of this project is to develop practical skills used by **IT Help Desk**, **Desktop Support**, and **Junior Systems Administrator** roles by simulating the administration of a small organization's cloud identity environment. Throughout this lab, I configure and manage users, groups, authentication methods, administrative roles, enterprise applications, and automation using Microsoft Graph PowerShell while documenting each stage of the learning process.

Unlike traditional on-premises Active Directory, Microsoft Entra ID is Microsoft's cloud-based Identity and Access Management (IAM) platform. This project focuses on understanding how organizations manage identities, secure access to cloud resources, and automate administrative tasks in Microsoft 365 environments.

---

# Objectives

The primary goals of this homelab are to:

- Learn Microsoft Entra ID administration through hands-on practice.
- Develop experience managing cloud identities and access.
- Understand the differences between on-premises Active Directory and Microsoft Entra ID.
- Simulate common IT support and identity administration tasks.
- Practice automation using Microsoft Graph PowerShell.
- Build a portfolio project that demonstrates cloud administration skills.
- Prepare for future hybrid identity integration with my existing Active Directory homelab.

---

# Lab Environment

| Component             | Details                      |
| --------------------- | ---------------------------- |
| Identity Platform     | Microsoft Entra ID Free      |
| Administration Portal | Microsoft Entra Admin Center |
| Operating System      | Windows 11                   |
| Scripting             | Microsoft Graph PowerShell   |
| Documentation         | GitHub Markdown              |
| Version Control       | Git & GitHub                 |

---

# Lab Architecture

The current environment consists of a cloud-only Microsoft Entra ID tenant used to simulate identity administration within a small business.

```text
                    Microsoft Entra ID Tenant
                              │
      ┌──────────────┬──────────────┬──────────────┐
      │              │              │
    Users          Groups      Administrative Roles
      │
Authentication Methods
      │
Multi-Factor Authentication
      │
Enterprise Applications
      │
Microsoft Graph PowerShell
```

As this project grows, the environment will eventually be expanded into a **Hybrid Identity** lab by synchronizing this tenant with my on-premises Active Directory environment on my previous documented homelab.

---

# Technologies Used

- Microsoft Entra ID Free
- Microsoft Entra Admin Center
- Microsoft Graph PowerShell
- PowerShell 7
- Windows 11
- Microsoft Authenticator
- Git
- GitHub

---

# Skills Practiced

This homelab focuses on developing practical experience in:

- Identity and Access Management (IAM)
- Cloud User Administration
- Security Group Management
- Administrative Role Assignment
- Authentication Methods
- Multi-Factor Authentication (MFA)
- Password Management
- Enterprise Application Management
- Device Registration
- Identity Security
- Microsoft Graph PowerShell
- Identity Automation
- Cloud Administration

---

# Documentation

Each document represents a milestone completed throughout the homelab. Every section includes the objective, implementation process, screenshots, validation, troubleshooting, and lessons learned.

| Document                             | Description                                                                 |
| ------------------------------------ | --------------------------------------------------------------------------- |
| **01 - Tenant Setup**                | Create the Microsoft Entra ID tenant and perform the initial configuration. |
| **02 - User Management**             | Create, modify, disable, restore, and delete cloud user accounts.           |
| **03 - Group Management**            | Configure security groups and manage group membership.                      |
| **04 - Administrative Roles**        | Assign built-in Microsoft Entra administrative roles using least privilege. |
| **05 - Multi-Factor Authentication** | Configure MFA and authentication methods for users.                         |
| **06 - Self-Service Password Reset** | Configure password reset options and recovery methods.                      |
| **07 - Enterprise Applications**     | Add and manage enterprise applications and user assignments.                |
| **08 - Device Registration**         | Register and manage devices within Microsoft Entra ID.                      |
| **09 - Microsoft Graph PowerShell**  | Automate common administrative tasks using PowerShell.                      |
| **10 - Hybrid Identity (Future)**    | Connect this tenant with my Active Directory homelab.                       |

---

# Learning Progress

This repository is maintained as a living project. Each major milestone will be documented below as new concepts are completed.

| Date       | Progress                                                                 |
| ---------- | ------------------------------------------------------------------------ |
| 2025-07-27 | Created Microsoft Entra ID Free tenant and began cloud identity homelab. |
|            | Future progress entries will be added as the project develops.           |

---

# Project Roadmap

## Phase 1 — Cloud Identity Fundamentals

- [ ] Create Microsoft Entra ID tenant
- [ ] Explore Microsoft Entra Admin Center
- [ ] Review tenant properties
- [ ] Configure organization settings

---

## Phase 2 — Identity Administration

- [ ] Create users
- [ ] Manage users
- [ ] Create security groups
- [ ] Assign group memberships
- [ ] Manage administrative roles

---

## Phase 3 — Identity Security

- [ ] Configure authentication methods
- [ ] Enable Multi-Factor Authentication
- [ ] Configure Self-Service Password Reset
- [ ] Review audit logs
- [ ] Explore sign-in logs

---

## Phase 4 — Applications & Devices

- [ ] Add enterprise applications
- [ ] Assign users and groups
- [ ] Register devices
- [ ] Explore device management

---

## Phase 5 — Automation

- [ ] Install Microsoft Graph PowerShell
- [ ] Connect to Microsoft Entra ID
- [ ] Create users with PowerShell
- [ ] Create groups with PowerShell
- [ ] Automate common administrative tasks

---

## Phase 6 — Hybrid Identity

- [ ] Connect on-premises Active Directory
- [ ] Configure Microsoft Entra Connect
- [ ] Synchronize users
- [ ] Synchronize groups
- [ ] Test password synchronization
- [ ] Document hybrid identity administration

---

# Active Directory vs. Microsoft Entra ID

One objective of this project is understanding how Microsoft's cloud identity platform differs from traditional on-premises Active Directory.

| Active Directory           | Microsoft Entra ID                                  |
| -------------------------- | --------------------------------------------------- |
| On-premises directory      | Cloud identity platform                             |
| Domain Controllers         | Microsoft-managed cloud service                     |
| Organizational Units (OUs) | Administrative Units                                |
| Group Policy Objects       | Conditional Access & Cloud Policies                 |
| Kerberos Authentication    | Modern Authentication (OAuth, OpenID Connect, SAML) |
| Domain Join                | Microsoft Entra Join                                |

Understanding both technologies is essential because many organizations operate hybrid environments that combine on-premises Active Directory with Microsoft Entra ID.

---

# Future Improvements

Planned enhancements include:

- Microsoft Intune
- Microsoft 365 Administration
- Conditional Access Policies
- Administrative Units
- Dynamic Groups
- Identity Governance
- Privileged Identity Management (PIM)
- Hybrid Identity Synchronization
- Automated User Provisioning
- Identity Lifecycle Management

---

# Related Project

This repository complements my **Active Directory Virtual Homelab**, where I built and administered a traditional Windows Server domain environment using:

- Windows Server 2022
- Active Directory Domain Services
- DNS
- DHCP
- Group Policy
- File Sharing
- Remote Desktop Services
- PowerShell

Together, these projects demonstrate experience administering both modern cloud identities and traditional on-premises directory services, providing a foundation for understanding hybrid enterprise environments.

---

# Disclaimer

This homelab is intended for educational purposes only. All users, groups, devices, and organizational information used throughout this project are fictitious and created solely for learning and demonstration purposes.
