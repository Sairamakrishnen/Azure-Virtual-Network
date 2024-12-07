This example shows how to create VM's in vnet and establish connection between two VM's via bastion.

## Assuming the following steps are created:
1. [Deploy a vnet into a resource group and add a subnet within vnet.](VNet/README.md)
2. [Create a Bastion subnet and bastion host resource.](bastion/README.md)

# Deploy VM's in the VNet

Create VM's following below steps:

* Set Credentials for VM using **Get-Credential** cmd.
* Create Network Interface for VM using **New-AzNetworkInterface** cmd.
* Configure VM using **New-AzVMConfig** cmd by setting VM size, OS, Soure Image and adding the NIC.
* Create VM using **New-AzVM** cmd.

**Snapshots from cloudshell:**

For the first VM **(vm-1)**

![vm-1_1](https://github.com/user-attachments/assets/203f2fc0-faab-4cdf-92ea-49b16ab67b50)
![vm-1_2](https://github.com/user-attachments/assets/671b3ee8-33c4-4048-be0f-127c37fc2e1d)
![vm-1_3](https://github.com/user-attachments/assets/4690c5b5-00b3-48b2-9424-79223dd8ab97)

For the second VM **(vm-2)**

![vm-2_1](https://github.com/user-attachments/assets/9fc7fc8e-a3e0-4e02-9b83-fd7c6beca773)
![vm-2_2](https://github.com/user-attachments/assets/08bcdb31-ba30-4441-bd2d-788cd9a64bc4)

## Connect to vm-1

* In Azure portal, On the **vm-1** overview tab, select connect via bastion entering credentials of vm-1.
* In the bash prompt of vm-1, ping vm-2 to verify connection with vm-1.

From below snapshot of vm-1 bash prompt we can observe the ping was successful and all packets were delivered to vm-2.

![ping vm-1 - vm-2](https://github.com/user-attachments/assets/c915bbaa-22ec-4f72-b35d-a822488d77d3)

* On vm-2 overview tab, select connect via Bastion entering the credentials of vm-2.
* In the bash prompt of vm-2, ping vm-1 to verify connection with vm-2.

 From below snapshot of vm-2 bash prompt we can observe the ping was successful and all packets were delivered to vm-1.

![ping vm-2 - vm-1](https://github.com/user-attachments/assets/ee10d80b-2124-4d04-afef-233323a615d8)
  
## Cleanup

Remove the resource group and all its resources using **Remove-AzResourceGroup** cmd.

![remove rg-1](https://github.com/user-attachments/assets/7bc1f427-688d-48ed-8f5f-44363f482528)

