# Exploring and Testing Different Authentication Technologies in Azure 👨🏻‍🔬

## Prerequisites ✔️
- Azure Subscription
- Basic understanding of authentication and authorization concepts

## Step 1: Azure Active Directory (Azure AD) 🛠️

### Create an Azure AD Tenant 

1. **Navigate to the Azure Portal**:
   - Go to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account.

2. **Create a new Azure AD tenant**:
   - In the left-hand menu, select "Azure Active Directory".
   - Click on "Manage tenants".
   - Click on "+ Create".
   - Fill in the required details:
     - Organization name
     - Initial domain name
     - Country/Region
   - Click "Create".

### Add Users to Azure AD

1. **Navigate to your Azure AD tenant**:
   - In the left-hand menu, select "Azure Active Directory".
   - Select your newly created tenant.

2. **Add users**:
   - In the Azure AD blade, select "Users".
   - Click on "+ New user".
   - Fill in the required details:
     - User name
     - Name
     - Password settings
   - Click "Create".

### Assign Roles to Users

1. **Assign roles**:
   - In the Azure AD blade, select "Users".
   - Select the user you created.
   - Click on "Assigned roles".
   - Click "+ Add assignment".
   - Select a role (e.g., "User" or "Global administrator").
   - Click "Add".

### Test Azure AD Authentication

1. **Test user login**:
   - Sign out from the Azure Portal.
   - Go to the Azure Portal login page.
   - Sign in with the new user credentials you created.
   - Verify successful login.

## Step 2: Azure Multi-Factor Authentication (MFA) 🔒

### Enable MFA for Users

1. **Navigate to Azure AD**:
   - In the Azure AD blade, select "Security".
   - Select "Multi-Factor Authentication".

2. **Configure MFA**:
   - Click on "Additional cloud-based MFA settings".
   - Configure MFA settings as needed.

3. **Enable MFA for users**:
   - Go to the "Users" blade in Azure AD.
   - Select "Multi-Factor Authentication".
   - Enable MFA for specific users.

### Test MFA

1. **Test MFA login**:
   - Sign out from the Azure Portal.
   - Go to the Azure Portal login page.
   - Sign in with the user credentials you enabled MFA for.
   - Follow the MFA prompts (e.g., phone call, SMS, or app notification) to complete the login.

## Step 3: Azure AD B2C (Business to Consumer) 🏢

### Create an Azure AD B2C Tenant

1. **Navigate to Azure AD B2C**:
   - In the left-hand menu, select "Create a resource".
   - Search for "Azure AD B2C" and select it.
   - Click "Create".

2. **Configure Azure AD B2C**:
   - Fill in the required details:
     - Organization name
     - Initial domain name
     - Country/Region
   - Click "Create".

### Configure Identity Providers

1. **Navigate to Azure AD B2C**:
   - In the left-hand menu, select "Azure AD B2C".

2. **Add Identity Providers**:
   - In the Azure AD B2C blade, select "Identity providers".
   - Add identity providers (e.g., Google, Facebook) by following the prompts and providing necessary credentials.

### Create User Flows

1. **Create a user flow**:
   - In the Azure AD B2C blade, select "User flows".
   - Click on "+ New user flow".
   - Choose a user flow type (e.g., sign-up and sign-in).
   - Configure the user flow settings and click "Create".

### Test Azure AD B2C

1. **Run the user flow**:
   - Go to the "User flows" blade.
   - Select the user flow you created.
   - Click on "Run user flow".
   - Follow the prompts to test the user flow (e.g., sign-up and sign-in using a social identity provider).
