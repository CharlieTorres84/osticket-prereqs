# osticket-prereqs<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial and walkthrough outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



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
Next were going to download "PHP" and then we are going to unzip the contents of this into the "PHP" folder that we created. While downloading "PHP" there will be a "Microsoft Defender" screen that will ask you if you are sure that you trust the file that is being downloaded (PHP) click on "Keep Anyway". Once it downloads in our "File Explorer" folder, right-click on the "PHP" folder and then click on "Extract All". When the "Extract Compressed (Zipped) Folder" screen appears, we will type in "C:\PHP" and then click on "Extract", and all of the data will be dropped into the file.
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
<img src="https://i.imgur.com/LdEkp59.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We can notice that some "Extensions" are not enabled here and we can see some red x's here, so we will adjust and enable a few things in "IIS" to eliminate some of the red x's and make them work.
</p>
<br />

<p>
<img src="https://i.imgur.com/5vJ4TL7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
So, we will go back to "IIS" and click on "osTicket" folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/l6tlq1q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then well double-click on "PHP Manager".
</p>
<br />

<p>
<img src="https://i.imgur.com/djlDFH1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then we will go down to "PHP Extensions" and click on "Enable or Disable an Extension".
</p>
<br />

<p>
<img src="https://i.imgur.com/AWPxT4O.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we are going to "Enable" the following extensions.
</p>
<br />

<p>
<img src="https://i.imgur.com/SKQtMEg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The 1st extension that we are going to "Enable" is "php_imap.dll", so we will click on it and then click on "Enable" at the upper right-hand corner under "Actions".
</p>
<br />

<p>
<img src="https://i.imgur.com/M3wth6j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The 2nd extension is going to be, "php_intl.dll", then click on "Enable".
</p>
<br />

<p>
<img src="https://i.imgur.com/2DUXcPt.png" height"80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The 3rd extension is going to be "php_opcache.dll" then click on "Enable" to complete the extensions.
</p>
<br />

<p>
<img src="https://i.imgur.com/p8Uu0jh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next well go back to our "oSTicket" Browser and click on "Refresh" icon to remove some of the red x's.
</p>
<br />

<p>
<img src="https://i.imgur.com/xSM9hSc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once we "Refresh" the "oSTicket" browser page, we can see that we removed 2 red x's now.
</p>
<br />

<p>
<img src="https://i.imgur.com/mCkr9tg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we need to open up "File Explorer" folder and we need to "Rename" "ost-config.php" file, so we will open up "File Explorer" to "wwwroot" and double-click on "osTicket" file.
</p>
<br />

<p>
<img src="https://i.imgur.com/ew7Heke.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we will double-click on "include" folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmrW8F.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then we will scroll down to "ost-sampleconfig.php"
</p>
<br />

<p>
<img src="https://i.imgur.com/Gz8F2Xt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
So, we will only delete "Sample" out of the "ost-sampleconfig.php", so it will look like this "ost-config.php" now.
</p>
<br />

<p>
<img src="https://i.imgur.com/a2K3ltB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we will be setting the "Permissions" on this "ost-config.php" file, so that everyone has the ability to do anything they want to this file. That's because the actual "osTicket" installer that's going to run on this browser, needs to manipulate and interact with this file and we don't know what "User" it's going to use to do that, so we need to let everyone have access to this file in the meantime. So in order to do that, first we will right-click on "ost-config.php" and click on "Properties".
</p>
<br />

<p>
<img src="https://i.imgur.com/tVHXblR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then well click on "Security" and then click on "Advanced".
</p>
<br />

<p>
<img src="https://i.imgur.com/EU3HmhE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we will click on "Disable Inheritance", so it will stop inheriting permissions.
</p>
<br />

<p>
<img src="https://i.imgur.com/LV3MahL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now, we will click on "Remove all inherited permissions from this object".
</p>
<br />

