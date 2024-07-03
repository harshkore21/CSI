# Observe Assigned Subscriptions in Azure

Observing assigned subscriptions in Azure helps you understand the scope of your access and manage resources efficiently. This guide will walk you through the steps to observe your assigned subscriptions using the Azure CLI.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Step-by-Step Guide](#step-by-step-guide)
  - [1. Install Azure CLI](#1-install-azure-cli)
  - [2. Sign In to Azure CLI](#2-sign-in-to-azure-cli)
  - [3. List Assigned Subscriptions](#3-list-assigned-subscriptions)
  - [4. Set a Default Subscription](#4-set-a-default-subscription)

## Prerequisites:
- Azure Subscription
- Azure CLI installed on your local machine

## Step-by-Step Guide:

### 1. Install Azure CLI

1. **Install Azure CLI**:
   - Follow the instructions on the [Azure CLI installation page](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli) to install Azure CLI on your local machine.
   - Verify the installation by running the following command in your terminal:
     ```sh
     az --version
     ```

### 2. Sign In to Azure CLI

1. **Sign In to Your Azure Account**:
   - Open a terminal or command prompt.
   - Run the following command to sign in to your Azure account:
     ```sh
     az login
     ```
   - A web browser will open and prompt you to enter your Azure account credentials. Follow the instructions to complete the sign-in process.

### 3. List Assigned Subscriptions

1. **List All Subscriptions**:
   - After signing in, run the following command to list all subscriptions associated with your account:
     ```sh
     az account list --output table
     ```
   - This command will display a table with details of all your subscriptions, including `Name`, `CloudName`, `SubscriptionId`, and `State`.

2. **List Only Enabled Subscriptions**:
   - To list only the enabled subscriptions, run the following command:
     ```sh
     az account list --query "[?state=='Enabled']" --output table
     ```

### 4. Set a Default Subscription

1. **Set Default Subscription**:
   - If you have multiple subscriptions and want to set one as the default, run the following command:
     ```sh
     az account set --subscription "SubscriptionNameOrId"
     ```
   - Replace `"SubscriptionNameOrId"` with the name or ID of the subscription you want to set as the default.
