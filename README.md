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
This is the final screen before Azure creates the virtual machine we configured. To reach this point, navigate to www.portal.azure.com. Log in, locate "Virtual Machines" (or use the search bar to find it), and click "Create Virtual Machine" to configure the necessary settings. Before Azure proceeds with creating the virtual machine, a validation check will appear. Once the validation passes, the virtual machine will be created.
</p>
<br />

<p>
<img width="1604" alt="image" src="https://github.com/user-attachments/assets/83eaf344-6b11-4d66-bfad-bae256518b3b" />
</p>
<p>
After the virtual machine is created, you will be redirected to this screen, where you can view the created virtual machine along with details such as its public IP address, status, location, and resource group.
</p>
<br />

<p>
<img width="302" alt="image" src="https://github.com/user-attachments/assets/fb1a93a1-1c73-4f19-a1a5-efd54bb188a3" />
</p>
<p>
Next, we will log in to the virtual machine from our PC. To begin, click the Windows icon or press it on your keyboard, then type "RDP." Select "Remote Desktop Connection" from the options. In the "Computer" field, enter the IP address of the machine you want to connect to. For this step, you will enter the IP address of the virtual machine we created.
</p>
<br />

<p>
<img width="333" alt="image" src="https://github.com/user-attachments/assets/e708c0bb-263c-4e81-8880-70c756d88caa" />
<img width="287" alt="image" src="https://github.com/user-attachments/assets/20f49880-c9e7-4319-9eec-b4cbd02f5186" />
</p>
<p>
Then, you will connect to the virtual machine using the credentials you provided during its initial creation. After logging in, you will see a prompt with a yellow warning sign; click "Yes" to complete the login process and access the virtual machine.
</p>
<br />

<p>
<img width="802" alt="image" src="https://github.com/user-attachments/assets/e9a11f05-2bc4-49cd-b298-5964cd033ace" />
</p>
<p>
After logging in, I downloaded the osTicket installation files from the provided link. Once downloaded, the files will appear in the "Downloads" folder on the virtual machine. <a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD">osTicket-Installation-Files.zip</a>
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

<p>
<img width="596" alt="image" src="https://github.com/user-attachments/assets/e270e9b8-5516-4390-b83e-8705dbbd68cc" />
</p>
<p>
Next, we will install and enable IIS (Internet Information Services) in Windows with CGI (Common Gateway Interface). IIS is a web server that allows the Windows virtual machine to host websites and web applications, including osTicket. CGI is a feature that enables IIS to run scripts, such as PHP, which is required for osTicket to function properly. Enabling CGI allows PHP scripts to be processed, making the help desk system interactive and dynamic.
</p>
<br />

<p>
<img width="596" alt="image" src="https://github.com/user-attachments/assets/e270e9b8-5516-4390-b83e-8705dbbd68cc" />
</p>
<p>
Next, we’ll install PHP Manager for IIS from the "osTicket-Installation-Files" folder. PHP Manager for IIS is a handy tool that makes it easier to configure and manage PHP settings within Internet Information Services (IIS). In this lab, installing PHP Manager lets us quickly register PHP with IIS, enable or disable extensions, and tweak settings without having to edit configuration files manually. This is important because osTicket runs on PHP, and PHP Manager helps streamline the setup and management process within IIS.
</p>
<br />