<p>
<img src="https://i.imgur.com/kQiCReE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now, we are going to click on "Add" for permissions.
</p>
<br />

<p>
<img src="https://i.imgur.com/i0z1etz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we will click on "Select a Principle".
</p>
<br />

<p>
<img src="https://i.imgur.com/hfKwB4z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then we will type in "EVERYONE" then click on "Check Names" and then click on "OK".
</p>
<br />

<p>
<img src="https://i.imgur.com/JvwcEFg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
For now, we are going to give everyone "Full Control" then click on "OK".
</p>
<br /> 

<p>
<img src="https://i.imgur.com/V9w5QcO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then we will click on "Apply" and then click on "OK".
</p>
<br />

<p>
<img src="https://i.imgur.com/2j2RPCQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then we will click on "OK" again so, now everyone in "ost-config.php" has permissions to it.
</p>
<br />

<p>
<img src="https://i.imgur.com/z4qR3rG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we are going to continue setting up "osTicket" in the browser, so well go back to our "osTicket" browser and we will click on "Continue".
</p>
<br />

<p>
<img src="https://i.imgur.com/N2Y4ZMW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
For "System Settings" we can type in any "Help Desk Name" and "Default Email"  we need to write the "Default Email" down in some notes somewhere so that we don't forget.
</p>
<br />

<p>
<img src="https://i.imgur.com/EqDRvY1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
For "Admin User" we will continue to type in our credentials, we need to always remember to right down our "Username" and "Password" in some notes in a pad so that we don't forget and we don't have any issues when we try to login.
</p>
<br />

<p>
<img src="https://i.imgur.com/ViznNuO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, before we fill in our "Database Settings" we have to setup a "Database" which is called "HeidiSQL". So, we will install "HeidiSQL" in which allows us to connect to our "MySQL" database that we installed earlier and it will allow us to connect to that "SQL" server and then were going to setup a database the "osTicket" is going to use.
</p>
<br />

<p>
<img src="https://i.imgur.com/tT8yceI.png" height"80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
So now we are going to install "HeidiSQL", so double-click on "HeidiSQL".
</p>
<br />

<p>
<img src="https://i.imgur.com/cKVuWSk.png" height"80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
For "License Agreement", we will click on "I accept the agreement" and then click on "Next".
</p>
<br />

<p>
<img src="https://i.imgur.com/ulyYhEm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we will click on "Next: for "Select Destination Location".
</p>
<br /

<p>
<img src="https://i.imgur.com/iaahhZY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then we will click on "Next" for "Select Start Menu Folder".
</p>
<br />

<p>
<img src="https://i.imgur.com/fCRsD4t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We will also click on "Next" for "Select Additional Tasks".
</P>
<br />

<p>
<img src="https://i.imgur.com/Azxm2th.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then we will click on "Install" for "Ready to Install".
</p>
<br />

<p>
<img src="https://i.imgur.com/Zvehpg7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then well make sure that the small box is checked for "Launch HeidiSQL" and then we will click on "Finish" to finish Installing.
</p>
<br />

<p>
<img src="https://i.imgur.com/dArPFcc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we need to create a "New" connection to the database , so we will click on "New".
</p>
<br />

<p>
<img src="https://i.imgur.com/mPJZyun.png" height="80%" width="80%" alt="Disk Saniyization Steps"/>
</p>
<p>
We need to put in the "Username" that we created earlier in "MySQL" server which is "root" and the password that we also created, so we will put in the "Password" and then click on open.
</p>
<br />

<p>
<img src="https://i.imgur.com/YFO10Dm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we can see that we have our connection to "MySQL" server. 
</p>
<br />

<p>
<img src="https://i.imgur.com/Z74TrjI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we need to our "MySQL Database", "MySQL Username" and "MySQL Password", so we will type in our "Username" which is "root" and the "Password" that we created in "MySQL" server.
</p>
<br />

