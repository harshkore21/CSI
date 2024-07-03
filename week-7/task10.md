# Create Custom Role in Azure and Assign to Users

Creating custom roles in Azure allows you to define fine-grained access control tailored to your specific needs. This guide will walk you through the steps to create a custom role, assign it to users, and test the assigned role.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Step-by-Step Guide](#step-by-step-guide)
  - [1. Create Custom Role Definition](#1-create-custom-role-definition)
  - [2. Assign Custom Role to Users](#2-assign-custom-role-to-users)
  - [3. Test Assigned Role](#3-test-assigned-role)

## Prerequisites:
- Azure Subscription
- Azure Portal access
- User with appropriate permissions to create custom roles and assign them

## Step-by-Step Guide:

### 1. Create Custom Role Definition

1. **Sign In to Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

2. **Navigate to Azure Active Directory**:
   - In the left-hand menu, select "Azure Active Directory".

3. **Access Roles and Administrators**:
   - Under "Manage", select "Roles and administrators".

4. **Create Custom Role**:
   - Click on "+ Add custom role" at the top of the Roles and administrators blade.

5. **Define Role Details**:
   - **Name**: Enter a name for your custom role.
   - **Description**: Optionally, provide a description for the role.
   - **Actions**: Define the actions (permissions) the role should have. You can specify actions manually or use Azure's built-in actions.
   - **Data Actions**: Optionally, define data actions if applicable.
   - **Not Actions**: Specify actions that should not be allowed for this role.
   - **Assignable Scopes**: Choose the scopes (subscriptions, resource groups) where this role can be assigned.
   - Click "Save" to create the custom role definition.

### 2. Assign Custom Role to Users

1. **Navigate to Roles and Administrators**:
   - In the Azure Active Directory blade, under "Manage", select "Roles and administrators".

2. **Assign Role to User**:
   - Click on "+ Add assignment" next to your custom role in the Roles and administrators blade.

3. **Select Role and User**:
   - **Role**: Select the custom role you created.
   - **Assign access to**: Select "User, group, or service principal".
   - **Select**: Search for and select the user(s) to whom you want to assign the custom role.
   - Click "Save" to assign the custom role.

### 3. Test Assigned Role

1. **Sign In with Assigned User**:
   - Sign out of the Azure Portal and sign back in using the credentials of the user to whom you assigned the custom role.

2. **Access Azure Resources**:
   - Navigate to the Azure resource (e.g., Virtual Machine, Storage Account) that the custom role grants access to.

3. **Verify Permissions**:
   - Attempt to perform actions allowed by the assigned custom role.
   - Ensure that the user can perform the defined actions and does not have access to actions restricted by the custom role.
