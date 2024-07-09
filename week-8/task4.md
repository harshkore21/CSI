# Scheduling a Daily Backup of VM at 3:00 AM using Vault with Retention Period 🕒

## Prerequisites ✔️
- Azure Subscription
- Azure Virtual Machine (VM) created
- Azure Recovery Services Vault created

## Step 1: Sign in to Azure Portal 🌍

1. **Navigate to the Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

## Step 2: Create or Use an Existing Recovery Services Vault 🛡️

1. **Create a Recovery Services Vault**:
   - Click "Create a resource" in the left-hand menu.
   - Search for "Recovery Services vault" and select it.
   - Click "Create".
   - Configure the basics:
     - **Name**: Enter a unique name for your vault.
     - **Subscription**: Select your subscription.
     - **Resource group**: Select an existing resource group or create a new one.
     - **Location**: Select the Azure region.
   - Click "Review + create" and then "Create".

## Step 3: Register the VM for Backup 🖥️

1. **Navigate to Backup Section**:
   - Go to your Recovery Services vault.
   - Click "Backup" under the "Getting started" section.

2. **Configure Backup**:
   - **Where is your workload running?**: Select "Azure".
   - **What do you want to back up?**: Select "Virtual machine".
   - Click "Start Backup".

3. **Select the VM**:
   - Choose the VM you want to back up.
   - Click "OK".

## Step 4: Create a Backup Policy with Retention Period ⏰

1. **Define Backup Policy**:
   - Go to the "Backup policies" section within your Recovery Services vault.
   - Click "+ Add" to create a new policy.
   - **Policy name**: Enter a name for your policy.
   - **Frequency**:
     - **Backup Schedule**: Daily.
     - **Time**: Set the time to 3:00 AM.
   - **Retention range**:
     - **Daily**: Retain backups for a specified number of days (e.g., 30 days).
     - **Weekly**: (Optional) Retain weekly backups for a specified number of weeks.
     - **Monthly**: (Optional) Retain monthly backups for a specified number of months.
     - **Yearly**: (Optional) Retain yearly backups for a specified number of years.
   - Click "OK" to create the policy.

## Step 5: Apply the Backup Policy 📅

1. **Assign Policy to VM**:
   - Go to the "Backup Items" section.
   - Select "Azure Virtual Machine".
   - Choose the VM you registered for backup.
   - Click "Backup now" to apply the policy and initiate the first backup.

## Step 6: Retain an Old Backup 📁

1. **Retain a Specific Backup**:
   - Go to the "Backup Items" section and select the VM.
   - Find the backup you want to retain.
   - Click on the backup and select the option to retain or lock it, ensuring it isn't deleted by retention policies.

## Step 7: Verify Backup Configuration ✅

1. **Check Backup Jobs**:
   - Go to the "Backup Jobs" section within your Recovery Services vault.
   - Verify that the backup job is scheduled and running as expected.
