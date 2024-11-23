Azure Active directory Lab

Setup Domain Controller in Azure
—
Create a Resource Group
Create a Virtual Network and Subnet
Create the Domain Controller VM (Windows Server 2022) named “DC-1”
Username: labuser
Password: Cyberlab123!
After VM is created, set Domain Controller’s NIC Private IP address to be static
Log into the VM and disable the Windows Firewall (for testing connectivity)

<img width="402" alt="image" src="https://github.com/user-attachments/assets/537ce34c-380e-4a6c-83f2-b82567da5629"> 

Log into the VM and disable the Windows Firewall

Go to <img width="286" alt="image" src="https://github.com/user-attachments/assets/8df0caeb-46ca-4e94-b427-21fea1cad505">

And then go to Windows Defender Firewall with Advanced Security. Next, go to Windows defender Firewall Properties

<img width="425" alt="image" src="https://github.com/user-attachments/assets/a4b9ac69-e65f-4078-b9f8-bd004d3bcecb">

In the Windows Defender Firewall with Advanced Security on Local Computer section the tabs Domain Profile, Private, 
and public make sure the Firewall state tabs are off to disable the firewall 

<img width="237" alt="image" src="https://github.com/user-attachments/assets/2e2cd5f4-ba88-4fbe-9b4e-75db5ac34e46">

Setup Client-1 in Azure:

Create the Client VM (Windows 10) named “Client-1”
Attach it to the same region and Virtual Network as DC-1
After VM is created, set Client-1’s DNS settings to DC-1’s Private IP address
1. Go to client-1 VM

 <img width="345" alt="image" src="https://github.com/user-attachments/assets/2af484ad-984f-42ab-888a-cc7bc2beb152">

2.Go to Network settings

<img width="131" alt="image" src="https://github.com/user-attachments/assets/4ebe9341-d0a4-4430-867a-fedcf48ad8e1">















