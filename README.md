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
<img src="https://i.imgur.com/Szr0Zzd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 
<p>
<img src="https://i.imgur.com/bWckbmP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we will be clicking on "Programs" for "Control Panel", then for "Programs and Features" we will click on "Turn Windows features On or Off".
</p>
<br />

<p>
<img src="https://i.imgur.com/nuIIAHJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/20wIc28.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we will be checking "Internet Information Services" (IIS) and expand it, we will also expand "Worldwide Web", "Application Development Features" and we will be checking the (CGI) box. We need to install (CGI) with (IIS), because (CGI) let's us install "PHP Manager". (PHP) is a back-end "Web Programming Language" and "oSTicket" runs off of (PHP), so we have to install a Web Server with (PHP) on this computer.  
</p>
<br />

<p>
<img src="https://i.imgur.com/pHAMXS3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/XqkIK00.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/HJSJ0S1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once the changes are done, the "Programs" screen will confirm "Windows completed the requested changes", then we will click on "Close". Now, to Test to see if our "Web Server" is working, we will open up a new "Tab" and type in "127.0.0.1" in which is called our "Local Host" or the "Loopback", this is essentially saying, try to load a web page that's running off myself and we can see that it loaded the default (IIS) Website, so we know that our Web Server is up and running.
</p>
<br />

<p>
<img src="https://i.imgur.com/6kcPOfl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/YO1Om29.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/0fmYDeR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
<p>
<img src="https://i.imgur.com/ujj49DU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
<p>
<img src="https://i.imgur.com/cO7b3Ns.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we will download and install "PHP Manager" for (IIS) and we will open up "File Folder" so that we can download it straight up. When the "PHP Manager" screen appears, we are going to click on "Next" for "Warranty", then for "License Agreement" we are going to click on "I Agree" and then click on "Next" for the installation. Once "PHP Manager" is finished with Installation, we will click on "Close"
</p>
<br />

<p>
<img src="https://i.imgur.com/0nX44zJ.png" height="80%" width="80%" alt"Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/kIFTFy3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
<p>
<img src="https://i.imgur.com/lEcWACw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/uwti634.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we need to install "Rewrite Module". "Rewrite Module" allows certain special configurations in the config files inside of "oSTicket" that does certain things behind the scenes with "URL's", so once it appears in the "File Explorer" file, double-click on it to start the process of installation. When the "IIS URL Rewrite Module 2 Setup" screen appears, we will check the box for "I accept the terms in the license agreement" and then click on "Install". Once it's done downloading and installing, we will click on "Finish"
</p>
<br />

<p>
<img src="https://i.imgur.com/TuQvbfX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
<p>
<img src="https://i.imgur.com/qrEIHRM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
<p>
<img src="https://i.imgur.com/I4o8Qqa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we need to create a "Directory" for "PHP" on the local harddrive, so we're just going to create "PHP" on the "Root" of "Windows (C) Drive". Next, we'll go to "Windows (C) Drive" then we'll right-click and go down and click on "New" and then click on "Folder" and then well name our new folder "PHP".
</p>
<br />

<p>
<img src="https://i.imgur.com/c5vlyl7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 
<p>
<img src="https://i.imgur.com/cTsgE8M.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
<p>
<img src="https://i.imgur.com/BlLtfOt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/Oc7N7lt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/BZYn2Xh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/V86pJQX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next were going to download "PHP" and then we are going to unzip the contents of this into the "PHP" folder that we created. While downloading "PHP" there will be a "Microsoft Defender" screen that will ask you if you are sure that you trust the file that is being downloaded (PHP) click on "Keep Anyway". Once it downloads in our "File Explorer" folder, right-click on the "PHP" folder and then click on "Extract All". When the "Extract Compressed (Zipped) Folder" screen appears, we will type in "C:\PHP" and then click on "Extract", and all of the data will be dumped into the file.
</p>
<br />

