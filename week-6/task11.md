# Create Azure File Share and Test Functionality 👨🏻‍🔬

Azure File Storage provides a cloud-based file share that can be accessed and managed like a standard file share. Follow these steps to create an Azure File Share and test its functionality.

## Prerequisites: ✔️
- Azure Subscription
- Azure Storage Account
- Azure Storage Explorer or Azure Portal access

## Steps to File Share and Test Functionality: 

### 1. Create Azure File Share

1. **Navigate to the Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

2. **Create a Storage Account** (if not already created):
   - In the left-hand menu, select "Storage accounts".
   - Click on "Add" to create a new storage account.
   - Choose a unique name, subscription, resource group, location, and performance (Standard or Premium).

3. **Access Your Storage Account**:
   - Once created, navigate to your storage account in the Azure Portal.

4. **Create a File Share**:
   - In the storage account pane, under "File service", select "File shares".
   - Click on "+ File share" to create a new file share.
   - Enter a unique name for your file share and set the quota size (maximum size allowed for the file share).

### 2. Test File Share Functionality

1. **Upload Files**:

   #### Using Azure Storage Explorer:

   - Open Azure Storage Explorer.
   - Connect to your Azure subscription and navigate to your storage account.
   - Expand "File Shares" and select the file share you created.
   - Upload one or more test files or folders into the file share.

2. **Access Files**:

   #### Using Azure Portal:

   - Navigate to your storage account in the Azure Portal.
   - Go to "File shares" under "File service".
   - Click on the file share you created.
   - Open a file or folder to view its contents.

3. **Modify and Delete Files**:

   #### Using Azure Storage Explorer:

   - In Azure Storage Explorer, navigate to the file share and modify/delete files as needed.
   - Test renaming files, creating new folders, and deleting files to verify permissions and functionality.

4. **Access from VM or App**:

   - Mount the Azure File Share on a VM or access it from an application using the SMB protocol.
   - Perform read and write operations from the VM or application to ensure connectivity and data integrity.

## Example Test Scenario: 🧩

- **Scenario**: Create a file share named "testshare" in your storage account. Upload a folder with test files, access it from Azure Storage Explorer, and verify file operations (e.g., rename, delete).
