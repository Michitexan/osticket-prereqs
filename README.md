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

<h2>Overview of Order of Operations</h2>

- Enable Internet Information Services (IIS)
- Installing PHP Manager 
- Installing MySequel
- Installing OS Ticket
- Cleanup

<h2>Installation Steps</h2>

<p>
  While osTicket is a very powerful tool, there are some supporting and interdependant programs that are required to use this tool to it's full potential. In this guide, you will establish the ground floor for your own ticketing system.

<h2>Enabling Internet Information Services (IIS) </h2>

  The first step is to Enable Internet Information Sevices, or IIS, in your computer. For Windows systems this is a simple process, but very important. Since osTicket requires access to other computers in the network, access will have to manually be granted. To so this, Open up ControlPanel, select Programs, and under "Programs and Features", select "Turn Windows Features On or Off"
</p>
<p>
<img src="https://i.imgur.com/9WCNWgZ.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Scroll down the list until you find "Internet Information Services". Click the box, so that it is filled with a black square. THen expand the dropdown menu to show "World Wide Web Services". 
</p>
<p>
  <img src="https://i.imgur.com/o3pXTDg.jpeg" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Expand this dropdown menu, and select "Application Development Features". THis will open up another dropdown meanu. Make sure the entry "CGI" is selected, before returning to the "World Wide Web Services". 
</p>
<p>
   <img src="https://i.imgur.com/3u8BaL4.jpeg" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
  From there select "Common HTTP Features". Make sure all entries are selected. Click "OK" to finalize your changes. THis will prompt Windows to install the apropriate web services on your computer. This process is automatic, and will take a couple minutes to complete.
</p>
<br />

<h2>Installing PHP Manager</h2>

<p>
Ther are a few programs that osTicket currelntly requires to function properly. The process is very simple, and straightforward. 

  The first files you will want to download are the <a href="https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view?usp=share_link">PHP manager for IIS</a>, and the <a href="https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link">Rewrite Module </a>. After downloading these files, run and install them. An installation wizard will guide you through the process.

The nest step is the creation of a folder for files to be placed in a little later. In the root directiory, creat a folder. The address should look like this [C:\PHP] This will be the target for the next file. Download <a href="https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link">PHP 7.3.8</a>. Unzip, and extract the files; placing them in the folder [C:\PHP] that you just created.Windows may throw up some errors, or warnings, but keep the files, and proceed with the extraction.
</p>
<p>
  <img src="https://i.imgur.com/1RWr8LP.png" height="40%" width="40%" alt="Disk Sanitization Steps"/><img src="https://i.imgur.com/l8dZXTv.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
  One final download will finish preparing the PHP groundwork for osTicket. This <a href="https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link">C++ Distributable file</a> is very important. Run and install the program.
</p>
<br />

<h2>Installing MySequel Server</h2>
<p>
The next prerequisite step is to install and configure a program called <a href="https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link">"MySQL"</a> Download and install this program from the link. In most cases the "Typical" Installation option is adequate. Once the Installation Wizard is complete, launch mySQL. Usinga standard configuration, set up your credentials.

The nest step will be to open IIS as an administrator. You can locate this program by searcing for it in the start menu
</p>
<p>
  <img src="https://i.imgur.com/7CxD87e.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
  To register MySQL in a way that the computer can use, you will utilize the PHP manager that you installed earlier. From the IIS menu, select and open the PHP Manager.
</p>
<p>
   <img src="https://i.imgur.com/lpY3Hfa.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once open, you will see an optioon to register a new PHP version. Open this and select the PHP in your [C:\PHP] folder.
</p>
<p>
  <img src="https://i.imgur.com/XMUDSwg.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/><img src="https://i.imgur.com/J9NRjbp.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h2>Installing OS Ticket</h2>
<p>
  Now that most of the prerequiste work has been done, you are now ready to install osTicket. <a href="https://drive.google.com/file/d/1VeVXKlzHDRjeaVUL99ptq7qYbrbXdFxJ/view?usp=drive_link">Download</a> the compressed folder, and open it. Locate the "Upload" folder. Copy this folder, and paste it into [c:\inetpub\wwwroot]. Within the target folder, rename "Upload" as "osTicket".

NExt, Open IIS, and navigate to "osTicket Home" by using the dropdown menues on the left hand side of the screen. You should see it cascade as sites -> Default -> osTicket
</p>
<p>
  <img src="https://i.imgur.com/Opqv3Mu.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Select and open PHP Manager. Then click on "Enable or Disable Extensions" under "PHP Extensions" 
</p>
<p>
  <img src="https://i.imgur.com/RZTLk8g.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/><img src="https://i.imgur.com/iP7V1LT.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Go through the list of extensions and enable the following extensions:
 -php_imap.dll
 -php_intl.dll
 -php_opcache.dll

  Once these extensions are enabled, return to the osTicket Home page on IIS, and open the link labled “Browse *:80” THis will bring up the landing page for the osTicket installer. 
</p>
<p>
  <img src="https://i.imgur.com/ZP8LHC5.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/><img src="https://i.imgur.com/i33hNb9.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Before you contionue with instalation there is one last detail that has to be taken care of. Open [C:\inetpub\wwwroot\osTicket\include], and rename "ost-sampleconfig.php" as "ost-config.php". you will need to temporarily open this file so that it can be edited by the installer. Right click on the file, slelect properties, and navigate to "security", then click on "Advanced". Click the button that says "Disable Inheritance", then confirm the removal when the pop-up window asks for confirmation.
</p>
<p>
  <img src="https://i.imgur.com/H3j5KKm.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/><img src="https://i.imgur.com/2nRTh28.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
  While still in the advanced settings, click "Add". A window will pop up. Click on "Service Personel to open another window. In the large box, type "Everyone", click "ok", and then select "Full control". Apply these changes and hit OK, apply, Ok, to close the windows opened while changing this file. 

  You are finally in the last leg! There are only a couple more steps to take!

  Click on "Continue" on the osTicket Installation landing page.
</p>
<p>
  <img src="https://i.imgur.com/kBdHIlP.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
  There is one last prerequisite program that must be installled at this point. <a href="https://docs.google.com/document/d/1WovrX2DaS9xkfaSr4LXyB4YnnWpXIgPCMMbbfgHmGVw/edit">HeidiSQL</a> is a database creation, and management program that will allow you to take advantage of all the capabilities that osTicket can offer, by acting as a bridge bwtween MySQL, and osTicket. Install and run the program.

  Once inside the program, click the "New" button, and enter the same username and password that you used when setting up MySQL. 
</p>
<p>
  <img src="https://i.imgur.com/wblxf0D.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
  This will open a session in MySQL, an will allow you to create a database that osTicket can use. once inside, Right-click on "Unnamed" to generate a cascade menu. Select "Create New", and then select "Database". I reccomend you name your new Database "osTicket", to avoid confussion.
</p>
<p>
  <img src="https://i.imgur.com/nNClUvY.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Now that this database is created, enter the information into the osTicket landing page, with the name of the database, your MySQL username and Password. Double check that you have all of the fields entered correctly, and hit the "Install Now" Button at the bottom of the page.
</p>
<br />

<h2> Cleanup</h2>
<p>
  Before we conclude, there are a couple housekeeping things that you should do.
  Fisrt open [C:\inetpub\wwwroot\osTicket\], and delete the folder named "setup"
  and secondly, Reinstate security protocals on [C:\inetpub\wwwroot\osTicket\include\ost-config.php], by changing "Full control" to "Read only" in the advanced security options.
</p>
<br />

<h2>  Congratulations! You have installed osTicket on your computer! </h2>
