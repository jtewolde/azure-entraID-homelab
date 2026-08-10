# 02- User Management

## Overview

User management is one of the most fundamental responsibilities of an Identity and Access Administrator. In an enterprise environment, IT administrators regularly create accounts for new employees, update user information, assign access, disable accounts when employees leave the organization, and troubleshoot authentication issues.

In this section of the Microsoft Entra ID homelab, I practiced managing cloud user accounts using the **Microsoft Entra Admin Center**.

The lab was based on Microsoft's official [Perform Basic User Management Tasks](https://microsoftlearning.github.io/Get-started-Microsoft-Entra-Management-Tasks/Instructions/Labs/01-perform-basic-user-management.html) exercise and adapted for this homelab environment. Instead of using the example users provided by Microsoft, I created fictional users to simulate a small organization.

---

## Objectives

The objectives of this lab are to:

- Understand how cloud identities are created in Microsoft Entra ID.
- Create and configure internal user accounts.
- Understand the difference between Member and Guest user types.
- Verify that newly created users can authenticate.
- Practice managing user properties.
- Explore user licensing.
- Understand external/B2B users.
- Assign administrative roles using least-privilege principles.
- Understand Active versus Eligible role assignments.
- Create multiple users using a CSV file.
- Practice identity administration tasks that are relevant to IT Support and System Administration roles.

---

## Step 1a: Create a New User

The first step was to create a new cloud user to represent an employee within the organization in **Microsoft Entra ID**.

1. Navigate to **Microsoft Entra Admin Center → Identity → Users → All users**.
2. Select **+ New User** > **Create New User**.
3. On the **Basics** section, fill out the neccessary info like **User Principal Name**, **Display Name**, etc.
    - Make sure that the "Account Enabled" checkbox is enabled.
    - By default, the account will be assigned a generated password. Either copy the password onto your **Notepad** app or manually create a password to sign back in with.

![BasicsUser](/images/UserBasics.png)

4. Move onto the **Properties** section where you can enter more information about the user like:
    - Full Name
    - Job Title
    - Job Department
    - Contact Info

![PropertiesUser](/images/UserProperties.png)

5. Skip the **Assignments** section as we will assign the user to a group later in the lab.
6. Review all of the information that you put down for the user and create the user.

![NewUser](/images/NewUser.png)

---

## Step 1b: Verify User Sign-In

After creating the account, I verified that the newly created user can sign into **Microsoft Entra Admin Center**.

1. Open an Incognito browsing window.
2. Connect to the [Microsoft Entra Admin Center](https://admin.microsoft.com/) to sign in.
3. You will be asked to provide an email and password for the user you created.
    - **Email:** PrincipalName@TenantName.onmicrosoft.com (e.g. Franklin@JoTewolde20gmail.onmicrosoft.com)
    - **Password:** Auto generated password you saved on Notepad.
4. If prompted, update the user's password.
5. Afterwards, you will be asked to follow instructions to set up **MFA** by downloading **Microsoft Authenticator** on your cellular device, create an account on there, scan an **QR Code** to link the account to the user, then type in the number that is displayed on the Authenticator app to the input on the screen.
    - **MFA(Multi-Factor Authentication)** is a security process in **Entra ID** to require users to provide two or more different pieces of proof to login and gain access to an account or app.

![MFA_Success](/images/UserAuthenticatorSuccess.png)

6. After setting up MFA correctly, you will be navigated to the **Entra Admin Center** under the user you created earlier. 
![MFADashboard](/images/NewUserDashboard.png)

7. Explore the admin center under the user and close the private window to do the next step.

---