<p>
<img src="https://i.imgur.com/bK6U0ba.png" heigth="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/iOY7CQ7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/YW0LwJ2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
<p>
<img src="https://i.imgur.com/YPCKVOG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now, we are going to download and install "Microsoft Visual C++ Redistributable". "PHP" requires it so we need to install it. Once we download it, it will show up in our "File Explorer" so we will double-click on the file and when the "Microsoft Visual C++ Redistributable" screen comes up, we will check the box for "I agree to the license terms and conditions" and then click on "Install". Once it's done installing, we will click on "Close".
</p>
<br />

<p>
<img src="https://i.imgur.com/JiMFv4h.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we are going to download "MySQL Server". The purpose of "MySQL Server", is that it is going to install a "Database" on this actual computer (Virtual Machine), because "oSTicket" needs to store the application data like all of the tickets and users. So, we will click on "Download" to start the installation.
</p>
<br />

<p>
<img src="https://i.imgur.com/9TOKrwQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now, we are going to go to our "File Explorer" and then go to "Downloads Folder" and we will double-click on "mysql-5.5.62-win32" to start downloading.
</p>
<br />

<p>
<img src="https://i.imgur.com/fEO4Uyl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
When the "MySQL Server 5.5 Setup" screen appears, we will click on next.
</p>
<br />

<p>
<img src="https://i.imgur.com/ubfXHed.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we will check on the small box for "I accept the terms in the Licence Agreement" and then click on "Next"
</p>
<br />

<p>
<img src="https://i.imgur.com/kyXcLd4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
For "Choose Setup Type" we will click on "Typical" and then click on "Next"
</p>
<br />

<p>
<img src="https://i.imgur.com/SyD2toE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
When the "Ready to install MySQL Server 5.5" screen appears, we will click on "Install"
</p>
<br />

<p>
<img src="https://i.imgur.com/ny9jsfB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
When the "Completed the MySQL Server 5.5 Setup Wizard" screen appears, we have to make sure that we check the small box where it states "Launch the MySQL Instance Configuration Wizard" and then we will click on "Finish"
</p>
<br />

<p>
<img src="https://i.imgur.com/TeBDA8k.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
When this screen appears we will click on "Next" to configure "MySQL".
</p>
<br />

<p>
<img src="https://i.imgur.com/AQaYvLk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, for configuration type we will click on "Standard Configuration" then click "Next".
</p>
<br />

<p>
<img src="https://i.imgur.com/ppBuuvo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
For "Window Options", we will click "Next".
</p>
<br
    
<p>
<img src="https://i.imgur.com/pqVGZFs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
For "Security Options", we are going to enter and re-enter a "root" password and then click on "Next".
</p>
<br />

<p>
<img src="https://i.imgur.com/MQgdB8m.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, click on "Execute" to start processing the configurations.
</p>
<br />

<p>
<img src="https://i.imgur.com/EcZQ4mY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once it's completed, click on "Finish" to complete the "MySQL Server" installation.
</p>
<br />

<p>
<img src="https://i.imgur.com/A9LfcMq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we are going to open up "IIS" as an "Admin" so, we will click on "Start Menu" in the lower left corner of our screen and type in the search bar "IIS". Then we will go up and right-click on "Internet Information Services Manager (IIS)" and then click "Run as administrator"
</p>
<br />

<p>
<img src="https://i.imgur.com/ryAbtCm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we will double-click on "PHP Manager".
</p>
<br />

<p>
<img src="https://i.imgur.com/voRt9RN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
"PHP" states "PHP is not enabled. Register new PHP version to enable PHP via FastCGI", so we are going to click on "Register new PHP version".
</p>
<br />

<p>
<img src="https://i.imgur.com/oc2MYCX.png" height="80%" width="80%" alt="Dik Sanitization Steps"/>
</p>
<p>
Next, we are going to register a new "PHP" version and this is where we are going to browse to where we dumped all of the "PHP" data in the "File Explorer" "C:\PHP" folder, so click on this small box.
</p>
<br />

