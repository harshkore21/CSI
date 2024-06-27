# Creating an Azure Storage Account and Exploring Options 🗃️

## Prerequisites ✔️
- Azure Subscription
- Basic understanding of Azure services

## Step 1: Sign in to Azure Portal 🌍

1. **Navigate to the Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

## Step 2: Create a Storage Account 💾

1. **Create a Storage Account**:
   - Click "Create a resource" in the left-hand menu.
   - Search for "Storage account" and select it.
   - Click "Create".

2. **Configure Basics**:
   - **Subscription**: Select your Azure subscription.
   - **Resource group**: Select an existing resource group or create a new one.
   - **Storage account name**: Enter a unique name for your storage account.
   - **Region**: Select the Azure region where you want your storage account to be located.
   - **Performance**:
     - Standard: For general-purpose storage.
     - Premium: For low-latency, high-throughput scenarios.
   - **Redundancy**:
     - Locally-redundant storage (LRS)
     - Zone-redundant storage (ZRS)
     - Geo-redundant storage (GRS)
     - Read-access geo-redundant storage (RA-GRS)

3. **Advanced Options**:
   - **Security**:
     - Enable infrastructure encryption
     - Enable secure transfer required
   - **Networking**:
     - Connectivity method: Public endpoint (all networks), Public endpoint (selected networks), Private endpoint.
   - **Data protection**:
     - Enable soft delete for blobs
     - Enable soft delete for containers
     - Enable versioning
     - Enable blob change feed
     - Enable blob immutability
   - **Blob access tiers**:
     - Hot: Optimized for data that is accessed frequently.
     - Cool: Optimized for data that is infrequently accessed.
     - Archive: Lowest-cost option for data that is rarely accessed.

4. **Tags** (Optional):
   - Add tags to categorize your storage account (e.g., Environment: Production, Department: Finance).

5. **Review + create**:
   - Review your settings and click "Create".

## Step 3: Explore Storage Account Features 💽

1. **Overview**:
   - View basic information about your storage account, including performance, access tier, and redundancy.

2. **Containers**:
   - Create and manage blobs in containers.

3. **File Shares**:
   - Create file shares to manage file storage.

4. **Queues**:
   - Create and manage queues for message storage.

5. **Tables**:
   - Create and manage tables for NoSQL data storage.

6. **Access Control (IAM)**:
   - Manage access permissions for your storage account.

7. **Networking**:
   - Configure network access rules and private endpoints.

8. **Data Protection**:
   - Configure soft delete, versioning, and other data protection features.

9. **Encryption**:
   - Manage encryption settings for your data at rest.

10. **Monitoring**:
    - View metrics, logs, and alerts related to your storage account.

11. **Configuration**:
    - Configure properties like minimum TLS version and large file shares.

12. **Shared Access Signature (SAS)**:
    - Generate SAS tokens for granular access control to your storage account.

