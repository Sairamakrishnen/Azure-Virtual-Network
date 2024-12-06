This example shows how to create a bastion host resource in vnet using azure cloudshell.

## Assuming the following steps are created:
1. Create a resource group.
2. Create a vnet.
3. Create a subnet within vnet.

# Create a Bastion subnet and bastion host resource


* To create a Subnet named AzureBastionSubnet exclusively for bastion resources with AddressPrefix '10.0.1.0/26' using Add-AzVirtualNetworkSubnetConfig cmdlet. Update vnet using Set-AzVirtualNetwork.

![bastion subnet](https://github.com/user-attachments/assets/033e26df-3a04-467b-bd21-199954482a1a)

* For bastion host, Create public ip address in vnet using New-AzPublicIpAddress cmdlet.
  
![public ip](https://github.com/user-attachments/assets/eb908b1a-798b-435a-a720-0f5ce866a4c8)

* Create a bastion host in vnet using New-AzBastion cmdlet.

![bastion host](https://github.com/user-attachments/assets/67f090c8-1bff-4db1-bda3-a26744a75a03)
