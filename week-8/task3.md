# Provisioning Backups in Azure Backup Center 🛡️

## Prerequisites ✔️
- Azure Subscription
- Azure Virtual Machine (VM) or other resources to back up
- Azure Recovery Services Vault created

## Step 1: Sign in to Azure Portal 🌍

1. **Navigate to the Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

## Step 2: Navigate to Backup Center ⚙️

1. **Open Backup Center**:
   - In the left-hand menu, click on "Backup center" under the "Operations" section.

## Step 3: Start Backup Process for VM or Other Resources 🖥️

1. **Start a Backup**:
   - In Backup Center, click on "+ Backup".

2. **Configure Backup**:
   - **Where is your workload running?**: Select "Azure".
   - **What do you want to back up?**: Select the appropriate option (e.g., "Azure Virtual machine" for VM backup).
   - Click "Continue".

3. **Select Backup Policy**:
   - **Vault**: Choose an existing Recovery Services vault or create a new one.
   - **Backup policy**: Select an existing policy or create a new one by clicking "Create new" and configuring the schedule and retention settings.
   - Click "Continue".

4. **Select Items to Backup**:
   - Click on "Add" and select the resources (e.g., VMs) you want to back up.
   - Click "OK" to confirm your selection.
   - Click "Continue".

## Step 4: Review and Finalize Backup Configuration ✅

1. **Review Backup Configuration**:
   - Ensure all configurations are correct, including the selected resources and backup policy.
   - Click "Enable Backup" to finalize the configuration.

## Step 5: Monitor Backup Jobs 🕒

1. **Check Backup Jobs**:
   - Go to the "Backup Jobs" section in Backup Center.
   - Monitor the status of the backup jobs to ensure they are running as expected.
