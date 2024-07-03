# Create Virtual Machine and VNet from Azure CLI

To create a Virtual Machine (VM) and Virtual Network (VNet) using Azure CLI, follow these steps:

## Create Virtual Network (VNet)

1. **Login to Azure CLI:**
   ```bash
   az login
   ```

2. **Set Subscription (if not already set):**
   ```bash
   az account set --subscription <subscription-id>
   ```

3. **Create Resource Group:**
   ```bash
   az group create --name MyResourceGroup --location eastus
   ```

   Replace `eastus` with your desired Azure region.

4. **Create Virtual Network:**
   ```bash
   az network vnet create --resource-group MyResourceGroup --name MyVNet --address-prefixes 10.0.0.0/16 --subnet-name MySubnet --subnet-prefixes 10.0.1.0/24
   ```

   Adjust the `address-prefixes` and `subnet-prefixes` as per your network requirements.

## Create Virtual Machine (VM)

1. **Create VM:**
   ```bash
   az vm create \
   --resource-group MyResourceGroup \
   --name MyVM \
   --image UbuntuLTS \
   --admin-username azureuser \
   --admin-password 123 \
   --vnet-name MyVNet \
   --subnet MySubnet \
   --public-ip-address "" \
   --size Standard_DS1_v2
   ```

  Replace `<your-password>` with your desired password for the VM.

2. **Open Ports (Optional):**
   ```bash
   az vm open-port --resource-group MyResourceGroup --name MyVM --port 80
   ```

   Modify `--port` as needed for your application.
