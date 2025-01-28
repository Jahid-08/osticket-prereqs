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

<p>
<img width="333" alt="image" src="https://github.com/user-attachments/assets/e708c0bb-263c-4e81-8880-70c756d88caa" />
<img width="287" alt="image" src="https://github.com/user-attachments/assets/20f49880-c9e7-4319-9eec-b4cbd02f5186" />
</p>
<p>
Then you will connect to the virtual machine with the credentials that you would have provided during the initial creation of the virtual machine. After you login you will be prompted with another prompt(yellow warning sign) click yes to officially login to the virtual machine.
</p>
<br />

<p>
<img width="802" alt="image" src="https://github.com/user-attachments/assets/e9a11f05-2bc4-49cd-b298-5964cd033ace" />
</p>
<p>
After we get logged in I downloaded the osTicket intallation files provided from this link. Once you download the files it will appear in the dowloads folder in the virtual machine. [osTicket-Installation-Files.zip](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD)
</p>
<br />

<p>
<img width="696" alt="image" src="https://github.com/user-attachments/assets/5e89e717-9f1b-4b49-add8-27e4ba103063" />
</p>
<p>
  Drag the zip folder file from the downloads section of the file explorer onto the desktop. Then right click the folder and select "Extract All". Then after that there should be two folders on the desktop, the zip folder, and the the folder with all of the files we actually need. 
  <br/>
 <strong>Note: You can delete the zip folder since we technically don't need it now, it's completely optional.</strong> 
</p>
<br />
