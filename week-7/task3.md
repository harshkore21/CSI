# Create Test Users and Groups in Azure Entra ID

Azure Entra ID (Azure Active Directory) allows you to manage users and groups to control access to resources. This guide will walk you through the steps to create test users and groups.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Step-by-Step Guide](#step-by-step-guide)
  - [1. Create Test Users](#1-create-test-users)
  - [2. Create Test Groups](#2-create-test-groups)
  - [3. Assign Users to Groups](#3-assign-users-to-groups)
- [Example Test Scenario](#example-test-scenario)
- [Additional Considerations](#additional-considerations)

## Prerequisites:
- Azure Subscription
- Azure Portal access
- Azure Entra ID (Azure Active Directory) setup

## Step-by-Step Guide:

### 1. Create Test Users

1. **Sign In to Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

2. **Navigate to Azure Active Directory**:
   - In the left-hand menu, select "Azure Active Directory".

3. **Create a New User**:
   - Under "Manage", select "Users".
   - Click on "+ New user" and select "Create new user".
   - Fill in the user information such as Name, User name, and Profile information.
   - Optionally, set the user to "Password" authentication and provide an initial password.
   - Click "Create" to add the new user.

### 2. Create Test Groups

1. **Navigate to Groups**:
   - In the Azure Active Directory blade, under "Manage", select "Groups".

2. **Create a New Group**:
   - Click on "+ New group".
   - Choose the Group type (e.g., Security).
   - Provide a Group name and Group description.
   - Optionally, set Membership type (e.g., Assigned, Dynamic user, Dynamic device).
   - Click "Create" to add the new group.

### 3. Assign Users to Groups

1. **Add Users to a Group**:
   - Navigate to the group you created by selecting "Groups" under "Manage".
   - Select the group name to open the group overview.
   - Click on "Members" under the "Manage" section.
   - Click "+ Add members".
   - Search for the users you created, select them, and click "Select".

## Example Test Scenario:

- **Scenario**: Create a new group named "Test Group" and add three test users to this group.

### Steps:

1. **Create Users**:
   - Create three new users: User1, User2, and User3 following the steps in the "Create Test Users" section.

2. **Create Group**:
   - Create a group named "Test Group" following the steps in the "Create Test Groups" section.

3. **Assign Users to Group**:
   - Add User1, User2, and User3 to "Test Group" following the steps in the "Assign Users to Groups" section.

## Additional Considerations:

- **Group Types**: Understand the different group types (Security, Office 365) and their use cases.
- **Dynamic Membership**: Utilize dynamic membership rules for automatic user assignment to groups based on attributes.
- **Security**: Implement security best practices such as least privilege access and regularly reviewing group memberships.
