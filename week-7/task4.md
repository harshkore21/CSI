# Assign an RBAC Role to a User and Test

Role-Based Access Control (RBAC) in Azure allows you to manage who has access to Azure resources, what they can do with those resources, and what areas they have access to. This guide will walk you through the steps to assign an RBAC role to a user and test the role.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Step-by-Step Guide](#step-by-step-guide)
  - [1. Assign an RBAC Role](#1-assign-an-rbac-role)
  - [2. Test the Assigned Role](#2-test-the-assigned-role)
- [Example Test Scenario](#example-test-scenario)
- [Additional Considerations](#additional-considerations)

## Prerequisites:
- Azure Subscription
- Azure Portal access
- User created in Azure Entra ID

## Step-by-Step Guide:

### 1. Assign an RBAC Role

1. **Sign In to Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

2. **Navigate to the Resource**:
   - Locate the resource to which you want to assign the RBAC role (e.g., a resource group, storage account, virtual machine).

3. **Access the Access Control (IAM) Blade**:
   - Click on the resource to open its management pane.
   - In the left-hand menu, select "Access control (IAM)".

4. **Add Role Assignment**:
   - Click on "+ Add" and select "Add role assignment".
   - In the "Role" dropdown, select the appropriate role (e.g., Reader, Contributor, Owner).
   - In the "Assign access to" dropdown, select "User, group, or service principal".
   - Click on "Select members" and search for the user you want to assign the role to.
   - Select the user and click "Save" to assign the role.

### 2. Test the Assigned Role

1. **Sign In with the User Account**:
   - Sign out of the Azure Portal and sign back in with the user account to which you assigned the RBAC role.

2. **Navigate to the Resource**:
   - Attempt to access the resource you assigned the role to (e.g., a resource group, storage account, virtual machine).

3. **Verify Permissions**:
   - Verify that the user can perform actions permitted by the assigned role. For example:
     - If the user was assigned the "Reader" role, they should be able to view the resource but not make changes.
     - If the user was assigned the "Contributor" role, they should be able to make changes to the resource.

## Example Test Scenario:

- **Scenario**: Assign the "Reader" role to a user for a specific resource group and verify that the user can view the resource group but cannot make changes.

### Steps:

1. **Assign Role**:
   - Assign the "Reader" role to the user for the target resource group following the steps in the "Assign an RBAC Role" section.

2. **Test Role**:
   - Sign in with the user's account and navigate to the resource group.
   - Verify that the user can view the resource group but cannot make changes (e.g., cannot add or delete resources within the group).

## Additional Considerations:

- **Role Scope**: Understand the scope of the RBAC role (e.g., subscription, resource group, resource) and assign roles at the appropriate level.
- **Custom Roles**: If built-in roles do not meet your needs, consider creating custom roles with specific permissions.
- **Audit Logs**: Monitor and review audit logs to track role assignments and access changes.