<p>
<img src="https://i.imgur.com/64woQ9k.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we have to create a "New" database in "HeidiSQL", so we will open up "HeidiSQL" and then right-click on "Unamed"
</p>
<br />

<p>
<img src="https://i.imgur.com/RJ2o5YA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then click on "Create new".
</p>
<br />

<p>
<img src="https://i.imgur.com/ouBOsYv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then click on "Database".
</p>
<br />

<p>
<img src="https://i.imgur.com/v9GwFIr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then we are going to name the database "osTicket" then click "OK".
</p>
<br />

<p>
<img src="https://i.imgur.com/ffYx7ey.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We can now see that our "osTicket" database was successfully created, because there was no error messages.
</p>
<br />

<p>
<img src="https://i.imgur.com/dDCgQif.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now, we will go back to our "osTicket" browser and go back to "Database Settings" and type in "osTicket" for "MySQL Database" and then click on "Install Now" to finish our "osTicket" installation.
</p>
<br />

<p>
<img src="https://i.imgur.com/isjLSDU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
If you see this screen, that means that we successfully installed our "osTicket" ticketing system. Now, we need to do a few things for clean up and then we are going to test our "Logging-in" and if it works properly, then we are ready to use our  "osTicket" ticketing system.
</p>
<br />

<p>
<img src="https://i.imgur.com/vQtemAm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
So, for clean up we need to go back to "File Explorer", then "My PC", and into our "Windows (C) Drive" to delete our "Setup" folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/m7dVXqp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</P>
<p>
Next, we will double-click on "inetpub".
</p>
<br />

<p>
<img src="https://i.imgur.com/OPhPy4J.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then, double-click on "wwwroot" folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/E3NUk1T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then, double-click on "osTicket" folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/R7t8Ah8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then go down to "Setup" folder and right-click and then click on "Delete" to delete "Setup" folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/hVpqMs4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we are going to double-click on "include" folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/KcgFRGN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then we are going to right-click on "ost-config.php" file and then click on "Properties", because we are going to set the "Permissions" back on "ost-config.php" file and we are going to reset the permissions to "Read-only".
</p>
<br />

<p>
<img src="https://i.imgur.com/79NrXMA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we will click on "Security" and then click on "Advanced".
</p>
<br />

<p>
<img src="https://i.imgur.com/bZ7w8ZH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then, well click on "Everyone".
</p>
<br />

<p>
<img src="https://i.imgur.com/d6pmWXA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then, we will click on "Edit".
</p>
<br />

<p>
<img src="https://i.imgur.com/uqSKXNa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we will uncheck "Full Control", "Modify" and "Write" and then click on "OK"
</p>
<br />

<p>
<img src="https://i.imgur.com/izxhNiC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then we will click on "Apply" and then "OK".
</p>
<br />

<p>
<img src="https://i.imgur.com/L5ivPSg.png" height="80%" width="80%" alt="Disk sanitization Steps"/>
</p>
<p>
Then we will click on "OK".
</p>
<br />

<p>
<img src="https://i.imgur.com/ujlwFsF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This "URL" here is used as an "Admin" to log into it and do "Admin" stuff.
</p>
<br />

<p>
<img src="https://i.imgur.com/SnQuSRp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This "URL" is for "End User's" who actually want to create tickets inside of "osTicket".
</p>
<br />

<p>
<img src="https://i.imgur.com/tk3tnBV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
So we will copy the "Admin" "URL" and this "osTicket" page should appear.
</p>
<br />

<p>
<img src="https://i.imgur.com/o9ihZN6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we will type in our "Username" and "Password" that we created in our "osTicket" page and then log-in.
</p>
<br />

<p>
<img src="https://i.imgur.com/1DHJB9f.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
If you were able to successfully Log-in to this page, that means that you completed all of the proper steps that was required to install and log-in to "osTicket".  In the next Repository we will go over the "Post-Installation Config" of all of the things inside of "osTicket". (140)
</p>
<br />




                                                                       







