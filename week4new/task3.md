# Azure Application Gateway Setup and Testing ⛩️

## Table of Contents 📋
1. [Introduction](#introduction)
3. [Create Azure Application Gateway](#create-azure-application-gateway)
4. [Configure Backend Pool and HTTP Settings](#configure-backend-pool-and-http-settings)
5. [Create and Test Listener and Routing Rules](#create-and-test-listener-and-routing-rules)
6. [Verify Application Gateway Configuration](#verify-application-gateway-configuration)
7. [Additional Resources](#additional-resources)

## Introduction 🎋

This guide provides step-by-step instructions to create an Azure Application Gateway, configure backend pools, HTTP settings, listeners, and routing rules, and verify its functionality.

## Create Azure Application Gateway 🏯

### Step 1: Navigate to Azure Portal

1. **Sign in** to the [Azure Portal](https://portal.azure.com/) with your Azure account.

### Step 2: Create Application Gateway

1. Click on **Create a resource** in the left-hand menu.
2. Search for **Application Gateway** and select it.
3. Click **Create**.
4. Configure the Application Gateway:
   - **Basics**:
     - Name: `AppGateway`
     - SKU: Standard (or choose as per your requirements)
     - Tier: Standard_v2 (or choose as per your requirements)
     - Virtual network: Select an existing virtual network or create a new one.
     - Subnet: Select or create a subnet within the virtual network.
   - **Frontends / Backends**: Configure as needed.
   - **Health probes, HTTP settings, etc.**: Configure according to your application requirements.
5. Click **Review + create**, then click **Create**.

## Configure Backend Pool and HTTP Settings ↩️

### Step 1: Add Backend Pool and HTTP Settings

1. Navigate to your newly created Application Gateway resource.
2. **Backend pools**:
   - Click on **Backend pools** under **Settings**.
   - Click **Add**.
   - Configure the backend pool:
     - Name: `BackendPool`
     - Add backend targets (VMs or IPs of backend servers).
   - Click **Add**.

3. **HTTP settings**:
   - Click on **HTTP settings** under **Settings**.
   - Click **Add**.
   - Configure HTTP settings:
     - Name: `HttpSettings`
     - Configure protocol, port, and other settings.
   - Click **Add**.

## Create and Test Listener and Routing Rules 🧾

### Step 1: Add Listener and Routing Rules

1. **Listeners**:
   - Click on **Listeners** under **Settings**.
   - Click **Add**.
   - Configure listener:
     - Name: `HttpListener`
     - Protocol: HTTP or HTTPS
     - Frontend IP: Select or create a public IP or private IP.
     - Port: 80 (or as needed)
   - Click **Add**.

2. **Routing rules**:
   - Click on **Routing rules** under **Settings**.
   - Click **Add**.
   - Configure routing rule:
     - Name: `HttpRoutingRule`
     - Listener: Select the previously created listener (`HttpListener`).
     - Backend pool: Select the previously created backend pool (`BackendPool`).
     - HTTP settings: Select the previously created HTTP settings (`HttpSettings`).
   - Click **Add**.

## Verify Application Gateway Configuration 🖥️

### Step 1: Test Application Gateway

1. **Access Application Gateway**:
   - Use the public IP or DNS name associated with the Application Gateway to access your application.

2. **Test Routing**:
   - Ensure traffic is routed correctly to backend servers.
   - Verify that HTTP requests are properly handled by backend servers.
