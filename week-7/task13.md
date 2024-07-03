# Create an Azure Key Vault and Store Secrets

To create an Azure Key Vault and store secrets using Azure CLI, follow these steps:

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
