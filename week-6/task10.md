# Testing Object Replication in Azure Blob Storage 🗃️

Testing object replication in Azure Blob Storage involves verifying that data stored in a primary storage account is replicated to a secondary (replica) storage account in a different region for redundancy and disaster recovery purposes. Here’s a structured approach to test object replication in Azure Blob Storage:

## Prerequisites: ✔️
- Two Azure Storage Accounts: Primary and Secondary (replica), preferably in different regions.
- Azure Storage Explorer or Azure Portal access.
- Sample blobs or files to upload for testing.

## Steps to Test Object Replication: 🔗

### 1. Set Up Replication:

- Ensure that you have configured Geo-redundant storage (RA-GRS or GRS) for your storage accounts. This ensures that data is replicated asynchronously to a secondary region.

### 2. Upload Test Objects:

#### Access Your Primary Storage Account:
- Navigate to the Azure Portal (portal.azure.com).
- Go to "Storage accounts" and select your primary storage account.

#### Upload Sample Objects:
- Navigate to the blob container where you want to test replication.
- Upload one or more sample blobs or files to this container. You can use Azure Storage Explorer for this purpose as well.

### 3. Verify Replication Status:

#### Check Blob Replication Status:
- After uploading, wait for a few minutes to allow time for replication to occur. Replication is asynchronous and may take some time depending on the data size and network conditions.

#### Navigate to Secondary Storage Account:
- Go to the Azure Portal.
- Select your secondary (replica) storage account.

#### Verify Blob Container and Objects:
- Navigate to the corresponding blob container in the secondary storage account.
- Verify that the uploaded blobs or files from the primary storage account are replicated and visible in the secondary storage account.

### 4. Confirm Data Integrity and Accessibility:

#### Download and Compare Objects:
- Download a replicated object from the secondary storage account to ensure that it matches the original from the primary storage account.
- Compare metadata and content to verify integrity.

#### Test Read Operations:
- Perform read operations (e.g., download, view properties) on the replicated objects from the secondary storage account to confirm accessibility.

## Example Test Scenario: ⬇️

- **Scenario**: Upload a file (`testfile.txt`) to the primary storage account in `East US`. Verify its replication to the secondary storage account in `West US`.
