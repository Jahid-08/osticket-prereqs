<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This page outlines how I installed OsTicket and the steps I did to do so.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create Virtual Machines in Azure
- Log into virtual machine
- Download OsTicket installation files
- Install / Enable IIS in Windows WITH CGI

<h2>Installation Steps</h2>

<p>
<img width="782" alt="image" src="https://github.com/user-attachments/assets/0c4807c9-614c-4f6e-a8a3-b7bbcf0795b9" />
</p>
<p>
Here is the final screen before azure creates the virutal machine we configured. To get here you go to "www.portal.azure.com" There you will login and find "Virtual Machines" or type it in the search bar. Then you click "create" virtual machine and configure the settings. Before Azure creates the virtual machine this validation check will appear. Once it passes the virtual machine will create.
</p>
<br />

<p>
<img width="1604" alt="image" src="https://github.com/user-attachments/assets/83eaf344-6b11-4d66-bfad-bae256518b3b" />
</p>
<p>
After the virtual machine is created you'll be redirected back to this screen to where you can see the created virtual machine and some details about it such as it's Public IP address, status, location, and resource group.
</p>
<br />

<p>
<img width="302" alt="image" src="https://github.com/user-attachments/assets/fb1a93a1-1c73-4f19-a1a5-efd54bb188a3" />
</p>
<p>
Then we will login to the virtual machine from our PC. To get here you click the windows icon, or press it on the keyboard and type "RDP". There you will see the ability to select "Remote Desktop Connection". Where it says "Computer", you will type the IP address of the computer of the computer you want to connect to. Here you would enter the IP address of the virtual machine we created.
</p>
<br />
