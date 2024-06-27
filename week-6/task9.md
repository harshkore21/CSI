# Apply Lifecycle Policy to Objects and Test the Policy 📝

Azure Storage Lifecycle Management policies allow you to manage your data's lifecycle by transitioning blobs to different access tiers, deleting them, or performing other actions based on defined rules. This guide explains how to apply a lifecycle management policy and test it.

## Prerequisites ✔️
- Azure Subscription
- Azure Storage Account
- Azure Storage Explorer installed on your machine

## Step 1: Define a Lifecycle Management Policy 🚲

1. **Navigate to the Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

2. **Select Your Storage Account**:
   - In the left-hand menu, select "Storage accounts".
   - Click on the storage account you want to manage.

3. **Access Lifecycle Management**:
   - In the storage account pane, under "Data management", select "Lifecycle management".

4. **Add a Rule**:
   - Click on "Add rule".
   - Define the rule with the following parameters:
     - **Name**: Enter a name for your rule.
     - **Rule Scope**: Select "Limit blobs with filters" if you want to apply the rule to specific containers or blobs, otherwise select "Apply rule to all blobs".
     - **Filter Set**: (Optional) Add filters based on blob name prefix or blob index tags to apply the rule only to specific blobs.

5. **Define Actions**:
   - **Transition blobs to a cooler storage tier**: Select the transition action and configure the number of days after modification or creation to transition blobs to Cool or Archive tier.
   - **Delete blobs**: Configure the number of days after modification or creation to delete blobs.
   - **Other actions**: Define other actions based on your requirements.

6. **Review and Save**:
   - Review the rule settings and click "Add" to save the rule.

## Step 2: Test the Lifecycle Management Policy ↩️

### Upload Test Blobs

1. **Upload Blobs to Your Storage Account**:
   - Open Azure Storage Explorer and connect to your storage account.
   - Navigate to the blob container where you want to test the lifecycle policy.
   - Upload several test blobs to the container.

### Verify Policy Application

1. **Wait for the Policy to Apply**:
   - Lifecycle policies run once a day. You may need to wait up to 24 hours for the policy to apply to your blobs.

2. **Check Blob Access Tier and Existence**:
   - After 24 hours, check the access tier of the blobs to verify if they have been transitioned according to the policy.
   - Check if any blobs have been deleted if the policy includes a deletion rule.

### Example Test Scenario

1. **Define a Lifecycle Policy**:
   - Rule Name: "Move to Cool Tier"
   - Rule Scope: Apply to all blobs
   - Action: Transition blobs to Cool storage tier after 1 day of creation

2. **Upload a Blob**:
   - Upload a blob to the container.

3. **Wait and Verify**:
   - Wait for 24 hours.
   - In Azure Storage Explorer, check the access tier of the blob. It should be set to Cool.

