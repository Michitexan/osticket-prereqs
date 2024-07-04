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
- Install Web Platform Installer
- Install MySequel
- install C++ Distributable 
- Install OS Ticket

<h2>Installation Steps</h2>

<p>
  While osTicket is a very powerful tool, there are some supporting and interdependant programs that are required to use this tool to it's full potential. In this guide, you will establish the ground floor for your own ticketing system.

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
  From there select "Common HTTP Features". Make sure all entries are selected. Click "OK" to finalize your changes. THis will prompt Windows to install the apropriate web services on your computer. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
