
# LAB-VIRTUAL NETWORK CREATION:

* OVERVIEW:
A VNet enables many types of Azure resources, such as Azure Virtual Machines (VMs), to securely communicate with each other, the internet, and on-premises networks.


* Step-by-Step Implementation Guide
Step 1: Sign in to the Azure Portal
1) Open your web browser and navigate to https://portal.azure.com.
2) Log in using your Azure credentials

Step 2: Navigate to Virtual Networks
1) In the top search bar of the Azure portal, type Virtual networks.
2) Select Virtual networks under the Services category or Click on Create resoource.

![image alt](https://github.com/skaushik258/AZ-Labs/blob/859f16fdc1a53a1bc4e4071db8ec386699313c13/02-Virtual%20Network(VNET)/screenshotsCreate%20resource.PNG).

Step 3: Configure Basic Settings
1) On the Virtual Networks dashboard, click on the + Create button.
2) Under the Basics tab, fill in the following project and instance details:
-> Subscription: Selected My Azure subscription.
-> Resource Group: Select an existing resource group and Mine is already selected. 
-> Name:VNET-Prod.
-> Region: Central India.

   ![image alt](https://github.com/skaushik258/AZ-Labs/blob/948d157e72ed54918fea070b740eb9f37c864e47/02-Virtual%20Network(VNET)/VNET_NAME.PNG)

Step 4: Configure Security Defaults
1) Review the security options (such as Azure Bastion, Firewall, or DDoS protection). For this basic lab, leave them at their defaults or select None if not required.
2) Click Next: IP Addresses >.

Step 5: Define Address Space and Subnets
1) Address Space: Define the IPv4 address space for the VNet (10.0.0.0/16).
2) Subnet address range: 10.0.1.0/24 (leaving 256 total addresses, with Azure reserving 5)
3) Subnets: Click on the default subnet and Changed name to VM_SUB.

[ Internet ] 
     │
     ▼
[ VNet: vnet-prod-eastus (10.0.0.0/16) ]
     ├── [ Subnet: frontend (10.0.1.0/24) ] (WEB_SUB)
     └── [ Subnet: backend (10.0.2.0/24) ] (DB_SUB)

![image alt]()

4) Click Save.
Click Next: Tags > (optional) and then Next: Review + create >.

Step 6: Review and Create
1) Azure will run an automated validation check. Ensure you see the green "Validation passed" message at the top.
2) Review your selected configurations (Address space, Subnets, Region, Subscription).
3) Click Create to kick off the deployment.

![image alt]()

Step 7: Verify Deployment
1) Wait a moment for the deployment notification to show "Deployment succeeded".
2) Click Go to resource to open your newly created Virtual Network overview page and review its properties.

![image alt]()

