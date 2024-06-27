# Azure Storage Access Tiers and Their Use Cases 💼

Azure Storage provides different access tiers to optimize storage costs based on the frequency of data access. Understanding these tiers and their use cases helps in selecting the appropriate tier for your data storage needs.

## Access Tiers Overview 🪟

Azure Storage offers three access tiers:

1. **Hot Access Tier**:
   - Optimized for data that is accessed frequently.
   - Highest storage cost but the lowest access cost.
   - Ideal for data that is in active use, such as websites, applications, or any data that needs to be retrieved often.

2. **Cool Access Tier**:
   - Optimized for data that is infrequently accessed and stored for at least 30 days.
   - Lower storage cost compared to the hot tier but higher access cost.
   - Suitable for data that is not accessed frequently but needs to be available immediately when required. Examples include backups, archived data, or long-term data storage with occasional access.

3. **Archive Access Tier**:
   - Lowest storage cost and the highest access cost.
   - Data is stored offline and must be rehydrated before it can be accessed, which can take several hours.
   - Ideal for data that is rarely accessed and can tolerate high latency in retrieval. Examples include long-term archival, compliance data, and data that needs to be retained for legal or regulatory reasons.

## Use Cases for Each Access Tier ☁️

### Hot Access Tier

- **Active Databases**: Databases with high transaction rates that require low-latency access.
- **Web Applications**: Websites and applications that need quick data retrieval to provide a seamless user experience.
- **Content Delivery**: Frequently accessed media files, documents, and other content delivered to users in real-time.

### Cool Access Tier

- **Backup Storage**: Recent backups that might need to be restored occasionally.
- **Disaster Recovery**: Data required for disaster recovery solutions, ensuring quick access when necessary.
- **Infrequent Data Access**: Data that is accessed less frequently but still needs to be retrieved quickly when needed.

### Archive Access Tier

- **Long-Term Archival**: Data that needs to be stored for years due to compliance or regulatory requirements.
- **Historical Data**: Old logs, records, or any data that is kept for future reference but not actively used.
- **Compliance Data**: Data stored to meet legal obligations, which is rarely accessed but must be preserved.

## Changing Access Tiers 🌍

### Using Azure Portal

1. **Navigate to the Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

2. **Select Your Storage Account**:
   - In the left-hand menu, select "Storage accounts".
   - Click on the storage account containing the data you want to change the tier for.

3. **Access the Blob Storage**:
   - Navigate to "Blob service" -> "Containers".
   - Select the container and then the blob(s) you want to change the tier for.

4. **Change Access Tier**:
   - Click on the blob you want to change.
   - In the blob properties pane, select the desired access tier (Hot, Cool, or Archive) from the "Access tier" dropdown.
   - Click "Save" to apply the changes.

### Using Azure Storage Explorer

1. **Open Azure Storage Explorer**:
   - Launch Azure Storage Explorer on your machine.

2. **Connect to Your Storage Account**:
   - Ensure your storage account is connected in Azure Storage Explorer.

3. **Select the Blob Container**:
   - Navigate to the container containing the blob(s) you want to change the tier for.

4. **Change Access Tier**:
   - Right-click on the blob and select "Change Access Tier".
   - Choose the desired access tier from the list (Hot, Cool, or Archive).
   - Confirm the change.
