# Create Test Users and Groups in Azure Entra ID

Creating test users and groups in Azure Entra ID helps manage and organize access to resources efficiently. This guide will walk you through the steps to create test users and groups in Azure Entra ID.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Step-by-Step Guide](#step-by-step-guide)
  - [1. Create Test Users](#1-create-test-users)
  - [2. Create Test Groups](#2-create-test-groups)
  - [3. Add Users to Groups](#3-add-users-to-groups)

## Prerequisites:
- Azure Subscription
- Azure Portal access

## Step-by-Step Guide:

### 1. Create Test Users

1. **Sign In to Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

2. **Navigate to Azure Active Directory**:
   - In the left-hand menu, select "Azure Active Directory".

3. **Access the Users Section**:
   - Under the "Manage" section, click on "Users".

4. **Create a New User**:
   - Click on "+ New user" at the top of the Users blade.
   - Select "Create user".

5. **Fill in User Details**:
   - **User name**: Enter a unique user name (e.g., `testuser1`).
   - **Name**: Enter the user's first and last name.
   - **Password**: Choose to let the user create their own password or create one for them.
   - **Groups and roles**: Optionally, assign groups and roles during creation.
   - **Job info**: Optionally, add job title and department information.
   - Click "Create" to create the user.

6. **Repeat for Additional Users**:
   - Repeat the steps above to create additional test users as needed (e.g., `testuser2`, `testuser3`).

### 2. Create Test Groups

1. **Navigate to Groups Section**:
   - In the Azure Active Directory blade, under the "Manage" section, click on "Groups".

2. **Create a New Group**:
   - Click on "+ New group" at the top of the Groups blade.

3. **Fill in Group Details**:
   - **Group type**: Select "Security".
   - **Group name**: Enter a name for the group (e.g., `TestGroup1`).
   - **Group description**: Optionally, add a description for the group.
   - **Membership type**: Select "Assigned" for manual user addition.
   - Click "Create" to create the group.

4. **Repeat for Additional Groups**:
   - Repeat the steps above to create additional test groups as needed (e.g., `TestGroup2`, `TestGroup3`).

### 3. Add Users to Groups

1. **Navigate to Groups Section**:
   - In the Azure Active Directory blade, under the "Manage" section, click on "Groups".

2. **Select a Group**:
   - Click on the group name to which you want to add users (e.g., `TestGroup1`).

3. **Add Members**:
   - In the group blade, click on "Members" under the "Manage" section.
   - Click on "+ Add members".
   - Search for the test users you created (e.g., `testuser1`, `testuser2`).
   - Select the users and click "Select" to add them to the group.

4. **Repeat for Additional Groups**:
   - Repeat the steps above to add users to the other test groups as needed.
