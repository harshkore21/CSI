# Retrieve Secret from Azure Key Vault

To retrieve a secret from an Azure Key Vault using Azure CLI, follow these steps:

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
   az keyvault secret show --vault-name MyKeyVault --name MySecret --query value -o tsv
   ```

   This command retrieves the value of the secret stored in the Key Vault. Replace `MyKeyVault` and `MySecret` with your Key Vault name and secret name, respectively.
