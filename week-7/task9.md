# Assign RBAC Role to User and Test

Assigning RBAC roles to users in Azure Entra ID allows you to control access to Azure resources. This guide will walk you through the steps to assign an RBAC role to a user and test the assigned role.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Step-by-Step Guide](#step-by-step-guide)
  - [1. Assign RBAC Role](#1-assign-rbac-role)
  - [2. Test Assigned Role](#2-test-assigned-role)

## Prerequisites:
- Azure Subscription
- Azure Portal access
- User with appropriate permissions to assign roles

## Step-by-Step Guide:

### 1. Assign RBAC Role

1. **Sign In to Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

2. **Navigate to Azure Active Directory**:
   - In the left-hand menu, select "Azure Active Directory".

3. **Access Roles and Administrators**:
   - Under "Manage", select "Roles and administrators".

4. **Assign Role to User**:
   - Click on "+ Add assignment" at the top of the Roles and administrators blade.

5. **Select Role and User**:
   - **Role**: Select the RBAC role you want to assign (e.g., Contributor, Reader).
   - **Assign access to**: Select "User, group, or service principal".
   - **Select**: Search for and select the user to whom you want to assign the role.
   - Click "Save" to assign the role.

### 2. Test Assigned Role

1. **Sign In with Assigned User**:
   - Sign out of the Azure Portal and sign back in using the credentials of the user to whom you assigned the RBAC role.

2. **Access Azure Resources**:
   - Navigate to the Azure resource (e.g., Virtual Machine, Storage Account) that the role grants access to.

3. **Verify Permissions**:
   - Attempt to perform actions allowed by the assigned RBAC role.
   - For example, if the role is Contributor, try creating or modifying resources. If it is Reader, attempt to view resources without the ability to modify them.
