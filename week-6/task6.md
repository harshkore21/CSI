# Create a Shared Access Signature (SAS) and Check Access Scope 🌐

## Prerequisites ✔️
- Azure Subscription
- Azure Storage Account
- Azure Storage Explorer installed on your machine

## Step 1: Create a Shared Access Signature (SAS) 💻

1. **Navigate to the Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

2. **Select Your Storage Account**:
   - In the left-hand menu, select "Storage accounts".
   - Click on the storage account you want to manage.

3. **Generate a SAS Token**:
   - In the storage account pane, under "Security + networking", select "Shared access signature".
   - Configure the SAS settings:
     - **Permissions**: Select the permissions you want to grant (e.g., Read, Write, Delete).
     - **Start and Expiry Date/Time**: Set the start and expiry date/time for the SAS token.
     - **Allowed IP Addresses**: (Optional) Restrict access to specific IP addresses.
     - **Allowed Protocols**: Choose between HTTPS only or HTTP and HTTPS.
   - Click on "Generate SAS and connection string".

4. **Copy the SAS Token**:
   - After generating the SAS, copy the SAS token (the part starting with `?sv=`) and save it securely.

## Step 2: Use the SAS Token in Azure Storage Explorer 🎫

1. **Open Azure Storage Explorer**:
   - Launch Azure Storage Explorer on your machine.

2. **Add an Account Using SAS**:
   - Click on the "Connect to Azure Storage" button (or the plug icon).
   - In the "Connect to Azure Storage" dialog, select "Use a shared access signature (SAS) URI".
   - Click "Next".

3. **Enter SAS URI**:
   - Enter the full SAS URI (including the storage account URL and the SAS token) in the "URI" field.
   - Optionally, you can enter a "Display name" to easily identify this connection.
   - Click "Next".

4. **Confirm and Connect**:
   - Review the information and click "Connect".

5. **Verify Connection**:
   - After successfully connecting, you will see the storage account listed under "Local & Attached" -> "Storage Accounts (SAS)" in Azure Storage Explorer.
   - Expand the storage account to see the available services (Blob Containers, File Shares, Queues, Tables) based on the SAS permissions.

## Step 3: Check Access Scope 🛠️

1. **Verify Permissions**:
   - Try performing different actions (e.g., read, write, delete) on the storage account services.
   - Ensure that only the permissions granted by the SAS are allowed. For example:
     - If the SAS token has only read permissions, try uploading a file to verify that write operations are not allowed.
     - If the SAS token has delete permissions, try deleting a blob or file.

2. **Access Blob Containers**:
   - Navigate to "Blob Containers" under your connected storage account.
   - Try to upload, download, or delete blobs based on the permissions granted by the SAS.

3. **Access File Shares**:
   - Navigate to "File Shares" under your connected storage account.
   - Try to upload, download, or delete files based on the permissions granted by the SAS.