<p>
<img src="https://i.imgur.com/KyLLoAd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then well go to "Windows (C) Drive" in "File Explorer" and go down and double-click on "PHP" folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/ewAaOV9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Then we will double-click on "php.cgi" and make sure that "PHP executable (php.cgi.exe)" box is selected, and then well double-click on "php.cgi" file again.
</p>
<br />

<p>
<img src="https://i.imgur.com/i7acNWC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then we will click on "OK" to register.
</p>
<br />

<p>
<img src="https://i.imgur.com/Mb0g9vt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once "PHP Manager" is registered, and whenever we make any adjustments to "IIS", it's recommended to "Restart" the Web Server. So we will click on the name of the server which is "vm-osticket(vm-osticket\lab)" and then we will click on "Restart" to refresh the Web Server.
</p>
<br />

<p>
<img src="https://i.imgur.com/ViMz8ek.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we will be installing the "oSTicket" ticketing system.
</p>
<br />

<p>
<img src="https://i.imgur.com/iezKzyX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we need to "Extract" and "Copy" the "Upload" folder into the "C:\inetpub\wwwroot". This is a special folder, this is our Web Server's main folder and our "Upload" folder is inside of our "oSTicket" that we just downloaded. So we will open up 2 "File Explorer" folders, were we have our "oSTicket" file.
</p>
<br />

<p>
<img src="https://i.imgur.com/DCB1K5t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we need to go to our 2nd "File Explorer" folder and we need to double-click our "oSTicket" zip file.
</p>
<br />

<p>
<img src="https://i.imgur.com/UUzzcTL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then we need to drop our "Upload" folder into our "C:\inetpub\wwwroot" folder in our "Windows (C) Drive".
</p>
<br />

<p>
<img src="https://i.imgur.com/LaxFlAC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
So, we will open up "Windows (C) Drive" in our 1st "File Explorer" folder and double-click the "Windows (C) Drive.
</p>
<br />

<p>
<img src="https://i.imgur.com/hVp12DO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then well double-click on our "Inetpub" folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/GEoBj5Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then well double-click on "wwwroot" folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/DsUIjJU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then we will go back to our 2nd "File Explorer" folder and click and drag our "Upload" folder into our 1st "File Explorer" folder into "c:\inetpub\wwwroot" in "Windows (C) Drive" and then let it "Copy" and finish.
</p>
<br />

<p>
<img src="https://i.imgur.com/Lb0s25a.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we can see that we have our "Upload" folder inside of our "wwwroot" folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/cpLT8tA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/W8UgMwj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
<p>
<img src="https://i.imgur.com/fAuyhhW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
<p>
<img src="https://i.imgur.com/IQGWX7g.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we have to "Rename" our "Upload" folder to "osTicket", so we will right-click on the "Upload" folder and go down to "Rename" and change it to "osTicket".
</p>
<br />

<p>
<img src="https://i.imgur.com/vT07pcU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
So, well go back to "IIS" and "Restart" the sever. So well click on the server which is "vm-osticket\Lab" and we are going to "Restart" the server again.
</p>
<br />

<p>
<img src="https://i.imgur.com/vAyunQ8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we are going to go to sites inside of "IIS" and click on the small arrow for "Sites".
</p>
<br />

<p>
<img src="https://i.imgur.com/AwSYcw8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then, click on the small arrow for "Default Web Site".
</p>
<br />

<p>
<img src="https://i.imgur.com/Uvg0a3L.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then, we will click on the "osTicket" folder and also click on "Browse*80" to open up "oSTicket".
</p>
<br />

<p>
<img src="https://i.imgur.com/bbjvMql.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
If you get an error here, it means that you need to either restart the lab or try to figure out what went wrong, but this "oSTicket" screen should appear which means that "oSTicket" is now working and installed properly.
</p>
<br />

<p>
<img src="


