<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



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
 
<img src="https://imgur.com/64svWK6.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>


<h2>Installation Steps</h2>

<p>
<img src="https://imgur.com/DSOdVOz.png" height="50%" width="50%" alt="Disk Sanitization Steps"/> <img src="https://imgur.com/znPAIDJ.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 1 - Using Microsoft Azure you must create a Virtual Machine(VM) and paste the IP Address in Remote Desktop (Windows) or Microsoft Remote Desktop (Mac) in order to start up the VM.

Step 2 - Once you have your VM up and running you will need to open up the control panel and access programs in order to turn certain windows features on/off. You can right click start on the bottom left press run then type control to do this.
</p>
<br />

<p>
<img src="https://imgur.com/9CvX0E8.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://imgur.com/hkES8Tn.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
Step 3 - Now that windows features is open follow the images below and enable the following which is not enabled. 
<p>
<img src="https://imgur.com/eHtBsPn.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://imgur.com/Pa15RXY.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://imgur.com/eHtBsPn.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>
<br />
Step 4 - Type 127.0.0.1 into the internet browser search to double check IIS was correctly setup. You should get a screen like this. 
<p>
<img src="https://imgur.com/tDtrcZ8.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Steo 5 - You can now go into the installation files and download the Files required to begin osTicket setup. Once you reach PHP 7.3.8 you will extract all files in that download to C:\PHP
</p>
<img src="https://imgur.com/Vnqt7Hm.png" height="50%" width="50%" alt="Disk Sanitization Steps"/> <img src="https://imgur.com/4IJaAuZ.png" height="50%" width="50%" alt="Disk Sanitization Steps"/> <img src="https://imgur.com/cWuTgx2.png" height="50%" width="50%" alt="Disk Sanitization Steps"/> <img src="https://imgur.com/BYHJbep.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
