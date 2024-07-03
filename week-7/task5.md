# Create a Custom Role and Assign to Users

Creating custom roles in Azure allows you to tailor permissions to your specific needs. This guide will walk you through the steps to create a custom RBAC role, assign it to users, and test the assigned role.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Step-by-Step Guide](#step-by-step-guide)
  - [1. Create a Custom Role](#1-create-a-custom-role)
  - [2. Assign the Custom Role to Users](#2-assign-the-custom-role-to-users)
  - [3. Test the Assigned Role](#3-test-the-assigned-role)
- [Example Test Scenario](#example-test-scenario)
- [Additional Considerations](#additional-considerations)

## Prerequisites:
- Azure Subscription
- Azure Portal access
- Azure CLI installed on your local machine (optional but recommended)

## Step-by-Step Guide:

### 1. Create a Custom Role

1. **Sign In to Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

2. **Navigate to Azure Active Directory**:
   - In the left-hand menu, select "Azure Active Directory".

3. **Access Roles and Administrators**:
   - Under "Manage", select "Roles and administrators".

4. **Create a Custom Role**:
   - Click on "+ New custom role".
   - Provide a name and description for the custom role.
   - Define the permissions by adding "Actions" and "DataActions". You can find specific permissions needed by searching for built-in roles and copying their permissions.
   - Example JSON for custom role definition:
     ```json
     {
       "Name": "Custom Role Name",
       "IsCustom": true,
       "Description": "Description of custom role",
       "Actions": [
         "Microsoft.Compute/virtualMachines/read",
         "Microsoft.Storage/storageAccounts/listKeys/action"
       ],
       "DataActions": [],
       "NotActions": [],
       "NotDataActions": [],
       "AssignableScopes": [
         "/subscriptions/{subscription-id}"
       ]
     }
     ```
   - Click "Review + create" and then "Create".

### 2. Assign the Custom Role to Users

1. **Navigate to the Resource**:
   - Locate the resource to which you want to assign the custom RBAC role (e.g., a resource group, storage account, virtual machine).

2. **Access the Access Control (IAM) Blade**:
   - Click on the resource to open its management pane.
   - In the left-hand menu, select "Access control (IAM)".

3. **Add Role Assignment**:
   - Click on "+ Add" and select "Add role assignment".
   - In the "Role" dropdown, select the custom role you created.
   - In the "Assign access to" dropdown, select "User, group, or service principal".
   - Click on "Select members" and search for the user you want to assign the role to.
   - Select the user and click "Save" to assign the role.

### 3. Test the Assigned Role

1. **Sign In with the User Account**:
   - Sign out of the Azure Portal and sign back in with the user account to which you assigned the custom RBAC role.

2. **Navigate to the Resource**:
   - Attempt to access the resource you assigned the role to (e.g., a resource group, storage account, virtual machine).

3. **Verify Permissions**:
   - Verify that the user can perform actions permitted by the assigned custom role. For example:
     - If the role allows reading virtual machines, the user should be able to view virtual machine details but not start or stop them if those actions were not included.

## Example Test Scenario:

- **Scenario**: Create a custom role that allows users to read virtual machines and list storage account keys, assign this role to a user, and verify that the user can perform these actions.

### Steps:

1. **Create Custom Role**:
   - Follow the steps in the "Create a Custom Role" section to create a role with the necessary permissions.

2. **Assign Role**:
   - Assign the custom role to the user for the target resource following the steps in the "Assign the Custom Role to Users" section.

3. **Test Role**:
   - Sign in with the user's account and navigate to the resource.
   - Verify that the user can read virtual machines and list storage account keys.

## Additional Considerations:

- **Permission Scopes**: Ensure the permissions and assignable scopes match your requirements.
- **Audit Logs**: Use Azure Monitor and audit logs to track role assignments and access changes.
- **Role Updates**: Regularly review and update custom roles to adapt to changing requirements.
