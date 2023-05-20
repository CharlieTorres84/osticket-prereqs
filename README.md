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
<img src="https://i.imgur.com/fIFEwWV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In order to create an osTicket, we must first create our Resource Group in Azure Portal. So we will go to (portal.azure.com) and create our Resource Group.
</p>
<br />

<p>
<img src="https://i.imgur.com/4ITVHnl.png" height="80%" width="80%" alt="Disk Sanitazation Steps"/>
</p>
<p>
Once we're done creating our Resource Group in Azure Portal we will create our Virtual Machine (VM) next.
</p>
<br />
  
<p>
<img src="https://i.imgur.com/3zbP04A.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The next step would be to type in Virtual Machine (VM) in our Search bar and create our Virtual Machine (Windows 10) with its credentials. 
</p>
<br />

<p>
<img src="https://i.imgur.com/rFNTeEV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once our Virtual Machine (VM) has been created and it's up and running with all of its resources, we will Remote Desktop Connect right into our Virtual Machine (VM).  
</p>
<br />

<p>
<img src="https://i.imgur.com/ZhgZYYX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once we have Remote Desktop Connection running, we will copy our Virtual Machine's (VM) Public IP Address and we will login into Remote Desktop Connection.
</p>
<br />

<p>
<img src="https://i.imgur.com/snRyFsV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we have to click on "Use a different Account" and we have to type in the Username and Password that we created when we created our Virtual Machine in Azure Portal.
</p>
<br />

<p>
<img src="https://i.imgur.com/Lce2EfA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once we are inside of the Virtual Machine we will see this Blue Desktop Screen with the Windows Icon.
</p>
<br />

<p>
<img src="https://i.imgur.com/ZKbeNr1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we're going to install and enable "Internet Information Services" (IIS) with (CGI). (IIS) is a Web Server that allows this computer to serve up different websites because "oSTicket" runs out of a website and we need to configure (IIS) so that we can run "oSTicket". So first, we need to right-click the "Start Menu" and click on "Run" and then we need to type in "Control" for Control Panel, then click "OK"
  
<p>
<img src="https://i.imgur.com/CQaHIqy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 
<p>
<img src="https://i.imgur.com/pKyhNQn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we will be clicking on "Programs" for "Control Panel", then for "Programs and Features" we will click on "Turn Windows features On or Off".
</p>
<br />

<p>
<img src="https://i.imgur.com/YpWhUZy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/hvAuaKm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we will be checking "Internet Information Services" (IIS) and expand it, we will also expand "Worldwide Web", "Application Development Features" and we will be checking the (CGI) box. We need to install (CGI) with (IIS), because (CGI) let's us install "PHP Manager". (PHP) is a back-end "Web Programming Language" and "oSTicket" runs off of (PHP), so we have to install a Web Server with (PHP) on this computer.  
</p>
<br />

<p>
<img src="https://i.imgur.com/kHBUgUh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/rrFODVu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/vUiBxV8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once the changes are done, the "Programs" screen will confirm "Windows completed the requested changes", then we will click on "Close". Now, to Test to see if our "Web Server" is working, we will open up a new "Tab" and type in "127.0.0.1" in which is called our "Local Host" or the "Loopback", this is essentially saying, try to load a web page that's running off myself and we can see that it loaded the default (IIS) Website, so we know that our Web Server is up and running.
</p>
<br />

<p>
<img src="https://i.imgur.com/CSuWy3B.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>


