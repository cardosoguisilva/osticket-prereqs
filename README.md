<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
In this tutorial I will be showing you the prerequisites and installation proccess of osTicket, an open-source ticketing system.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create Virtual Machine in Azure
- Install / Enable IIS in Windows with CGI and Common HTTP Festures
- Download and Install Necessary Files
- Configure Permissions
- Practice within OsTicket

<h2>Installation Steps</h2>
<h4>Step 1</h4>
<p>Create an Azure Virtual Machine Windows 10, 4 vCPUs. Username and password of your choice.
</p>
<br />

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/95dccdcf-c4be-47f9-aec2-267e28a66071)

<h4>Step 2</h4>
<p>Log into your virtual machine with remote desktop, install and enable IIS within VM. In order to do that, please select all the highlighted squares and press "okay" to install. To make sure you installed correctly open a web browser and go to 127.0.0.1, it should open up IIS.
</p>
<br />

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/049cab92-0ae8-4c8c-b464-3be2bade7ef5)


<h4>Step 3</h4>
<p>Download and install the <a href="https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">files of OsTicket</a> in this order:
</p>

- PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
- Rewrite Module (rewrite_amd64_en-US.msi)
  
<p> Before dowloading the remaining files create a directory C:\PHP </p>

- Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP. Note: If you have any trouble downloading PHP 7.3.8, please try replicating the same proccess on Google Chrome.
- VC_redist.x86.exe
- MySQL 5.5.62 (mysql-5.5.62-win32.msi)
 <p>  i. Typical Setup </p>
 <p>
   
   ![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/abe6e6d1-bd25-44a1-bfed-4969be4f8729)</p>

  ii. Launch Configuration Wizard (after install)
<p>
 
 ![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/a6bc73c2-2ef9-4f8b-8dd7-acbf350bd060)
</p>

 
  iii. Standard Configuration
<p>
 
 ![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/e50fdc9c-b923-480d-acf1-dcbf39868747)
</p>

  iv. Password1 NOTE: this is the password for MySQL log in "root1"
<p>
 
![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/eeee7485-f263-46de-b0e9-9cac105fbf87)
</p>
<p> Open IIS as Admin and register PHP by clicking on "PHP Manager" then "Register new PHP Version". Provide a path to the php executable file by selecting php-cgi.exe in the php folder. </p>

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/0aeffeb9-f9fd-4422-be27-d7272385fc12)

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/0bf32214-250a-4704-847d-d05455f4f394)

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/4f2254bf-17ec-4c7d-b711-aac6ead8606f)

<p> </p>
<p> </p>
<br />

<h4>Step 4</h4>
<p>Create an Azure Virtual Machine Windows 10, 4 vCPUs. Username and password of your choice.
</p>
<br />

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/95dccdcf-c4be-47f9-aec2-267e28a66071)
<h4>Step 5</h4>
<p>Create an Azure Virtual Machine Windows 10, 4 vCPUs. Username and password of your choice.
</p>
<br />

![image](https://github.com/cardosoguisilva/osticket-prereqs/assets/157248613/95dccdcf-c4be-47f9-aec2-267e28a66071)
