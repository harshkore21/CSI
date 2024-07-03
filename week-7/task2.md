# Observe or Create Azure Entra ID

Azure Entra ID (Azure Active Directory) is Microsoft’s cloud-based identity and access management service. It helps your employees sign in and access resources in external resources like Microsoft 365, the Azure portal, and thousands of other SaaS applications.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Step-by-Step Guide](#step-by-step-guide)
  - [1. Observe Azure Entra ID](#1-observe-azure-entra-id)
  - [2. Create Azure Entra ID](#2-create-azure-entra-id)
- [Example Test Scenario](#example-test-scenario)
- [Additional Considerations](#additional-considerations)

## Prerequisites:
- Azure Subscription
- Azure Portal access

## Step-by-Step Guide:

### 1. Observe Azure Entra ID

1. **Sign In to Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

2. **Access Azure Entra ID**:
   - In the left-hand menu, select "Azure Active Directory".
   - This page will display an overview of your Azure Entra ID, including tenant information, users, groups, and applications.

3. **View Tenant Information**:
   - Under the "Overview" section, you can view details about your tenant, such as Tenant ID, primary domain, and licensing information.

4. **Manage Users and Groups**:
   - Navigate to the "Users" and "Groups" sections to view and manage the users and groups within your Azure Entra ID.
   - You can add, remove, and modify users and groups as needed.

### 2. Create Azure Entra ID

1. **Navigate to Azure Active Directory**:
   - In the left-hand menu, select "Azure Active Directory".

2. **Create a New Directory**:
   - At the bottom of the Azure Active Directory blade, select "Create a directory".
   - Follow the prompts to create a new Azure Entra ID tenant.
   - Provide necessary information such as the organization name, initial domain name, and country/region.

3. **Switch to the New Directory**:
   - After creating the new directory, you can switch to it by selecting your account name in the top-right corner of the Azure Portal and selecting "Switch directory".
   - Choose the newly created directory from the list.

4. **Configure the New Azure Entra ID**:
   - Configure the new Azure Entra ID by adding users, groups, and applications as needed.
   - Set up additional configurations such as custom domains, branding, and security settings.

## Example Test Scenario:

- **Scenario**: Create a new Azure Entra ID tenant for a test environment, add a user to this directory, and configure basic settings.

### Steps:

1. **Create New Directory**:
   - Follow the steps in the "Create Azure Entra ID" section to create a new directory.

2. **Add a User**:
   - In the new directory, navigate to "Users".
   - Click on "New user" and fill in the necessary details to add a new user.

3. **Configure Settings**:
   - Configure basic settings such as password reset policies, MFA (Multi-Factor Authentication), and group assignments for the new user.

## Additional Considerations:

- **Security**: Implement security best practices such as enabling MFA, conditional access policies, and monitoring sign-in activity.
- **Licensing**: Ensure you have the appropriate licenses for the features you intend to use within Azure Entra ID.
- **Integration**: Integrate Azure Entra ID with other Azure services and third-party applications for a unified identity management solution.
