# Create Azure File Sync 🗃️

Azure File Sync allows you to sync files from your on-premises Windows Server to an Azure file share, enabling centralized file management, multi-site synchronization, and cloud tiering. Follow these steps to set up Azure File Sync:

## Prerequisites: ✔️
- Azure Subscription
- Windows Server running Windows Server 2012 or later
- Azure File Sync agent installed on the Windows Server
- Azure Storage Account with File Sync enabled

## Steps to File Sync: 🔄

### 1. Prepare Azure Storage Account

1. **Create a Storage Account** (if not already created):
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.
   - In the left-hand menu, select "Storage accounts".
   - Click on "Add" to create a new storage account.
   - Choose a unique name, subscription, resource group, location, and performance (Standard or Premium).

2. **Enable Azure File Sync**:
   - In the storage account pane, under "File service", select "File sync".
   - Click on "+ Azure File Sync" to create a new sync group.
   - Follow the prompts to set up the sync group and associate it with your Azure file share.

### 2. Install Azure File Sync Agent on Windows Server

1. **Download and Install Azure File Sync Agent**:
   - Download the Azure File Sync agent from the Azure portal.
   - Install the agent on your on-premises Windows Server.
   - During installation, sign in with your Azure account credentials.

2. **Register Server with Azure File Sync**:
   - Open Azure File Sync agent on the Windows Server.
   - Follow the wizard to register the server with your Azure subscription.
   - Select the sync group and Azure file share created earlier.

### 3. Sync On-Premises Files to Azure

1. **Configure Sync Settings**:
   - In Azure File Sync agent, configure sync settings such as sync frequency, bandwidth usage, and sync filters (optional).

2. **Initial Sync**:
   - Start the initial synchronization process to upload on-premises files to the Azure file share.
   - Monitor the sync progress and ensure all files are successfully transferred.

### 4. Monitor and Manage Sync

1. **Monitor Sync Status**:
   - Use Azure Portal or Azure File Sync agent to monitor sync status, errors, and synchronization health.
   - Resolve any sync conflicts or issues as they arise.

2. **Manage Sync Group**:
   - Modify sync group settings as needed, such as adding additional servers or changing sync rules.
   - Use Azure Storage Explorer to view and manage files in the Azure file share.

## Example Test Scenario: 🚀

- **Scenario**: Set up Azure File Sync between an on-premises Windows Server and Azure Storage Account. Sync a folder containing test files to the Azure file share, monitor sync status, and verify file accessibility from Azure Portal.
