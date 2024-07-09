# Creating an Alert Rule for VM CPU Percentage: More Than 80% 🚨

## Prerequisites ✔️
- Azure Subscription
- Azure Virtual Machine (VM) created and running
- Basic understanding of Azure Monitor and Alerts

## Step 1: Sign in to Azure Portal 🌍

1. **Navigate to the Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

## Step 2: Navigate to Monitor ⚙️

1. **Open Azure Monitor**:
   - In the left-hand menu, click on "Monitor".

## Step 3: Create an Alert Rule for VM CPU Percentage 📈

1. **Create a New Alert Rule**:
   - In Azure Monitor, click on "Alerts" in the left-hand menu.
   - Click on "+ New alert rule".

2. **Select Resource**:
   - Click on "Select a resource".
   - Use the filters to find your VM and select it.
   - Click "Done".

3. **Configure Condition**:
   - Click on "Add condition".
   - In the "Configure signal logic" pane, search for and select "Percentage CPU".
   - Under "Threshold", set the criteria as "Greater than" and value as "80".
   - Click "Done".

4. **Configure Action Group**:
   - Click on "Add action group".
   - Click on "+ Create action group".
   - **Basics**:
     - **Action group name**: Enter a name (e.g., `HighCPUAlertGroup`).
     - **Short name**: Enter a short name (e.g., `HighCPU`).
     - **Subscription**: Select your subscription.
     - **Resource group**: Select an existing resource group or create a new one.
   - **Actions**:
     - Click "Add action" and choose "Email/SMS message/Push/Voice".
     - **Action name**: Enter a name (e.g., `EmailAlert`).
     - **Email**: Enter the email address where the alert should be sent.
     - Click "OK".
   - **Notifications** (Optional):
     - Configure additional notifications if needed.
   - Click "Review + create" and then "Create".

5. **Configure Alert Details**:
   - **Alert rule name**: Enter a name for the alert rule (e.g., `HighCPUAlert`).
   - **Description**: (Optional) Enter a description for the alert rule.
   - **Severity**: Select the severity level (e.g., "Sev 2" for Warning).
   - **Enable rule upon creation**: Ensure this is checked.

6. **Review and Create**:
   - Review the alert rule details and click "Create".

## Step 4: Verify Alert Rule Configuration ✅

1. **Check Alert Rules**:
   - Go to the "Alerts" section under Monitor.
   - Verify that the new alert rule is listed and enabled.
   - Check for any alert activity if the CPU usage exceeds 80%.
