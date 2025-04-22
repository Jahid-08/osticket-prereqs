<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This page outlines how I installed OsTicket and the steps I did to do so.<br />



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
 
This is the final screen before **Azure** creates the virtual machine we configured.  

To reach this point, navigate to [**www.portal.azure.com**](http://www.portal.azure.com).  

Log in, locate **"Virtual Machines"** (or use the search bar to find it), and click **"Create Virtual Machine"** to configure the necessary settings.  

Before Azure proceeds with creating the virtual machine, a **validation check** will appear. Once the validation passes, the virtual machine will be created.  
</p>
<br />

<p>
<img width="1604" alt="image" src="https://github.com/user-attachments/assets/83eaf344-6b11-4d66-bfad-bae256518b3b" />
</p>
<p>
 
After the virtual machine is created, you will be redirected to this screen, where you can view the created virtual machine along with details such as its **public IP address**, **status**, **location**, and **resource group**.  
</p>
<br />

<p>
<img width="302" alt="image" src="https://github.com/user-attachments/assets/fb1a93a1-1c73-4f19-a1a5-efd54bb188a3" />
</p>
<p>
Next, we will log in to the virtual machine from our PC.  

To begin, click the **Windows icon** or press it on your keyboard, then type **"RDP."**  

Select **"Remote Desktop Connection"** from the options.  

In the **"Computer"** field, enter the IP address of the machine you want to connect to. For this step, you will enter the IP address of the virtual machine we created.  
</p>
<br />

<p>
<img width="333" alt="image" src="https://github.com/user-attachments/assets/e708c0bb-263c-4e81-8880-70c756d88caa" />
<img width="287" alt="image" src="https://github.com/user-attachments/assets/20f49880-c9e7-4319-9eec-b4cbd02f5186" />
</p>
<p>
Then, you will connect to the virtual machine using the credentials you provided during its initial creation.  

After logging in, you will see a prompt with a yellow warning sign; click **"Yes"** to complete the login process and access the virtual machine. 
</p>
<br />

<p>
<img width="802" alt="image" src="https://github.com/user-attachments/assets/e9a11f05-2bc4-49cd-b298-5964cd033ace" />
</p>
<p>
 
After logging in, I downloaded the **osTicket installation files** from the provided link.  

Once downloaded, the files will appear in the **"Downloads"** folder on the virtual machine.  

[**osTicket-Installation-Files.zip**](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD)
</p>
<br />

<p>
<img width="696" alt="image" src="https://github.com/user-attachments/assets/5e89e717-9f1b-4b49-add8-27e4ba103063" />
</p>
<p>
 
 Drag the zip folder file from the **Downloads** section of the **File Explorer** onto the **Desktop**.  

Then, right-click the folder and select **"Extract All"**.  

After that, there should be two folders on the Desktop:  
1. The zip folder.  
2. The folder with all of the files we actually need.  

**Note:** You can delete the zip folder since we technically don't need it now; it's completely optional.  
</p>
<br />

<p>
<img width="596" alt="image" src="https://github.com/user-attachments/assets/e270e9b8-5516-4390-b83e-8705dbbd68cc" />
</p>
<p>
 
Next, we will install and enable **IIS (Internet Information Services)** in Windows with **CGI (Common Gateway Interface)**.  

**IIS** is a web server that allows the **Windows virtual machine** to host websites and web applications, including **osTicket**.  

**CGI** is a feature that enables **IIS** to run scripts, such as **PHP**, which is required for osTicket to function properly.  

Enabling CGI allows **PHP scripts** to be processed, making the help desk system interactive and dynamic.  
</p>
<br />

<p>
<img width="848" alt="image" src="https://github.com/user-attachments/assets/29c99bd7-a7a1-4199-be27-ca7bbac74c9b" />
</p>
<p>
 
Next, we’ll install **PHP Manager for IIS** from the **osTicket-Installation-Files** folder.  

**PHP Manager for IIS** is a handy tool that makes it easier to configure and manage PHP settings within **Internet Information Services (IIS)**.  

In this lab, installing PHP Manager lets us quickly register **PHP** with **IIS**, enable or disable extensions, and tweak settings without having to manually edit configuration files.  

This is important because **osTicket** runs on PHP, and **PHP Manager** helps streamline the setup and management process within IIS.  
  <br/>
  <br/>
  So once we click onto the folder on the desktop the file explorer will appear and we'll click "osTicket-Installation-Files" and navigate to PHP manager to install it to our virtual machine.
</p>
<br />

<p>
<img width="843" alt="image" src="https://github.com/user-attachments/assets/380c2696-8c45-4186-a82f-ea498dfc0eba" />
</p>
<p>
 
Next, we’re going to install the **Rewrite Module**.  

This helps **IIS** handle website links properly, making them look cleaner and easier to use. It also ensures that pages load correctly and that everything in **osTicket** works smoothly when you click around.  

Plus, it helps with things like **redirecting pages** and making the site easier to find on search engines.  
  <br/>
</p>
<br />

<p>
<img width="449" alt="image" src="https://github.com/user-attachments/assets/326de6fb-e8bf-4290-880b-8c38b064d5f8" />
</p>
<p>
 
Next, we will create the **PHP** directory in our **C drive (C:\)**.  

The reason we're doing this is to give **IIS** a dedicated location to find and run **PHP**, which is essential for **osTicket** to work.  

This helps keep things organized and ensures that **PHP scripts** run smoothly when the system needs them.  
</p>
<br />

<p>
<img width="520" alt="image" src="https://github.com/user-attachments/assets/03e83284-a464-4aee-83b6-5543e0398c8f" />
</p>
<p>
 
Next, we will open the **osTicket-Installation-Files** and unzip the **PHP** folder within the installation files into the **PHP** folder we just created in the **C drive**.  

The reason we're doing this is that **IIS** looks for PHP in this location when running osTicket. By placing the files there, we're ensuring PHP is properly installed and ready to process scripts.  

This setup helps **IIS** recognize and use PHP correctly, allowing osTicket to function as expected.  
</p>
<br />

<p>
<img width="446" alt="image" src="https://github.com/user-attachments/assets/2b0c3acf-0ae1-481f-a9ef-cf5761a7776a" />
<p>
 
Next, once again from the **osTicket-Installation-Files**, we're going to install the **VC_redist.x86** file.  

The **vcredist** file is like a missing puzzle piece that helps **PHP** and other programs run properly. Some parts of **PHP** and **MySQL** require special Microsoft files to function, and installing **vcredist** ensures those files are available so everything runs smoothly without errors.  
</p>
<br />

<p>
<img width="547" alt="image" src="https://github.com/user-attachments/assets/60944a38-d8f2-4dab-bed6-461e74c9435a" />
<img width="373" alt="image" src="https://github.com/user-attachments/assets/19349af4-caa4-4e6f-9e1f-d96eac764d72" />
<img width="374" alt="image" src="https://github.com/user-attachments/assets/47d477a9-f38e-462d-b84e-d87308d8d69e" />
<img width="371" alt="image" src="https://github.com/user-attachments/assets/265d6613-6dc5-4d3a-baad-b4d9c53d9a00" />

<p>
 
Next, we're going to install **MySQL** from the **osTicket-Installation-Files**.  

MySQL acts as the **database** that stores all the information for osTicket, such as user details, support tickets, and settings. Think of it as a **giant filing cabinet**, keeping everything organized so osTicket can quickly find and manage the data it needs.  

After installing MySQL, we’ll launch the **configuration wizard**, set up the **standard configuration**, and create our **root password** to log in and access the database.  
</p>
<br />

<p>
<<img width="724" alt="image" src="https://github.com/user-attachments/assets/b63ad8d1-3223-41a5-983c-9321a8acbd14" />
<img width="727" alt="image" src="https://github.com/user-attachments/assets/87583368-98c0-4918-958e-ac872a2c9af6" />
<img width="724" alt="image" src="https://github.com/user-attachments/assets/6e52bb00-f56a-4f61-9522-d46f3285caee" />
<p>
 
Next, we're going to open **IIS (Internet Information Services) Manager** as an administrator and register PHP within IIS.  

Registering PHP in IIS tells the web server where to find PHP so it can properly run PHP scripts. This is important because osTicket relies on PHP to function. Without registering PHP, IIS wouldn’t know how to process PHP files, and the help desk system wouldn’t work.  

Steps to register PHP in IIS:  
- Double-click **PHP Manager** → **Register a new PHP version**.  
- Provide the file path where we created the **PHP** folder in the **C drive**.  
- Click on **osticket-vm** (on the side panel).  
- Stop and restart the server for the changes to take effect.  
</p>
<br />

<p>
<<img width="737" alt="image" src="https://github.com/user-attachments/assets/7b91b559-db55-4770-af6b-25b8755f38e3" />
<img width="644" alt="image" src="https://github.com/user-attachments/assets/35bd9a9d-2bc4-474c-9fdf-955b24ac37de" />

<p>
 
Next, we’ll go back to the **osTicket-Installation-Files** folder, unzip the **osTicket-v1.15.8** folder, and extract it to its default location.  

A new window should open, showing two folders: **scripts** and **upload**.  

We’ll copy the **upload** folder to `C:\inetpub\wwwroot`, which places osTicket in IIS’s main web directory so it can be accessed through a web browser.  

After copying the folder, we’ll rename **upload** to **osTicket**.  

After these steps, we will reload IIS and stop and restart the server.  
</p>
<br />

<p>
 
<img width="775" alt="image" src="https://github.com/user-attachments/assets/e154583d-ad1d-420e-8cd7-109bb9acc378" />
<img width="887" alt="image" src="https://github.com/user-attachments/assets/45bd5358-37ff-476c-84df-724f739523d4" />
 
After that, we’ll go back into IIS and launch osTicket from there.  

In IIS, on the left panel, navigate to:  
- `osticket-vm` → `Sites` → `Default Web Site` → `osTicket`  

Click on **osTicket**, then look at the right panel under **"Manage Folder."**  

Find **"Browse** **:80 (http)"** and click it.  

A new window should pop up, launching osTicket.  

At this point, you’ll see a mix of **checkmarks** and **X-marks** on the setup page. Now, we’re going to resolve the **X-marks** to ensure osTicket is properly configured.  

</p>
<br />

<p>
<img width="612" alt="image" src="https://github.com/user-attachments/assets/4f709b95-d296-4f81-8379-aeb0cfb55585" />
<p>
 Enabling PHP Extensions in IIS for osTicket  

We're going to open IIS again and, under the **osTicket** connections, double-click **PHP Manager**.  

### Enabling Required PHP Extensions  

1. Under **PHP Extensions**, click **Enable or disable an extension**.  
2. Scroll through the list and enable the following extensions:  

   - `php_imap.dll`  
   - `php_intl.dll`  
   - `php_opcache.dll`  

### Why These Extensions Are Needed  

Enabling these extensions is essential because **PHP Manager** allows PHP to support additional features required for osTicket to function properly. These extensions provide:  

- **`php_imap.dll`** – Enables email handling for support ticket functionality.  
- **`php_intl.dll`** – Provides internationalization support for different languages and formats.  
- **`php_opcache.dll`** – Improves PHP performance by caching script operations.  

Without these, certain osTicket features may not work correctly or at all.  

### Final Step  

After enabling these extensions, go back to the osTicket browser and refresh the page. It should now reflect the correct setup above.  

</p>
<br />

<p>
<img width="563" alt="image" src="https://github.com/user-attachments/assets/c809229c-06e0-430d-890f-158903f2784d" />
<img width="566" alt="image" src="https://github.com/user-attachments/assets/3778d39e-bdfc-4e75-9199-b34c38de2921" />
<img width="263" alt="image" src="https://github.com/user-attachments/assets/2135c79e-8e2d-40bb-868a-3eeccb267282" />
</p>

<p>
Now, we’re going back to the osTicket files in File Explorer and navigating to the wwwroot folder. Open the osTicket folder, then go into the include folder. Inside, rename the "ost-sampleconfig.php" file to "ost-config.php".

Now, we’re going back to the osTicket files in File Explorer and navigating to the **wwwroot** folder. Open the **osTicket** folder, then go into the **include** folder. Inside, rename the file:

- Change `ost-sampleconfig.php` to `ost-config.php`.

### Assigning File Permissions

Next, we’ll assign the correct file permissions:

1. Right-click **ost-config.php** → select **Properties** → go to the **Security** tab → click **Advanced**.
2. Click **Disable inheritance**, then in the window that appears, select **Remove all inherited permissions from this object**.
3. Click **Add** → select **Select a Principal**.
4. In the third box, type **everyone**, then click **Check Names** and press **OK**.
5. Check the **Full control** box and click **OK**.
6. On the final two screens, make sure to click **Apply** and then **OK** to save the changes.

</p>
<br />

<p>
 <img width="613" alt="image" src="https://github.com/user-attachments/assets/374e4c8a-de7c-4765-978a-c0e0a992355b" />
<img width="551" alt="image" src="https://github.com/user-attachments/assets/a7b0bb66-e421-4cd5-85c6-003706ae090b" />
 <img width="507" alt="image" src="https://github.com/user-attachments/assets/08f207cb-f451-4c6f-8148-9ebda743075c" />
 <img width="605" alt="image" src="https://github.com/user-attachments/assets/8623ff32-8d7c-47e7-84db-dc87d603fe7d" />
 <img width="617" alt="image" src="https://github.com/user-attachments/assets/499d05b0-569f-402e-b88e-fafb87a20c02" />
 <img width="693" alt="image" src="https://github.com/user-attachments/assets/8387095f-5eba-4d51-bb19-446c93e63f51" />
</p>

<p>
 
Once we get there, we will go back to the **osTicket installation files** and install **"HeidiSQL"**.  

This will be used as a graphical interface to connect to the **MySQL server** and create the **osTicket database**.  

This database is where **osTicket** will store all of its data, such as tickets, users, configurations, etc. The **osTicket installation process** requires that this database exists before it can proceed.  

After we install **"HeidiSQL"**, we'll see this window. We're going to make a connection to our database and then set up a database that **osTicket** can use.  

We will click **"New"** in the bottom left-hand corner, and on the right-hand side in **"User"** and **"Password"**, we'll enter **"root"** in both fields because this is the username and password we created for our database when we set up MySQL.  

After that, we will be prompted with a new window where we will create the database named **osTicket**. To do that, we'll right-click **"Unnamed"** → **Create New** → **Database**, and name it **"osTicket"**.  

Then click **"Open"**, and we will go back to the **osTicket** setup browser to fill in those **"Database Settings"** details.  

Now, we will fill those fields with the **"osTicket"** database we just created in HeidiSQL, along with the username and password set as **"root"**, and click **Install Now**. You should then see a **Congratulations** screen. If we go back to **"HeidiSQL"** and go back to the **osTicket** database we can see the tables of data in which we will use populate.
</p>
<br />

<p>
<img width="502" alt="image" src="https://github.com/user-attachments/assets/b991a1d1-dd42-4cad-8843-c0a4c4e3abe3" />
 <img width="760" alt="image" src="https://github.com/user-attachments/assets/f4bc4791-ed07-4c6c-b8cf-9113235383f9" />
<img width="649" alt="image" src="https://github.com/user-attachments/assets/aad6624a-501c-42c0-a273-ab71791ec51f" />
</p>
<p>
 
So this is the installation process of **osTicket** on our virtual machine. After completing this process, there will be two links we will use to log in to **osTicket**:

1. **Help Desk Staff Login**  
   This link is for the people running the help desk. They use this link to log in, see all the tickets, respond to customers, and manage the whole system.  
   [http://localhost/osTicket/scp/login.php](http://localhost/osTicket/scp/login.php)

2. **Customer Support Portal**  
   This link is for users who need help desk support. It serves as the main entrance for customers to submit tickets, check the status of their issues, or find answers to common questions.  
   [http://localhost/osTicket/](http://localhost/osTicket/)
</p>
<br />



