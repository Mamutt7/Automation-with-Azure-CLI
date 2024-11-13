<p align="center">
  <img src="https://github.com/user-attachments/assets/dcd0ebb3-1a49-4d9f-b86b-8ebea9fbd561" alt="Azure CLI Logo" width="200"/>
</p>

# Automation with Azure CLI

This project demonstrates how to automate the deployment of a Virtual Machine (VM) in Azure using Azure CLI and Bash scripting. The process involves creating essential resources such as a resource group, virtual network, and network security group, and automating VM size selection based on availability.

---

## Steps and Screenshots

### Step 1: Create a Resource Group
![image](https://github.com/user-attachments/assets/1861bf0f-5d87-4b9e-98b4-90a4668effbe)

In this step, I created a resource group using the Azure CLI in Cloud Shell. This resource group will hold all resources for the automation project, keeping everything organized and manageable.

### Step 2: Set Up Virtual Network and Subnet
![image](https://github.com/user-attachments/assets/2b2231cb-bcb2-4515-8fd7-fedcbf2564da)

In this step, I created a virtual network and subnet within my resource group using Azure CLI. This network setup provides the foundational structure for our virtual machine, allowing us to control IP ranges and manage resources within a secure network.

### Step 3: Create a Network Security Group and SSH Rule
![image](https://github.com/user-attachments/assets/6e0f9141-73b7-4c15-bac7-a8013e64b743)

In this step, I created a Network Security Group (NSG) with a rule allowing SSH access. The NSG secures network traffic to the VM, and this SSH rule enables safe access while keeping other ports closed.

### Step 4: Automate VM Size Selection and Deployment
![image](https://github.com/user-attachments/assets/5e910b61-dccc-4e0f-8072-22c9ce046b99)

In this step, I ran a script that checks for available VM sizes in the `centralus` region. The script automatically attempts each size until it finds one that is deployable, simplifying resource management.

### Step 5: Successful VM Deployment
![image](https://github.com/user-attachments/assets/b5c7a52b-5c65-446f-9bdc-5cfa0424d50a)

The script successfully deployed a VM using the first available size, `Standard_B1s`, in the `centralus` region. Automating the selection of VM sizes allows for efficient and reliable VM deployment, especially in regions with capacity constraints.

---

## Key Commands Used
- `az group create`: Creates a resource group to hold Azure resources.
- `az network vnet create`: Sets up a virtual network and subnet.
- `az network nsg create` and `az network nsg rule create`: Creates a Network Security Group and configures security rules.
- `az vm create`: Deploys a VM with specified parameters, automating the selection of available sizes.

## What I Learned
This project enhanced my skills in using Azure CLI for automated cloud resource management, handling capacity constraints programmatically, and deploying secure, efficient cloud infrastructure.

---

## Additional Information
To run this automation project, you can find the full script in this repository, and feel free to adapt it to other regions or configurations as needed.
