<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
In this tutorial, I will be showing you the prerequisites and installation process of osTicket, an open-source ticketing system.<br />





<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

<ul>
<li>Microsoft Azure (Virtual Machines/Compute)</li>
<li>Remote Desktop</li>
<li>Internet Information Services (IIS)</li>
</ul> 

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create a Virtual Machine in Azure
- Install / Enable IIS in Windows with CGI and Common HTTP Features
- Download and Install Necessary Files

<h2>Installation Steps</h2>
<h4>Step 1</h4>
<p>
  <ul>
    <li>Create an Azure Virtual Machine Windows 10, 4 vCPUs. Username and password of your choice.</li>
    </ul> 
</p>
<br />

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/95dccdcf-c4be-47f9-aec2-267e28a66071)

<h4>Step 2</h4>
<p>
  <ul>
    <li> Log into your virtual machine with remote desktop, install and enable IIS. In order to do that, please select all the highlighted squares and press "okay" to install. To make sure you installed it correctly, open a web browser and go to 127.0.0.1. It should open up IIS.</li>
    </ul>
 
</p>


![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/049cab92-0ae8-4c8c-b464-3be2bade7ef5)


<h4>Step 3</h4>

- Download and install the <a href="https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">files of OsTicket</a> in this order to be more organized:

<ol type="1" >
<li>PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)</li>
<li>Rewrite Module (rewrite_amd64_en-US.msi)</li> </ol>

- Before downloading the remaining files, create a directory C:\PHP
<ol start="3" >
<li>Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP. Note: If you have any trouble downloading PHP 7.3.8, please try replicating the same process on Google Chrome.</li>
<li>VC_redist.x86.exe</li>
<li>MySQL 5.5.62 (MySQL-5.5.62-win32.msi)</li> 
<ul><br>
<li>Typical Setup1</li> <br>
  
  ![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/abe6e6d1-bd25-44a1-bfed-4969be4f8729)
  
<li>Make sure Launch Configuration Wizard (after install) is selected</li><br>

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/a6bc73c2-2ef9-4f8b-8dd7-acbf350bd060)

<li>Select Standard Configuration</li><br>

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/e50fdc9c-b923-480d-acf1-dcbf39868747)

<li>Password1 NOTE: this is the password for MySQL log in "root1"</li><br>

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/eeee7485-f263-46de-b0e9-9cac105fbf87)
</ul>
</ol>
<br>

- Open IIS as Admin and register PHP by clicking on "PHP Manager" then "Register new PHP Version". Provide a path to the php executable file by selecting php-cgi.exe in the php folder that we created earlier. </p> 

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/0aeffeb9-f9fd-4422-be27-d7272385fc12)
<br>
![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/0bf32214-250a-4704-847d-d05455f4f394)
<br>
![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/4f2254bf-17ec-4c7d-b711-aac6ead8606f)


<p>
  <ul>
  <li>After these steps, please restart the web server; press restart under "manage server" on the right-hand side.</li> </ul> </p>

 <ol start="6">
<li>Install osTicket v1.15.8</li>
<ul>
<li>Download osTicket from the Installation Files Folder</li>
<li>Extract and copy “upload” folder to c:\inetpub\wwwroot</li><br>
  
  ![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/be3ef338-14b7-485b-9e23-3ce39b24edf6)
<li>Within c:\inetpub\wwwroot, Rename “upload” to “osTicket” </li><br> 

<li>On ISS go to sites -> Default -> osTicket and on the right, click “Browse *:80”</li> <br>

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/b3dbc1eb-3e46-4843-a34d-36ed8d9a8b8d)

</ul>
</ol>
<br>

- It should load this page; now we are going to enable some of these extensions.
<br>

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/b8f5f4aa-a391-4569-bc6b-0c35963b4583)


<br>

- Go to osticket on IIS and click “Enable or disable an extension.”<br>

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/442733ea-411e-497d-a4ec-1f8099884b03)

<br>

- Right-click and enable the following extensions:<br>

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/f33f12e2-bdb2-4925-b816-7dddef2fefdf)

<br>

- Refresh the osTicket site in your browser
<br>

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/88c82eb0-3103-4957-b088-ba3535a70097)

<br>

- <p> Rename the folder ost-config.php from: C:\inetpub\wwwroot\osTicket\include\<b>ost-sampleconfig.php</b> <br>
  To: C:\inetpub\wwwroot\osTicket\include\<b>ost-config.php</b> </p>
 

- Assign Permissions: ost-config.php <br>
Disable inheritance -> Remove All <br>
New Permissions -> Everyone -> All

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/fc73daec-3207-4ee,6-82will94b)

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/1efa2622-1c78-4034-a2cc-e57a4b3d6c78)

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/0d61688b-fcd0-4643-bb57-189d87ba8c5e)


<ol start="7">
<li>From the Installation Files, download and install HeidiSQL</li> <br>

<ul>
<li>Open Heidi SQL and Create a new session, root/Password1. Click on open.</li>
  <br>
  
  ![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/55fe518a-e473-4849-a2c0-b6783273310a)
  
<li>Create a database called “osTicket”</li> <br> 
<li>Click on "Unnamed", Create new, Database</li>
<br>

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/56f6172d-ac90-44e7-b046-84d15e2a5d8a)

</ul>
</ol>


- Continue Setting up osTicket in the browser (click Continue) 
- Set up  the Name of Helpdesk and the Default email (receives an email from customers) <br>
NOTE: everything from username and password is your choice; make sure to keep a record of it in case you forget.

- After all these steps, your Osticket installer page should look similar to mine. 
<br>

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/c035d098-e7fb-4366-aaa0-324b9338b175)

<br>

- Go ahead and click install now, and if you followed all my instructions, this page will open.

<br>
   
![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/f9ad1af7-75e6-4778-8e77-7cd48fa8dfb0)

<br>

<p> - For clean up Delete the "SETUP" folder in C:\inetpub\wwwroot\osTicket\<b>setup</b> AND <br>
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

  
![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/01973ec7-8029-41ff-a945-5e98131c04cf)


- Log into your account at http://localhost/osTicket/scp/login.php using the login we made earlier. Mine, for example, was Login: "guilherme@gmail.com" Password: "Password1"
  
<br>

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/a18784e2-a448-4d79-a639-2593bc6221eb)


<br />

