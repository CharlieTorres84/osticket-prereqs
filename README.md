# osticket-prereqs<p align="center">
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

- Enable Internet Information Servives (IIS)
- Install Web Platform Installer
- Install MySQL, Setup Username and Password
- Install VC Redistributable
- Configure Permissions and Install oS Ticket

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/sJ2oN8x.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In order to create an osTicket, we must first create our Resource Group in Azure Portal. So we will go to (portal.azure.com) and create our Resource Group.
</p>
<br />

<p>
<img src="https://i.imgur.com/DObtWqn.png" height="80%" width="80%" alt="Disk Sanitazation Steps"/>
</p>
<p>
Once we're done creating our Resource Group in Azure Portal we will create our Virtual Machine (VM) next.
</p>
<br />
  
<p>
<img src="https://i.imgur.com/NV5IRT0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The next step would be to type in Virtual Machine (VM) in our Search bar and create our Virtual Machine with its credentials. 
</p>
<br />

<p>
<img src="https://i.imgur.com/VFDFBPO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once our Virtual Machine (VM) has been created and it's up and running with all of its resources, we will Remote Desktop Connect right into our Virtual Machine (VM).  
</p>
<br />

<p>
<img src="https://i.imgur.com/E6siYHV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once we have Remote Desktop Connection running, we will copy our Virtual Machine's (VM) Public IP Address and we will login into Remote Desktop Connection.
</p>
<br />

<p>
<img src="https://i.imgur.com/dzspsDA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we have to click on "Use a different Account" and we have to type in the Username and Password that we created when we created our Virtual Machine in Azure Portal.
</p>
<br />
