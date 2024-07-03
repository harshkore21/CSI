# Configure Access Policies for Azure Key Vault

To configure access policies for the Azure Key Vault to allow authorized users or applications to manage keys and secrets, follow these steps using Azure CLI:

## Step-by-Step Guide

1. **Login to Azure CLI:**
   ```bash
   az login
   ```

2. **Set Subscription (if not already set):**
   ```bash
   az account set --subscription <subscription-id>
   ```

3. **Create a Resource Group (if needed):**
   ```bash
   az group create --name MyResourceGroup --location eastus
   ```

   Replace `eastus` with your desired Azure region.

4. **Create Azure Key Vault:**
   ```bash
   az keyvault create --name MyKeyVault --resource-group MyResourceGroup --location eastus
   ```

   Replace `MyKeyVault` with your desired Key Vault name.

5. **Store a Secret in Key Vault:**
   ```bash
   az keyvault secret set --vault-name MyKeyVault --name MySecret --value "MySecretValue"
   ```

   Replace `MySecret` and `"MySecretValue"` with your secret name and value, respectively.

6. **Retrieve Secret from Key Vault:**
   ```bash
   az keyvault secret show --vault-name MyKeyVault --name MySecret
   ```

   This command retrieves the secret stored in the Key Vault.

## Configure Access Policies

1. **Get the Object ID of the User or Service Principal:**
   ```bash
   az ad user show --id user@example.com --query objectId --output tsv
   ```
   Or for a service principal:
   ```bash
   az ad sp show --id <app-id> --query objectId --output tsv
   ```

   Replace `user@example.com` with the email address of the user and `<app-id>` with the application ID of the service principal.

2. **Set Access Policy for the Key Vault:**
   ```bash
   az keyvault set-policy --name MyKeyVault --object-id <object-id> --secret-permissions get list set delete
   ```

   Replace `<object-id>` with the object ID obtained in the previous step. Adjust the permissions (`get`, `list`, `set`, `delete`) as required.

3. **Allow Applications to Access Key Vault (Optional):**
   ```bash
   az keyvault set-policy --name MyKeyVault --spn <app-id> --key-permissions get list create delete --secret-permissions get list set delete
   ```

   Replace `<app-id>` with the application ID of the service principal. Adjust the key and secret permissions as required.
