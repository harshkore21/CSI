# Azure Virtual Machine Load Balancing using Azure Load Balancer 📊

## Objective 🎯
Use the Azure portal to create a public Azure Load Balancer, configure it to manage a backend pool containing two virtual machines (VMs), and set up Azure Bastion, a NAT Gateway, a virtual network, and necessary subnets to support the load balancer configuration.

## Prerequisites ✔️
- Azure Subscription
- Basic understanding of Azure services

## Step 1: Sign in to Azure Portal 🌍

1. **Navigate to the Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

## Step 2: Create a Virtual Network (VNet) 🌐

1. **Create a VNet**:
   - Click "Create a resource" in the left-hand menu.
   - Search for "Virtual Network" and select it.
   - Click "Create".
   
2. **Configure VNet Basics**:
   - **Name**: Enter a unique name for your VNet.
   - **Region**: Select the Azure region.
   - **Address space**: Specify the address space (e.g., `10.0.0.0/16`).
   - **Subnet**: Add subnets, for example:
     - **Subnet 1**: Name: `frontend`, Address range: `10.0.1.0/24`
     - **Subnet 2**: Name: `backend`, Address range: `10.0.2.0/24`
   
3. **Review + create**:
   - Review your settings and click "Create".

## Step 3: Create a NAT Gateway 🔄

1. **Create a NAT Gateway**:
   - Click "Create a resource" and search for "NAT Gateway".
   - Click "Create".

2. **Configure NAT Gateway Basics**:
   - **Name**: Enter a unique name for your NAT Gateway.
   - **Virtual Network**: Select the VNet created in Step 2.
   - **Subnet**: Select the `frontend` subnet.
   - **Public IP Address**: Create a new public IP address or use an existing one.

3. **Review + create**:
   - Review your settings and click "Create".

## Step 4: Create Virtual Machines (VMs) 🖥️

1. **Create the first VM**:
   - Click "Create a resource" and select "Virtual Machine".
   - **Basics**:
     - **Name**: Enter a name for your VM (e.g., `vm1`).
     - **Region**: Select the same region as the VNet.
     - **Image**: Choose an OS image (e.g., Windows Server or Ubuntu).
     - **Size**: Choose an appropriate size.
   - **Networking**:
     - **Virtual network**: Select the VNet created in Step 2.
     - **Subnet**: Select the `backend` subnet.
     - **Public IP**: None (for internal load balancing).
   - **Management**: Disable boot diagnostics.

2. **Create the second VM**:
   - Repeat the steps to create another VM (e.g., `vm2`) in the `backend` subnet.

## Step 5: Create a Public Load Balancer ⚖️

1. **Create a Load Balancer**:
   - Click "Create a resource" and search for "Load Balancer".
   - Click "Create".

2. **Configure Load Balancer Basics**:
   - **Name**: Enter a unique name for your load balancer.
   - **Region**: Select the same region as your VNet.
   - **Type**: Select "Public".
   - **SKU**: Select "Standard".
   - **Public IP Address**: Create a new public IP address or use an existing one.

3. **Backend Pools**:
   - **Add a backend pool**: Name it (e.g., `backendpool`).
   - **Add VMs**: Select the VMs created in Step 4 and add them to the backend pool.

4. **Health Probes**:
   - **Add a health probe**: Name it (e.g., `healthprobe`).
   - **Protocol**: Select TCP.
   - **Port**: Enter 80.
   - **Interval**: Set to 5 seconds.
   - **Unhealthy threshold**: Set to 2.

5. **Load Balancing Rules**:
   - **Add a rule**: Name it (e.g., `lbrule`).
   - **Frontend IP Address**: Select the public IP address.
   - **Protocol**: Select TCP.
   - **Port**: Enter 80.
   - **Backend Port**: Enter 80.
   - **Backend Pool**: Select the backend pool created earlier.
   - **Health Probe**: Select the health probe created earlier.

6. **Review + create**:
   - Review your settings and click "Create".

## Step 6: Set up Azure Bastion for VM Access 🔒

1. **Create Azure Bastion**:
   - Click "Create a resource" and search for "Bastion".
   - Click "Create".

2. **Configure Bastion Basics**:
   - **Name**: Enter a unique name for Bastion.
   - **Region**: Select the same region as your VNet.
   - **Virtual Network**: Select the VNet created in Step 2.
   - **Subnet**: Select the `frontend` subnet.
   - **Public IP Address**: Create a new public IP address or use an existing one.

3. **Review + create**:
   - Review your settings and click "Create".

## Step 7: Test Load Balancer Configuration 🧪

1. **Access VMs via Bastion**:
   - Use Azure Bastion to access the VMs.
   - Install a web server or application on both VMs (e.g., Apache on Linux or IIS on Windows).

2. **Verify Load Balancer**:
   - Open a web browser and navigate to the public IP address of the load balancer.
   - Ensure that the requests are being balanced between the two VMs.

## Additional Resources 📚

- [Azure Load Balancer Documentation](https://learn.microsoft.com/en-us/azure/load-balancer/load-balancer-overview)
- [Azure Bastion Documentation](https://learn.microsoft.com/en-us/azure/bastion/bastion-overview)
- [Azure NAT Gateway Documentation](https://learn.microsoft.com/en-us/azure/virtual-network/nat-gateway/nat-gateway-resource)
- [Azure VNet Documentation](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)
- [Google Slides Presentation](https://docs.google.com/presentation/d/1bJbQs_TH6CMaZyOJGfXQl12jEo_jDHiN/edit?usp=sharing&ouid=106645495933275419660&rtpof=true&sd=true)