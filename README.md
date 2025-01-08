# Configure-Azure-VN-Peering
Creating a regional and global virtual network.

Scenario:
An organization has three data centers connected with a mesh wide-area network. As the Azure administrator for the organization,
the task here is to implement the on-premises infrastructure in Azure.
1. The organization has two offices, New York and Boston, both in the same region (north-eastern US)
2. There is another office in Seattle, another region (NorthWest US)
3. All the offices need to be networked together to share information.


Architectural diagram here:![image](https://github.com/user-attachments/assets/25790ade-cd8f-4ba9-b6da-4cb121e8d03c)


Moving on to the steps required to complete this project,
step 1 involves using PowerShell to deploy three virtual machines with a pre-existing template in different regions and virtual networks. 
This is done using the cloud shell option on the Azure portal. 

The deployment details : 
![image](https://github.com/user-attachments/assets/160db9e8-a190-411e-a9cf-aec8fa9f6396)
![image](https://github.com/user-attachments/assets/21feb46a-77f2-43bc-9aea-c47ef21011f5)
NB: Make sure to create the resource group on the portal with the exact name provided as the $rgname parameter before deployment. 

Step 2: Configure Global and Regional Virtual Network Peering Between Virtual Networks Deployed In Step 1.
Peering works both ways, for instance, when a network az-104-vnet0 is paired with az-104-vnet1, for a successful connection, az-104-vnet1 has to be paired back with az-104-vnet0.
The same goes for trying to initiate a global peering connection. 

Step 3 involves testing connectivity between the pairs. 
- Test connectivity via a virtual machine between regional network pairs
- Test connectivity between global network pairs. 


