# Create a Virtual Machine (VM) from PowerShell

To create a Virtual Machine (VM) using Azure PowerShell, follow these steps:

## Step-by-Step Guide

1. **Install Azure PowerShell Module (if not already installed):**
   ```powershell
   Install-Module -Name Az -AllowClobber -Scope CurrentUser
   ```

2. **Login to Azure:**
   ```powershell
   Connect-AzAccount
   ```

3. **Set Subscription (if not already set):**
   ```powershell
   Select-AzSubscription -SubscriptionId <subscription-id>
   ```

4. **Create a Resource Group:**
   ```powershell
   $resourceGroupName = "MyResourceGroup"
   $location = "EastUS"
   New-AzResourceGroup -Name $resourceGroupName -Location $location
   ```

5. **Define VM Parameters:**
   ```powershell
   $vmName = "MyVM"
   $cred = Get-Credential -Message "Enter the username and password for the VM"

   $vmConfig = New-AzVMConfig -VMName $vmName -VMSize "Standard_DS1_v2" | `
       Set-AzVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred | `
       Set-AzVMSourceImage -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2019-Datacenter" -Version "latest" | `
       Add-AzVMNetworkInterface -Id $nic.Id
   ```

6. **Create a Virtual Network and Subnet:**
   ```powershell
   $vnet = New-AzVirtualNetwork -ResourceGroupName $resourceGroupName -Location $location -Name "MyVNet" -AddressPrefix "10.0.0.0/16"
   $subnet = Add-AzVirtualNetworkSubnetConfig -Name "MySubnet" -AddressPrefix "10.0.1.0/24" -VirtualNetwork $vnet
   $vnet | Set-AzVirtualNetwork
   ```

7. **Create a Public IP Address:**
   ```powershell
   $pip = New-AzPublicIpAddress -ResourceGroupName $resourceGroupName -Location $location -Name "MyPublicIP" -AllocationMethod Dynamic
   ```

8. **Create a Network Security Group (NSG):**
   ```powershell
   $nsgRuleRDP = New-AzNetworkSecurityRuleConfig -Name "Allow-RDP-All" -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
   $nsg = New-AzNetworkSecurityGroup -ResourceGroupName $resourceGroupName -Location $location -Name "MyNSG" -SecurityRules $nsgRuleRDP
   ```

9. **Create a Network Interface:**
   ```powershell
   $nic = New-AzNetworkInterface -Name "MyNIC" -ResourceGroupName $resourceGroupName -Location $location -SubnetId $subnet.Id -PublicIpAddressId $pip.Id -NetworkSecurityGroupId $nsg.Id
   ```

10. **Create the Virtual Machine:**
    ```powershell
    New-AzVM -ResourceGroupName $resourceGroupName -Location $location -VM $vmConfig
    ```
