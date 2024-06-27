# Provision Access Keys and Connect with Storage Account 🔐

## Prerequisites ✔️
- Azure Subscription
- Azure Storage Account
- Azure Storage Explorer installed on your machine

## Step 1: Provision Access Keys 🔑

1. **Navigate to the Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

2. **Select Your Storage Account**:
   - In the left-hand menu, select "Storage accounts".
   - Click on the storage account you want to manage.

3. **Access the Access Keys**:
   - In the storage account pane, under "Security + networking", select "Access keys".
   - You will see two access keys (key1 and key2) and the corresponding connection strings.

4. **Copy an Access Key**:
   - Click on the "Copy" button next to one of the access keys (e.g., key1).
   - Save this key securely as you will need it for connecting to the storage account.

## Step 2: Connect with Storage Account Using Access Keys in Azure Storage Explorer ⚙️

1. **Open Azure Storage Explorer**:
   - Launch Azure Storage Explorer on your machine.

2. **Add an Account Using Access Keys**:
   - Click on the "Connect to Azure Storage" button (or the plug icon).
   - In the "Connect to Azure Storage" dialog, select "Use a storage account name and key".
   - Click "Next".

3. **Enter Storage Account Details**:
   - Enter the "Storage Account Name" (the name of your storage account).
   - Enter the "Storage Account Key" (the access key you copied earlier).
   - Optionally, you can enter a "Display name" to easily identify this connection.
   - Click "Next".

4. **Confirm and Connect**:
   - Review the information and click "Connect".

5. **Verify Connection**:
   - After successfully connecting, you will see your storage account listed under "Local & Attached" -> "Storage Accounts" in Azure Storage Explorer.
   - Expand the storage account to see the available services (Blob Containers, File Shares, Queues, Tables).

## Step 3: Manage Storage Account Using Azure Storage Explorer 👨‍💻

### Manage Blob Containers

1. **Create a Blob Container**:
   - Right-click on "Blob Containers" under your connected storage account.
   - Select "Create Blob Container".
   - Enter a name for your container and click "OK".

2. **Upload a Blob**:
   - Click on the container you created.
   - Click the "Upload" button in the toolbar.
   - Select "Upload Files" or "Upload Folder" based on your requirement.
   - Browse and select the files or folders you want to upload.
   - Click "Upload".

3. **Access a Blob**:
   - Navigate to the container and select the blob you uploaded.
   - Right-click on the blob and select "Copy URL" to get the blob URL.
   - You can access the blob using the copied URL in a web browser if the container's access level allows it.

### Manage File Shares

1. **Create a File Share**:
   - Right-click on "File Shares" under your connected storage account.
   - Select "Create File Share".
   - Enter a name for your file share and click "OK".

2. **Upload Files to File Share**:
   - Click on the file share you created.
   - Click the "Upload" button in the toolbar.
   - Select "Upload Files" or "Upload Folder".
   - Browse and select the files or folders you want to upload.
   - Click "Upload".

3. **Access Files in File Share**:
   - Navigate to the file share and select the files you uploaded.
   - You can download or delete files by right-clicking on them and selecting the appropriate option.
