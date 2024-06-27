# Create a Stored Access Policy Over Shared Access Signature and Check Access Scope 💿

## Prerequisites ✔️
- Azure Subscription
- Azure Storage Account
- Azure Storage Explorer installed on your machine

## Step 1: Create a Stored Access Policy 📄

1. **Navigate to the Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

2. **Select Your Storage Account**:
   - In the left-hand menu, select "Storage accounts".
   - Click on the storage account you want to manage.

3. **Create a Stored Access Policy for Blob Container**:
   - Navigate to "Containers" under your storage account.
   - Select the container you want to apply the policy to.
   - Click on the "Access policy" button in the container settings.

4. **Add a New Policy**:
   - Click "Add policy".
   - Configure the policy settings:
     - **Identifier**: Enter a name for the policy.
     - **Start and Expiry Date/Time**: Set the start and expiry date/time for the policy.
     - **Permissions**: Select the permissions you want to grant (e.g., Read, Write, Delete).
   - Click "OK" to save the policy.

## Step 2: Generate a SAS Token Using the Stored Access Policy 🎟️

1. **Generate SAS Token**:
   - Navigate back to the container settings.
   - Click on "Shared access signature" under the "Settings" section.
   - Configure the SAS settings:
     - **Permissions**: Select the permissions you want to grant.
     - **Start and Expiry Date/Time**: Set the start and expiry date/time for the SAS token.
     - **Allowed IP Addresses**: (Optional) Restrict access to specific IP addresses.
     - **Allowed Protocols**: Choose between HTTPS only or HTTP and HTTPS.
     - **Signing Key**: Select "User provided policy" and choose the policy identifier you created.
   - Click on "Generate SAS and connection string".

2. **Copy the SAS Token**:
   - After generating the SAS, copy the SAS token (the part starting with `?sv=`) and save it securely.

## Step 3: Use the SAS Token in Azure Storage Explorer 💽

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

## Step 4: Check Access Scope 🔗

1. **Verify Permissions**:
   - Try performing different actions (e.g., read, write, delete) on the storage account services.
   - Ensure that only the permissions granted by the SAS and the stored access policy are allowed. For example:
     - If the SAS token has only read permissions, try uploading a file to verify that write operations are not allowed.
     - If the SAS token has delete permissions, try deleting a blob or file.

2. **Access Blob Containers**:
   - Navigate to "Blob Containers" under your connected storage account.
   - Try to upload, download, or delete blobs based on the permissions granted by the SAS and the stored access policy.

3. **Access File Shares**:
   - Navigate to "File Shares" under your connected storage account.
   - Try to upload, download, or delete files based on the permissions granted by the SAS and the stored access policy.
