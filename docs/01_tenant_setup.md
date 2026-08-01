# 01 - Microsoft Entra ID Tenant Setup

## Overview

The purpose of this document is to establish the Microsoft Entra ID environment that will be used throughout this homelab. A dedicated **Microsoft Entra ID Free** tenant was created to simulate a cloud-based identity infrastructure similar to what is commonly used in enterprise environments.

This tenant serves as the foundation for future labs involving cloud user administration, security groups, authentication methods, Microsoft Graph PowerShell, enterprise applications, and eventually hybrid identity integration with my existing Active Directory homelab.

---

## Objectives

By completing this section of the lab, I will:

- Create a dedicated Microsoft Entra ID tenant.
- Become familiar with the Microsoft Entra Admin Center.
- Review the tenant's configuration and properties.
- Verify administrative access.
- Understand how Microsoft Entra ID differs from traditional Active Directory.
- Prepare the environment for future identity management tasks.

---

## Lab Environment

| Component         | Details                      |
| ----------------- | ---------------------------- |
| Identity Platform | Microsoft Entra ID Free      |
| Management Portal | Microsoft Entra Admin Center |
| Client Device     | Windows 11                   |
| Browser           | Google Chrome                |
| Documentation     | GitHub Markdown              |

---

## What is Microsoft Entra ID?

**Microsoft Entra ID** is Microsoft's cloud-based Identity and Access Management (IAM) platform. It allows organizations to securely manage users, groups, applications, devices, and authentication without requirng on-premises domain controllers.

Unlike traditional **Active Directory**, Microsoft Entra ID is hosted entirely in Microsoft's cloud and is designed to provie secure authentication for Microsoft 365 services, enterprise applications, and cloud resources.

Common administrative responsibilities include:

- Managing users
- Managing security groups
- Assigning administrative roles
- Configuring authentication methods
- Enabling Multi-Factor Authentication (MFA)
- Managing enterprise application access
- Monitoring sign-in activity
- Automating identity management using Microsoft Graph PowerShell

---

## Creating the Microsoft Entra ID Tenant

The first step in building this homelab was creating a dedicated Microsoft Entra ID Free tenant. Using a separate tenant provides an isolated environment for experimenting with cloud identity management without affecting any personal or production Microsoft accounts.

I created a new **Microsoft Entra ID Free Tenant** through the Microsoft Entra portal by:

1. Signing in with a Microsoft account and enter the Azure Portal.
2. Selecting **Microsoft Entra ID** under **Azure Services** or using the navigation bar.
3. Selecting the **Manage Tenants** tab in the overview.
4. Clicking on the **Create** tab on the **Manage Tenants** page.
5. Picked the recommended **Governance Workface** configuration for the tenant.
6. Providing the organization name, initial `.onmicrosoft.com` domain, and country/region.
7. Completing the tenant creation process and signed into the **Entra Admin Center**.

The following GIF demonstrates the tenant creation process used to set up this lab.

![AzureTenantSetup](/images/AzureTenant.gif)

---

## Exploring the Microsoft Entra Admin Center

After signing into the tenant, I explored the Microsoft Entra Admin Center to become familiar with the available management tools.

Key sections reviewed included:

- Overview
- Users
- Groups
- Administrative Roles
- Enterprise Applications
- Devices
- Identity
- Monitoring & Health

Understanding the portal layout will make future administrative tasks easier as the lab expands.

![AdminCenter](/images/EntraAdminCenter.png)

---

## Reviewing Tenant Properties

After the tenant was created, I reviewed the tenant's configuration to verify that the environment was created successfully.

Information reviewed included:

- Organization Name
- Primary Domain
- Tenant ID
- Licensing Information

These properties uniquely identify the tenant and are commonly referenced when configuring integrations, automation, and hybrid identity.

![TenantProperties](/images/TenantProperties.png)

---

## Verifying Adminstrative Access

The Global Administrator account created during tenant setup was verified by accessing administrative features throughout the Microsoft Entra portal.

In order to successfully verify adminstrative access, do the following:

1. Open the **Users** section of the Admin Center by clicking on the tab on the sidebar.
2. Currently, there should only be one user from the tenant creation. Click on the user's name to access its properties.
3. Select the **Assigned Roles** option to see what roles the user is assigned.
4. You should see the the role, **Global Adminstrator** is assigned to this user.

This confirms that the administrator account has the required permissions for future lab exercises.

![AdminstrativeRole](/images/TenantAdminstrativeRole.gif)

---

## Understanding The Difference from Active Directory

One objective of this project is understanding how Microsoft Entra ID differs from traditional Active Directory.

| **Active Directory**            | **Microsoft Entra ID**                              |
| ------------------------------- | --------------------------------------------------- |
| On-premises directory service   | Cloud identity platform                             |
| Requires Domain Controllers     | Microsoft-hosted service                            |
| Uses Organizational Units (OUs) | Uses Administrative Units                           |
| Group Policy                    | Cloud-based identity policies                       |
| Kerberos Authentication         | Modern Authentication (OAuth, OpenID Connect, SAML) |

Although both platforms manage identities, Microsoft Entra ID focuses on providing secure authentication and authorization for cloud services rather than managing traditional Windows domains.

---

## Verification

The following checks were completed to verify the tenant was successfully configured.

- ✅ Successfully created a Microsoft Entra ID tenant.
- ✅ Signed into the Microsoft Entra Admin Center.
- ✅ Verified administrator access.
- ✅ Reviewed tenant properties.
- ✅ Confirmed access to user, group, and role management sections.
- ✅ Verified the tenant is ready for future configuration.

---

## Lessons Learned

Creating a Microsoft Entra ID tenant introduced the core concepts of Microsoft's cloud identity platform. Unlike Active Directory, which relies on on-premises infrastructure, Microsoft Entra ID provides identity management as a cloud service with centralized administration through a web-based portal.

Understanding the tenant structure and administrative interface establishes the foundation for future labs involving user management, security, application access, and automation.

---

## Next Steps

The next stage of this homelab focuses on creating and managing cloud user accounts.

Topics covered in the next document include:

- Creating users
- Modifying user properties
- Resetting passwords
- Disabling user accounts
- Restoring deleted users
- Managing user licenses (where applicable)
- Creating joined-hybrid environment between on-premises Active Directory and Entra ID
