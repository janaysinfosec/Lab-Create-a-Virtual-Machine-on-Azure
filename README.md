# Lab: Create a Virtual Machine on Azure
This lab guides me through creating a Virtual Machine (VM) on Microsoft Azure, configuring it, and connecting to it via SSH. It helped me understand core Azure services and how to manage cloud resources.
# Prerequisites
* An active Azure subscription.
* Access to the Azure Portal https://portal.azure.com/

# Step-by-Step Process
1. Create a Resource Group

* Logged into the Azure Portal.
* Searched for Resource Groups in the search bar and clicked + Create.
* Named my resource group MyLabRG and selected the Central US region (to match my preferences).
* Clicked Review + Create and then Create to set it up.

2. Create a Virtual Machine

* Navigated to Virtual Machines from the portal search.
* Clicked + Create and chose Azure Virtual Machine.
* Configured the VM with the following settings:
    * Subscription: My active Azure subscription.
    * Resource Group: Selected MyLabRG.
    * Virtual Machine Name: MyLabVM.
    * Region: Central US.
    * Image: Selected Ubuntu 20.04 LTS for a free, Linux-based server.
    * Size: Selected Standard_B1s, which is sufficient for basic testing and is free tier eligible.
    * Administrator Account: Set my username (e.g., azureuser) and a secure password.
* Left other options as default and proceeded to the next steps.

3. Configure Disks
   
* Kept the default OS disk settings and clicked Next: Networking.

4. Set Up Networking

* Allowed Azure to create a new Virtual Network and subnet automatically.
* Set the Public IP to enabled by creating a new public IP resource named 'enabled'.
* For inbound port rules, selected SSH (22) to enable secure remote access.
* Reviewed and created the VM, waiting a few minutes for deployment.

5. Connecting to the VM

* After deployment, I found the VM’s public IP address in the overview tab (e.g., 20.221.58.242).
* Opened a terminal on my desktop (PowerShell on Windows).
* Connected via SSH using the command:  ssh azureuser@20.221.58.242
* Entered my password (note: the terminal does not show characters while typing).
* Successfully logged in and saw the “Welcome to Ubuntu” message.

Cleanup

To avoid charges, I deleted my resource group MyLabRG from the portal by selecting Resource Groups and clicking Delete Resource Group.

Summary

This provided me with practical experience in deploying a Linux VM on Azure, setting up network access, and securely connecting using SSH. It helped me understand cloud VM provisioning, resource management, and basic Linux server administration.

![MyLabVM5](https://github.com/user-attachments/assets/f4593b77-05da-473b-8462-5ac935b3f16f)
![MyLabVM4](https://github.com/user-attachments/assets/e66f7039-7bf6-4f32-85d3-d436478a9704)
![MyLabVM3](https://github.com/user-attachments/assets/19ef4b6e-2022-4dd2-8acf-98716bf42364)
![MyLabVM2](https://github.com/user-attachments/assets/fd05dc79-6bde-4194-acb4-249974bb6d73)
![MyLabVM1](https://github.com/user-attachments/assets/d0137355-a5e0-403b-ab79-d7ef4ee5bd12)

