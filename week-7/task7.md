# Observe or Create Azure Entra ID in Personal Azure Account

Azure Entra ID (formerly Azure Active Directory) is a cloud-based identity and access management service. This guide will walk you through the steps to observe an existing Azure Entra ID or create your own in a personal Azure account.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Step-by-Step Guide](#step-by-step-guide)
  - [1. Observe Existing Azure Entra ID](#1-observe-existing-azure-entra-id)
  - [2. Create a New Azure Entra ID](#2-create-a-new-azure-entra-id)

## Prerequisites:
- Azure Subscription
- Azure Portal access

## Step-by-Step Guide:

### 1. Observe Existing Azure Entra ID

1. **Sign In to Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

2. **Navigate to Azure Active Directory**:
   - In the left-hand menu, select "Azure Active Directory".

3. **View Directory Information**:
   - Once in the Azure Active Directory blade, you can view various details about your directory, such as users, groups, applications, and more.
   - To see the list of users, click on "Users" under the "Manage" section.
   - To see the list of groups, click on "Groups" under the "Manage" section.
   - To see the list of registered applications, click on "App registrations".

### 2. Create a New Azure Entra ID

1. **Sign In to Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

2. **Navigate to Azure Active Directory**:
   - In the left-hand menu, select "Azure Active Directory".

3. **Create a New Directory**:
   - Click on "Manage tenants" at the top of the Azure Active Directory blade.
   - Click on "+ Create" to create a new directory.

4. **Configure Directory Settings**:
   - Fill in the necessary details for your new directory:
     - Organization name: Enter a name for your new directory.
     - Initial domain name: Enter a unique domain name for your new directory.
     - Country or region: Select your country or region.
   - Click on "Create" to create your new directory.

5. **Switch to the New Directory**:
   - After the directory is created, you will be notified. Click on your account name at the top-right corner of the Azure Portal.
   - Click on "Switch directory" and select the newly created directory.
