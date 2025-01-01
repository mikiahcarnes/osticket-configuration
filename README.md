<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png"/>
</p>

<h1>Post-Install Configuration</h1>
This will outline the post-installation configuration of osTicket.<br/>

 <h2> Objectives </h2>

- Configure Roles
- Configure Department
- Configure Teams
- Configure Agents
- Configure Users
- Configure SLA
- Configure Help-Topics


<h2> Operating System & Technologies  Used</h2>

- Windows 10
- VMware Workstation Pro
- XAMPP v8.2.12
- osTicket v1.18.1

 

  <h2>Steps</h2>
<p>
<h3 align="center">Note: Before you continue, ensure XAMPP Apache and MySQL are still running and you have logged into your osTicket admin account, which you made in the previous steps. Here is the link to the login page: http://localhost/osticket/upload/scp/login.php. After logging in, ensure you are in the Admin Panel, not the Agent Panel. Look up the top right where it says Welcome; if it says Agent Panel, you are in the Admin Panel. If it says Admin Panel, you are in the Agent Panel. Reference the picture below. I will leave links to the osTicket documentation with each step.</h3>
<br />
</p>
<p>
 <img src="https://i.postimg.cc/PrS169Qt/Add-New-Role.png" height="75%" width="100%">
</p>
<p>
<h3 align="center">From the Admin Panel, you should be at the settings tab by default. Click on Agents to the far right and then click on Roles. Then click on Add New Role. Create the name of the role, then click on the permissions tab. I created the Supreme Admin role for demonstration, so all permissions are checked. The permission given will depend on the role you are creating. <a href="https://docs.osticket.com/en/latest/Admin/Agents/Roles.html" target="_blank">Documentation</a></h3>
<br />
</p>
<p>
	<img src="https://i.postimg.cc/0N0dBWf8/Add-New-Department.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center"> We'll set up a new department next. If a ticket comes into an agent in the Support department that the System Administration department would better handle, they can pass it off. From the Admin Panel, click on Agents, Department, and then Add New Department. In this lab, I kept it simple</h3>
<br />
<p>
	<div align="center">
  <img src="https://i.postimg.cc/1tztSwJj/os-Ticket-Install-Page.png" alt="Image 1" height="75%" width="45%">
  <img src="https://i.postimg.cc/VsXCRQdG/os-Ticket-Git-Hub.png" alt="Image 2" height="75%" width="45%">
</div>
	
</p>
<br />
<h3 align="center">Now that XAMPP is up and running, it's time to download the osTicket .zip folder. You can find the latest version of osTicket <a href="https://osticket.com/download/" target="_blank">here</a>. I circled what you need to click on each page to download the osTicket .zip folder only. After downloading the osTicket .zip folder, right-click it and extract all. After you extract the osTicket folder, I suggest renaming it to "osTicket." </h3>
<br />
<p>
	<img src="https://i.postimg.cc/zfN9gyXj/Path-Foros-Ticket-In-XAMPP.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Now, we want to move the unzipped osTicket folder into your XAMPP server. You can do this by either right-clicking and copying the folder, then pasting it in the htdocs folder, or clicking ctrl + x and then pasting it to the htdocs folder. The path for this is "C:\xampp\htdocs." After you paste the file, it should look like the image above. </h3>
<br />
<p>
  <img src="https://i.postimg.cc/J4tx0MFw/localhostpath.png" height="75%" width="100%"/>
</p>
<br />
<h3 align="center">Go back to the XAMPP control panel, make sure Apache and MySQL are started, and click on the Admin action beside Apache. It will likely open into the "localhost/dashboard/" link. Change dashboard to osTicket or whatever you changed the name of your osTicket folder to. It should look like the picture above. Click on the upload folder and click continue on the setup page for a default setup. You can always enable the other features later if you need them.</h3>
<br />
<p>
  <img src="https://i.postimg.cc/xTRXwz5n/pathforos-confignamechange.png"height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">The next page will tell you that you are missing the configuration file. The above picture is the path to the ost-sampleconfig.php file which you need to rename to ost-config.php.</h3>
<br />
<p>
  <img src="https://i.postimg.cc/nLbwL5tF/os-Ticket-Basic-Install.png" height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">This page is where you will setup where you will name your helpdesk and create the admin user. You do not have to use a real email for either of these but they do need to be different emails. Be sure to take note of your username and password for the admin user login.</h3>
<br />
<p>
  <img src="https://i.postimg.cc/85nZ0Svt/Database-Set-Up.png" height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">Go back to the XAMPP Control Panel and click on the Admin action beside MySQL. This will bring you to the phpmyadmin page shown above. On the left side of the page click new to create a new database. Name it whatever you want to.</h3>
<br/>
<p>
  <img src="https://i.postimg.cc/4xzrYK8L/Login-Info-Database.png" height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">Now we need to make a new user for the database. After the database is created you will see it to the left of the page at the bottom. Click on it and click on the privileges tab and click on add user account. You can name it whatever you what, but make sure the Host name is set to Local and localhost. Again, remember to take note of your username and password. Then, scroll down a bit and you will see the Global privileges section, go ahead and check all. Then scroll all the way down and click Go. After the database has been made go back to the osTicket setup page and type in the into. MySQL Hostname, MySQL Database, MySQL Usename, and MySQL Password.</h3>
<p>
  <img src="https://i.postimg.cc/T1hdkQ9S/After-Install.png" height="75%" width="100%" />
</p>
<br/>
<h3 align="center">Your install page will look different from the one above, but nonetheless. You have now installed osTicket! You can now follow the instructions for Config file permissions. After that head over to the Admin Panel, which you will see a link to on the right of the page, and continue with configuring osTicket.</h3>
