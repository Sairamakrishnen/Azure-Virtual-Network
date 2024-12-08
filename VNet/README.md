This example shows how to create a vnet using azure powershell scripts.

## Create a resource group 

* Open Cloudshell module in Azure portal.
* Create a resource group using **New-AzResourceGroup** cmdlet.

![create rg-1](https://github.com/user-attachments/assets/d0e3cd8a-6077-4394-a478-1a285036841d)

## Provision a Virtual Network

* Create a vnet using **New-AzVirtualNetwork** and add a subnet to it using **Add-AzVirtualNetworkSubnetConfig.** Update vnet using **Set-AzVirtualNetwork** cmdlet.

![vnet-1 subnet-1](https://github.com/user-attachments/assets/3f9f04f1-f39e-4b1f-9d89-ab9e8ff616ca)
