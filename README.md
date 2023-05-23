# Azure VPN Lab

This creates an onprem vnet with vpn gateway connected to a hub vnet vpn gateway and a spoke vnet attached to the hub. VM's are created in all 3 vnets.
You'll be prompted for the resource group name, location where you want the resources created, your public ip, and username and password to use for the VM's. NSG's are placed on the default subnets of each vnet allowing RDP access from your public ip. This also creates a logic app that will delete the resource group in 24hrs.
The topology will look something like this:

![vpnlab](https://user-images.githubusercontent.com/128983862/231853551-e8d07cc3-146b-4631-8f40-fa77a807fbcb.png)


You can run Terraform right from the Azure cloud shell by cloning this git repository with "git clone https://github.com/quiveringbacon/AzureVPNLab.git ./terraform".

Then, "cd terraform" then, "terraform init" and finally "terraform apply -auto-approve" to deploy.
