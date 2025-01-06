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
<h3 align="center">Note: Before you continue, ensure XAMPP Apache and MySQL are still running, and you have logged into your osTicket admin account, which you made in the previous steps. Here is the link to the login page: http://localhost/osticket/upload/scp/login.php. After logging in, ensure you are in the Admin Panel, not the Agent Panel. Look at the top right where it says Welcome; if it says Agent Panel, you are in the Admin Panel. If it says Admin Panel, you are in the Agent Panel. Reference the picture below. I will leave links to the osTicket documentation with each step.</h3>
<br />
</p>
<p>
	<img src="https://i.postimg.cc/PrS169Qt/Add-New-Role.png" height="75%" width="100%">
</p>
<p>
<h3 align="center">From the Admin Panel, you should be at the settings tab by default. Click on Agents to the far right and then click on Roles. Then click on Add New Role. Create the name of the role, then click on the permissions tab. I created the Supreme Admin role for demonstration, so all permissions are checked. The permission given will depend on the role you are creating. <a href="https://docs.osticket.com/en/latest/Admin/Agents/Roles.html" target="_blank"> Documentation</a></h3>
<br />
</p>
<p>
	<img src="https://i.postimg.cc/0N0dBWf8/Add-New-Department.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center"> We'll set up a new department next. If a ticket comes into an agent in the Support department that the System Administrator department would better handle, they can pass it off. From the Admin Panel, click on Agents, Department, and then Add New Department. In this lab, I kept it simple and kept all default settings, but in a real environment, you would want to change a few of these accordingly. We will set up the SLA later.<a href="https://docs.osticket.com/en/latest/Admin/Agents/Departments.html" target="_blank"> Documentation</a></h3>
<br />
<p>
	<img src="https://i.postimg.cc/pXR67ZZD/Add-New-Team.png" height="75%" width="100%" />
</p>
<br />
<h3 align="center">Now, we'll create a new team. Teams are how you group people together; level 1, 2, and 3 support, for example. Click on the Agents tab if you aren't already, then click on Teams, and then Add New Team. Refer to the picture above. Since there are no members of the newly created team, you can either make yourself the team lead or leave it blank. For lab purposes, it doesn't matter. <a href="https://docs.osticket.com/en/latest/Admin/Agents/Teams.html" target="_blank"> Documentation</a></h3>
<br />
<p>
	<img src="https://i.postimg.cc/J0rCRt0p/Allow-Anyone-To-Create-Tickets.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">We need a setting that allows everyone to create a ticket without logging in. From the Admin Panel, click on the Settings tab, then click on Users Settings. Uncheck the "Require registration and login to create ticket" box if it is checked; if not, just leave it unchecked. Registration Method should also be set to public. </h3>
<br />
<p>
  <img src="https://i.postimg.cc/br3JstQs/Add-New-Agent.png" height="75%" width="100%"/>
</p>
<br />
<h3 align="center">Now we need to make a couple of new agents(workers) to work on the tickets. Admin Panel -> Agents -> Agents -> Add New. Give them whatever name and email you want; it doesn't have to be a real email and make the username their first name. Then click Set Password and uncheck "Send agent a password reset email" if it has already been checked. Make a simple password you can remember; I suggest noting down the username and password somewhere, like the Notepad app. After you create the agent, click on the Access tab, put the agent in a department, and give them a role. You can choose which ones to use based on the agent you create. Next, click on the Permissions tab and adjust those accordingly. Finally, click the Teams tab and put the agent in one of the Teams we created earlier. Either Level 1 or Level 2 support. You can create as many agents as you want. <a href="https://docs.osticket.com/en/latest/Admin/Agents/Agents.html" target="_blank"> Documentation</a></h3>
<br />
<p>
  <img src="https://i.postimg.cc/SNC5zTG9/Add-New-User.png"height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">Next, lets create a couple of users(customers). You need to switch to the Agent Panel to create Users before you proceed. Agent Panel -> Users -> Add New. Again, just give them whatever email you want, put in a full name, and leave the rest empty. When you click on User Directory, you should see the new users you have created.<a href="https://docs.osticket.com/en/latest/Agent/Users/User%20Directory.html#add-new-users" target="_blank"> Documentation</a></h3>
<br />
<p>
  <img src="https://i.postimg.cc/wMNwn71b/Add-New-SLAPlan.png" height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">We must set up a few SLAs now. SLA (Service Level Agreement) in osTicket exists to provide a length of time in which the help desk admin expects tickets to be closed. You will need to switch back to the Admin Panel for this step. Admin Panel -> Manage -> SLA -> Add New SLA Plan.<a href="https://docs.osticket.com/en/latest/Admin/Manage/SLA%20Plans.html" target="_blank"> Documentation</a></h3>
<br />
<p>
	<div align="center">
  		<img src="https://i.postimg.cc/Hx4ZwHW7/Sev-A.png" alt="Image 1" height="75%" width="33%">
  		<img src="https://i.postimg.cc/0rgz9gmc/Sev-B.png" alt="Image 2" height="75%" width="33%">
  		<img src="https://i.postimg.cc/HxqMk71w/Sev-C.png" alt="Image 3" height="75%" width="33%">
	</div>
 
</p>
<br/>
<h3 align="center">The first SLA I made is Sev-A, which has a grace period of 1 hour and a schedule of 24/7. Something that would fit into this SLA is a server outage or some other business-critical problem. Something that would need to be solved quickly. The second SLA I made is Sev-B, which has a grace period of 4 hours and a schedule of 24/7. Something that would fit into this SLA is a failed backup or some other high-priority but not business-critical problem. The third SLA I made is Sev-C, which has a grace period of 8 hours and a business hours schedule. Moderate to low-priority issues fall into this SLA. Something like a password reset or the printer not working.</h3>
<br/>
<p>
  <img src="https://i.postimg.cc/pTsThJLZ/Help-Topic-Options.png" height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">Lastly, we'll create some help topics for the users to choose when creating a ticket. Admin Panel -> Manage -> Help Topics -> Add New Help Topic. You can create whatever help topics you want, but I will give you a few for reference. Business Critical Outage, Personal Computer Issues, Equipment Request, and Password Reset. By clicking on the "New ticket options" tab, you can change the Department and Priority of the topics. A password reset won't have the same priority as a business-critical outage, so it's important to adjust the priority and department to which the topic belongs. <a href="https://docs.osticket.com/en/latest/Admin/Manage/Help%20Topic.html" target="_blank"> Documentation</a></h3>
