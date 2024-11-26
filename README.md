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

3. In network settings, go to the NIC/IP configuration. It should say (client-1178-1 (primary) / ipconfig1

![image](https://github.com/user-attachments/assets/069d188c-1ba8-4e4b-b48a-9a3f05663ede)

In the NIC setting on the left side of the display, you will go to DNS servers settings. In the DNS server settings, go to DNS servers customs and add the private Ip address. 
Remember your private Ip address is in your Client-1’s network settings. HIT SAVE!

![image](https://github.com/user-attachments/assets/dc8f537d-df82-4182-843f-27aa425590a2)

From the azure portal, restart the client-1 VM. After the restart, log back into client-1 VM. Go to powershell and ping your DC-1 private IP address. 
To ensure a success ping type in ipconfig /all. The output should show DC-1 private Ip address. 

![image](https://github.com/user-attachments/assets/437c1a4b-a802-4a73-9ba0-a595c6d94af5)
![image](https://github.com/user-attachments/assets/1d283e19-e385-44cb-8269-10f1326fecca)


























