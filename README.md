<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial provides a detailed guide for setting up the open-source help desk ticketing system, osTicket, covering prerequisites and installation steps.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- **Installation Files** (https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)
   -  PHP Manager for IIS (https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view?usp=share_link)
   - Rewrite Module (https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link)
   - PHP 7.3.8 (https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link)
   - VC_Redist.86 (https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link)
   - MySQL (https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link)
   - HeidiSQL (https://docs.google.com/document/d/1WovrX2DaS9xkfaSr4LXyB4YnnWpXIgPCMMbbfgHmGVw/edit)
 
<img src="https://i.imgur.com/SxttUZX.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>


<h2>Installation Steps</h2>

<p>
<img src="https://imgur.com/DSOdVOz.png" height="50%" width="50%" alt="Disk Sanitization Steps"/> <img src="https://imgur.com/znPAIDJ.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 1: Create a Virtual Machine (VM) using Microsoft Azure. Retrieve the IP Address and utilize Remote Desktop (Windows) or Microsoft Remote Desktop (Mac) to initiate the VM.

Step 2: After launching your VM, access the control panel to manage Windows features. Right-click on the Start menu, select "Run," and type "control" to open the control panel. From there, navigate to Programs to enable or disable specific Windows features as needed.
</p>
<br />
<p>
<img src="https://imgur.com/9CvX0E8.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://imgur.com/hkES8Tn.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>

Step 3: With the Windows Features window open, refer to the provided images to identify and enable the required features that are currently disabled. 
<p>
<img src="https://imgur.com/eHtBsPn.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://imgur.com/Pa15RXY.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://imgur.com/eHtBsPn.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>
<br />

Step 4: Verify the correct setup of Internet Information Services (IIS) by typing "127.0.0.1" into the internet browser's address bar. Confirm the expected screen appearance, resembling the image provided.
<p>
<img src="https://i.imgur.com/ZJfSWTu.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>

Step 5: Proceed to download the necessary files from the installation package for osTicket. Upon reaching the file PHP 7.3.8 version, extract all files from the download and place them in the directory "C:\PHP".
</p>
<img src="https://i.imgur.com/JpMu75i.png" height="50%" width="50%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/afdC14p.png" height="60%" width="60%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/KlCeOOX.png" height="60%" width="60%" alt="Disk Sanitization Steps"/> <img src="https://imgur.com/BYHJbep.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />

Step 6: Complete the download of the remaining files, excluding osTicket and HeidiSQL. During the MySQL setup process, opt for a typical setup and adhere to standard configurations in the Wizard configuration (post-installation). Ensure to note down the username and password for future steps.
<p>
<img src="https://i.imgur.com/aTGrfpf.png" height="60%" width="60%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/mR62BrZ.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>

Step 7: Launch and execute IIS as an administrator, then access PHP Manager. Within PHP Manager, proceed to register PHP from within IIS according to the provided instructions. After completion, reload IIS to apply the changes.
<p>
<img src="https://i.imgur.com/bvU22b0.png" height="50%" width="50%" alt="Disk Sanitization Steps"/> <img src="https://imgur.com/68pYzyt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

Step 8: Upon completing the osTicket file download, open the file and extract the contents of the "upload" folder into "C:\inetpub\wwwroot". 
</p>
<br />

<p>
 <img src="https://imgur.com/KqyEchz.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>

Step 9: Navigate to "This PC" > "Windows (C:)" > "inetpub" > "wwwroot". Locate the "upload" folder and rename it to "osTicket".
<p>
<img src="https://imgur.com/YR00J4S.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<br />

Step 10: In IIS, navigate through the following sequence: IIS > Sites > Default Web Site > osTicket. Access PHP Manager from within osTicket. Scroll down to the "PHP Manager Enable or Disable Extension" section. Enable the extensions: php_imap.dll, php_intl.dll, php_opcache.dll
<p>
<img src="https://i.imgur.com/zb9cB8E.png" width="80%" alt="Disk Sanitization Steps"/> 
</p>
<p>
Step 11: Proceed to the following directory: "This PC" > "Windows (C:)" > "inetpub" > "wwwroot" > "osTicket" > "include". Rename the "ost-sampleconfig" folder to "ost-config". Then, right-click on "ost-config", open Properties, navigate to Security, and choose Advanced. Disable Inheritance and remove all permissions.

Step 12: Under the Security tab in the Properties window of "ost-config", click on Add. Type "Everyone" and select Check Names. Afterward, grant "Read" and "Execute" permissions to "Everyone".
</p>
<img src="https://imgur.com/Fyqq3Ud.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <img src="https://imgur.com/xpk1lXx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/MYQYFfm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
</p>

Step 13: Navigate back to IIS and locate "Sites" > "Default Web Site" > "osTicket". On the right-hand side, click on "Browse *:80". This action will display the screen depicted below. Proceed with the osTicket setup as prompted.
<p>

<img src="https://i.imgur.com/tbCAJlN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<br />

Step 14: The final file to download is HeidiSQL. Create a username and password during setup, ensuring to remember or note down the information. After installation, open HeidiSQL, connect to the session, and proceed to create a new database titled "osTicket".
<p>
<img src="https://imgur.com/vIWDDtj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/UQLbaG5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Step 15: Input the database information obtained from HeidiSQL into the designated fields on the osTicket setup page. Click "Install", and upon successful completion, the final page should be displayed.
</p>
<img src="https://imgur.com/1mMMtB2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/iDwas1j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
</p>

Cleanup (Optional): Navigate to "This PC" > "Windows (C:)" > "inetpub" > "wwwroot" > "osTicket". Delete the "setup" folder if no longer needed. Additionally, return to the "ost-config" file, open its properties, and enable full control permissions as necessary.
<p>
<img src="https://imgur.com/WcVQBe5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <img src="https://imgur.com/0NXwFMW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
</p>

Step 16: Access the Agent login page using the previously set up information at http://localhost/osTicket/scp/login.php. For end users, utilize the osTicket URL http://localhost/osTicket/.

Step 17: Log in to osTicket!
<p>
<img src="https://imgur.com/BL4zEGX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <img src="https://imgur.com/IayoADD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
</p>
