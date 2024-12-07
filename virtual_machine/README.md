This example shows how to create VM's in vnet using azure powershell scripts.

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

