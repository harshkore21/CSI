# Upload and Access a Blob in Azure Storage 🗂️

## Prerequisites ✔️
- Azure Subscription
- Azure Storage Account
- Azure Storage Explorer (optional but recommended)

## Step 1: Create a Blob Container 🗄️

1. **Navigate to the Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

2. **Select Your Storage Account**:
   - In the left-hand menu, select "Storage accounts".
   - Choose the storage account you want to use for blob storage.

3. **Create a Blob Container**:
   - Under the "Data storage" section, click on "Containers".
   - Click on the "+ Container" button.
   - Provide a name for your container (e.g., `mycontainer`).
   - Set the public access level:
     - Private (no anonymous access)
     - Blob (anonymous read access for blobs only)
     - Container (anonymous read access for container and blobs)
   - Click "Create".

## Step 2: Upload a Blob 📡

### Method 1: Using Azure Portal

1. **Navigate to Your Container**:
   - In the storage account, go to the "Containers" section.
   - Click on the container you created (`mycontainer`).

2. **Upload a Blob**:
   - Click the "Upload" button.
   - Browse and select the file you want to upload.
   - Click "Upload".

### Method 2: Using Azure Storage Explorer

1. **Open Azure Storage Explorer**:
   - Download and install [Azure Storage Explorer](https://azure.microsoft.com/en-us/features/storage-explorer/).

2. **Connect to Your Storage Account**:
   - Click "Add an account" and sign in with your Azure credentials.
   - Navigate to your storage account and expand it to see the blob containers.

3. **Upload a Blob**:
   - Right-click on your container (`mycontainer`) and select "Upload".
   - Select the file you want to upload and click "Upload".

## Step 3: Access the Blob 🛰️

### Using Azure Portal

1. **Navigate to Your Blob**:
   - Go to your container (`mycontainer`).
   - Click on the blob you uploaded.

2. **Get Blob URL**:
   - Under "Properties", copy the URL of the blob.
   - If the container's access level is set to "Blob" or "Container", you can access the blob via the copied URL in a web browser.

### Using Azure Storage Explorer 🔧

1. **Navigate to Your Blob**:
   - In Azure Storage Explorer, navigate to your container (`mycontainer`).
   - Right-click on the blob you uploaded and select "Properties".

2. **Get Blob URL**:
   - Copy the URL from the properties window.
   - Access the blob using the copied URL if the container's access level allows it.
