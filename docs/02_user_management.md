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

## Step 1A: Create a New User

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

## Step 1B: Verify User Sign-In

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

## Step 1C: License Assignment

The Microsoft Learn exercise includes assigning a license to the practice user. However, completing this portion of the exercise requires **Microsoft Entra ID Premium** licensing, which is not included with my Microsoft Entra ID Free tenant.

Because I am using the Free tier for this homelab, I was unable to complete the license assignment myself.

Follow the steps below if you have **Entra ID Premium** taken directly from [Perform Basic User Management Tasks](https://microsoftlearning.github.io/Get-started-Microsoft-Entra-Management-Tasks/Instructions/Labs/01-perform-basic-user-management.html) lab from **Microsoft Leanring Exercise**.

![AddLicense](/images/AddLicenseStep.png)

---

## Step 2: External User Management

**Microsoft Entra ID** supports collaboration with users outside of an organization through Microsoft Entra B2B collaboration.

An external user can be invited to access resources within an organization's tenant without creating a traditional internal employee account.

This is useful for scenarios such as:
- Contractors
- Consultants
- Business partners
- Vendors
- External project members

1. Connect to the [Microsoft Entra Admin Center](https://admin.microsoft.com/) to sign in.
2. From the menu on the left, open the **Entra ID** option and navigate to **Identity → Users → All users**.
3. Select **+ New User** > **Invite External User**.

![AddExternalUser](/images/AddExternalUser.gif)

4. Enter the information under the **Basics** tab for your external user:
  - **Email**: ExtUser@example.com
  - **Display Name**: External User
  - **Invitation Message**: "Thank you for joining the company for this short work project. We look forward to building this project together."
5. Additionally, you can enter information under **Properties** and **Assignments** similar to the previous step of creating a new user to the organziation.
6. Select the blue **Review + Create** button to review the information you entered.
7. Select **Invite** to send the invite to the external user.

![AddExternalUser1](/images/AddExternalUser1.gif)

To verify that the external user got the invite, try to use an email that you have access to for checking that the invite arrived in the user's inbox.

![ExternalEmail](/images/ExternalEmail.png)

---

## Step 3: Assign a Role to a User

**Microsoft Entra ID** uses role-based access control (RBAC) to provide users with roles that have specific permissions and actions in the organization.

1. Connect to the [Microsoft Entra Admin Center](https://admin.microsoft.com/) to sign in.
2. From the menu on the left, open the **Entra ID** option and navigate to **Identity → Users → All users**.
3. Choose a user that you created earlier and click on the hyperlinked name.
4. Select the **Assigned Roles** option in the newly opened menu.
5. The created user shouldn't have any assigned roles. At the top of the screen select **"+ Add Assignment"**.
6. From the **Select role** dropdown menu, chose the role that you want the user to have(e.g. Application Adminstrator).
7. Click the blue **"Add"** button to confirm adding the role to the user.
8. Refresh the page to see if the role has been successfully assigned to the selected user.

![AssignedRole](/images/AssignedRoles.gif)