# DevOps Project: Load Balancing using Azure Load Balancer 🖥️⚖️

## Objective 🎯
To use the Azure portal to create a public Azure Load Balancer, configuring it to manage a backend pool containing two virtual machines. Additionally, set up Azure Bastion, a NAT Gateway, a virtual network, and necessary subnets to support the load balancer configuration.

## Prerequisites ✔️
- Azure Subscription
- Basic understanding of Azure services

## Step-by-Step Instructions 📝

### Step 1: Create a Resource Group
1. **Navigate to Azure Portal**: 
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.
2. **Create a Resource Group**: 
   - Click on **Resource groups**.
   - Click on **Create**.
   - Fill in the project details and resource details.
   - Click on **Review + create** after validation, then click on **Create** to create the resource group (e.g., `Harsh_RD`).

### Step 2: Create an Availability Set
1. **Navigate to Availability Sets**:
   - Click on **Availability sets**.
   - Click on **Create**.
2. **Fill in the Details**:
   - Fill in the project details and instance details.
   - Click on **Review + create** after validation, then click on **Create** to create the availability set (e.g., `Harsh_Aset001`).

### Step 3: Create Virtual Machines
1. **Create the First Virtual Machine**:
   - Go to **Virtual machine** and click on **Create**.
   - Fill in the project details, instance details, administrator account, and inbound port rules.
   - Click on **Review + create** after validation, then click on **Create** (e.g., `HarshVM001`).
2. **Set Up the First Virtual Machine**:
   - Click on the created VM to see details.
   - Copy the Public IP address.
   - Open **Remote Desktop Connection** and paste the copied IP address, then connect using your credentials.
   - In the VM, open **Server Manager** and install **IIS server**.
   - Create a custom page with the content “Hi This is HarshVM001”.
3. **Create the Second Virtual Machine**:
   - Repeat the steps above to create another VM (e.g., `HarshVM002`).
4. **Set Up the Second Virtual Machine**:
   - Repeat the steps above to set up the second VM with a custom page “Hi This is HarshVM002”.

### Step 4: Create a Load Balancer
1. **Navigate to Load Balancers**:
   - Click on **Load Balancer** and click on **Create**.
2. **Fill in the Details**:
   - Fill in the basic details and click on **Next**.
3. **Add Frontend IP Configuration**:
   - Add the frontend IP configuration and click on **Review + create**.
   - Click on **Create** to create the load balancer (e.g., `Harsh_LB001`).

### Step 5: Configure Load Balancer
1. **Add Backend Pools**:
   - Click on the created load balancer and add backend pools.
   - Select the two virtual machines.
2. **Add Health Probes**:
   - Add health probes.
3. **Add Load Balancing Rules**:
   - Add load balancing rules.
4. **Test the Load Balancer**:
   - Go to the **Overview** of the load balancer and copy the public IP address.
   - Paste the IP address in a new browser tab to see the first VM's custom page, then reload to see the second VM's custom page.

---

# Application Gateway Setup 🌐🚪

## Step-by-Step Instructions 📝

### Step 1: Create an Application Gateway
1. **Navigate to Application Gateway**:
   - Click on **Application Gateway** and click on **Create**.
2. **Fill in the Details**:
   - Fill in the basics.
3. **Add Subnet**:
   - Add a subnet (e.g., `hk_subnet`) and select it.
4. **Configure Frontend and Backend**:
   - Fill in the frontend and backend details.
5. **Add Backend Settings and Routing Rules**:
   - Add backend settings and routing rules.
6. **Create the Application Gateway**:
   - After validation, click on **Create**.

### Step 2: Test the Application Gateway
1. **Copy the Frontend IP Address**:
   - Click on the created application gateway and copy the frontend IP address.
2. **Test the Gateway**:
   - Paste the IP address in a new browser tab to see the first VM's custom page, then reload to see the second VM's custom page.
