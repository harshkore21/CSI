# Create and Assign a Policy at Subscription Level

To create and assign a policy at the subscription level in Azure, follow these steps using Azure Policy and Azure CLI:

## Step-by-Step Guide

1. **Login to Azure CLI:**
   ```bash
   az login
   ```

2. **Set Subscription (if not already set):**
   ```bash
   az account set --subscription <subscription-id>
   ```

3. **Create a Policy Definition:**
   You can create a custom policy definition using Azure CLI. Below is an example command to create a simple policy definition that enforces a tag on all resources.
   ```bash
   az policy definition create \
     --name "EnforceTagOnResources" \
     --display-name "Enforce a tag on all resources" \
     --description "This policy enforces a required tag on all supported Azure resources." \
     --rules '{ "if": { "not": { "field": "tags.environment", "exists": "true" } }, "then": { "effect": "deny" } }' \
     --mode All
   ```

   Modify the policy definition (`--name`, `--display-name`, `--description`, `--rules`) as per your requirements.

4. **Assign the Policy Definition to the Subscription:**
   Once the policy definition is created, you need to assign it to the subscription.
   ```bash
   az policy assignment create \
     --name "EnforceTagAssignment" \
     --display-name "Enforce tag on all resources assignment" \
     --policy "EnforceTagOnResources" \
     --scope "/subscriptions/<subscription-id>"
   ```

   Replace `<subscription-id>` with your actual subscription ID.
