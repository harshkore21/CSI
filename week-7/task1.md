# Observe Assigned Subscriptions in Azure

Azure provides various ways to manage and observe your assigned subscriptions using the Azure CLI and the Azure Portal. Follow these steps to list and manage your Azure subscriptions.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Step-by-Step Guide](#step-by-step-guide)
  - [1. Using Azure Portal](#1-using-azure-portal)
  - [2. Using Azure CLI](#2-using-azure-cli)
- [Example Test Scenario](#example-test-scenario)
- [Additional Considerations](#additional-considerations)

## Prerequisites:
- Azure Subscription
- Azure CLI installed on your local machine
- Azure account with the necessary permissions

## Step-by-Step Guide:

### 1. Using Azure Portal

1. **Sign In to Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

2. **Access Subscriptions**:
   - In the left-hand menu, select "Subscriptions".
   - This page will list all the subscriptions associated with your Azure account.
   - You can view details such as subscription ID, subscription name, and subscription status.

3. **Manage Subscriptions**:
   - Click on any subscription to view more details.
   - You can manage settings, view resource usage, and access billing information.

### 2. Using Azure CLI

1. **Install Azure CLI** (if not already installed):
   - Follow the instructions on the [Azure CLI installation guide](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli).

2. **Sign In to Azure CLI**:
   - Open your terminal or command prompt.
   - Run the command `az login` and follow the prompts to sign in with your Azure account.

3. **List Subscriptions**:
   - Once signed in, run the command `az account list --output table`.
   - This will display a list of all subscriptions associated with your Azure account in a table format.

4. **Set Active Subscription**:
   - If you need to work with a specific subscription, run the command `az account set --subscription "Your-Subscription-Name"`.

## Example Test Scenario:

- **Scenario**: List and view details of all Azure subscriptions associated with your account using Azure CLI. Set a specific subscription as the active subscription for further operations.

### Steps:

1. **List Subscriptions**:
   - Run `az account list --output table` to list all subscriptions.

2. **Set Active Subscription**:
   - Run `az account set --subscription "Your-Subscription-Name"` to set the desired subscription as active.

3. **Verify Active Subscription**:
   - Run `az account show` to display the currently active subscription.

## Additional Considerations:

- **Permissions**: Ensure your Azure account has the necessary permissions to view and manage subscriptions.
- **Billing**: Use the Azure Portal to access detailed billing and cost management information for each subscription.
- **Automation**: Automate subscription management tasks using Azure CLI scripts and Azure DevOps.
