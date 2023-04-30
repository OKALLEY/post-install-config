<p align="center">
<img src="https://camo.githubusercontent.com/f8ede6a7f4ad832bfd66a54f6912689d1ef080eb15e2b64b7ca43306d648395d/68747470733a2f2f696d6775722e636f6d2f4f7771396c4f562e706e67"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Links (to be used inside your VM):</h2>
<li>Help Desk Login Page: http://localhost/osTicket/scp/login.php</li>
<li>End Users osTicket URL: http://localhost/osTicket/</li>

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles
- Configure Departments
- Configure Teams
- Allow anyone to create tickets
- Configure Agents (workers)
- Configure Users (customers)
- Configure SLA
- Configure Help Topics

<h2>Configuration Steps</h2>
<li>Sign in to Azure - portal.azure.com/</li>
<li>In Azure under Virtual Machines find and click your virtual machine. Locate its Public IP address. Click to copy it.</li>
<img src="https://imgur.com/FH3XIuY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<li>In Windows click start and type: Remote Desktop Connection. (Mac users install Microsoft Remote Desktop)</li>
<img src="https://imgur.com/OzCsluN.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<h2>Help Desk Login Page: http://localhost/osTicket/scp/login.php</h2>
<li>Within the VM Sign into osTicket using your Admin Username or Email Address and Password</li>
<p>
<img src="https://imgur.com/aeD0fjj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h2>Configure <a href="https://docs.osticket.com/en/latest/Admin/Agents/Roles.html">Roles</a></h2>
<li>Click the Admin Panel -> hover over Agents ->  select Roles</li>
<img src="https://imgur.com/3h69TS0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/M9r1ReY.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>
<p>
<li>Here you will see built in rules already established.</li>
<li>To get a sense of the environment create another one: click "Add New Role"</li>
<img src="https://imgur.com/DT5hQeo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<li>Your organization may only want target specific permissions assigned. <br> Go through Tickets, Tasks and Knowledgebase and select the appropriate permissions</li> <li>Once you're finished adding permissions click "Add Role"</li> 
<img src="https://imgur.com/BZEjd4A.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
  
<h2>Configure <a href="https://docs.osticket.com/en/latest/Admin/Agents/Departments.html">Departments</a></h2>
<li>Go to Admin Panel -> Agents -> Departments <img src="https://imgur.com/36rS45y.png" height=".02%" width=".02%" alt="Disk Sanitization Steps"/> </li>
<li>Click "Add New Department"</li>
<img src="https://imgur.com/vf9uZ4P.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p> 
<li>Create a Top-Level Deapartment with the Name: System Administrators</li>
<img src="https://imgur.com/7LC93zC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/2LGSwEj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
<h2>Configure <a href="https://docs.osticket.com/en/latest/Admin/Agents/Teams.html">Teams</a></h2>
<li>Go to Admin Panel -> Agents -> Teams <img src="https://imgur.com/wyWG747.png" height=".02%" width=".02%" alt="Disk Sanitization Steps"/></li>
<li>Click "Add New Team"</li>
<img src="https://imgur.com/mv0xRYp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<li>Name the team</li>
<img src="https://imgur.com/CasWCx3.png" height="50%" width="50%" alt="Disk Sanitization Steps"/> 
<li>Under "Members", add yourself to the Team</li>    
<img src="https://imgur.com/d1OgxeP.png" height="50%" width="50%" alt="Disk Sanitization Steps"/> 
<h2>Allow Anyone To Create Tickets</h2>  
<li>Go to Admin Panel -> Settings -> Users</li>
<img src="https://imgur.com/oeZ1uec.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>
<li> Where it reads "Registration Required" make sure the box is unchecked</li>
<img src="https://imgur.com/5CChuNB.png" height="55%" width="55%" alt="Disk Sanitization Steps"/>

<h2>Configure <a href="https://docs.osticket.com/en/latest/Admin/Agents/Agents.html">Agents(workers)
</a></h2>
<li>Go to Admin Panel -> Agents -> Add New Agent <img src="https://imgur.com/MSvSyRa.png" height=".05%" width=".05%" alt="Disk Sanitization Steps"/> </li>
Here you will make two agents: Jane Doe as a System Administrator and then John Doe
<li>Enter the Agent's Name, Email Address and Username then click "Set Password"</li>
<img src="https://imgur.com/iREagx4.png" height="55%" width="55%" alt="Disk Sanitization Steps"/>
FOR THIS TUTORIAL ONLY:
<li>Uncheck the box for: Send the agent a password reset email</li>
<li>Create a password and confirm</li>
<li>Uncheck the box for: Require password change at next login</li>
<li>Click "Set"</li>
<img src="https://imgur.com/lMbIZVN.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<p>
<li>Under Access assign: "System Administrator" and "Imperial Admin" and "Support"</li<>  
<img src="https://imgur.com/IFqw9g0.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>  
<li>Under Teams assign: Level II Support and click "Create"</li>  
<img src="https://imgur.com/ULNCyMG.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>  

Repeat these steps again for John Doe, but in Access assign "Support" and "View only" under Primary Department*
<img src="https://imgur.com/TroMTLQ.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<h2>Configure <a href="https://docs.osticket.com/en/latest/Agent/Users/User%20Directory.html">Users (customers)
</a></h2>

Here we will create two users: Karen and Ken
<p>
Remember to switch from Admin Panel to the Agent Panel <img src="https://imgur.com/r75IgS3.png" height="15%" width="15%" alt="Disk Sanitization Steps"/>
<li>Go to Agent Panel -> Users -> Add New</li>
<li>Enter a email address and name then click "Add User"</li>  
<img src="https://imgur.com/NK75Ny9.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<li>When finished clickinG "Users" will bring you back to the screen to click "Add User" once again.</li>
<img src="https://imgur.com/0cihKqy.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>  


<h2>Configure <a href="https://docs.osticket.com/en/latest/Admin/Manage/SLA%20Plans.html">SLA</a></h2>
Here you will create 3 SLA plans:

<br>
<ul>
<li type =circle>Sev-A (1 hour, 24/7)<br>
<li type =circle>Sev-B (4 hours, 24/7)<br>
<li type =circle>Sev-C (8 hours, business hours)
</ul>

<li>Go to Admin Panel -> Manage -> SLA</li>
<img src="https://imgur.com/0tIty4e.png" height="15%" width="15%" alt="Disk Sanitization Steps"/>
<li>Find and click "Add New SLA Plan"</li>
<img src="https://imgur.com/jEi1arl.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
 
<li>Create Sev-A with a 1 hour grace Period and a Schedule of 24/7.
<li>Click "Add Plan"</li>  
NOTE: This means that if a Sev-A comes through Sunday night at 10pm it needs to be resolved by 11pm</li>  
  <img src="https://imgur.com/VHDQ5Wh.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>

<p>
  
<li>Next Click "Add New SLA Plan" and create
Sev-B with a 4 hour grace Period and a Schedule of 24/7</li> 
NOTE: This means that if a Sev-B comes through Saturday morning at 2am it needs to be resolved by 6am</li>  

<img src="https://imgur.com/ltMdQbj.png" height="70%" width="70%" alt="Disk Sanitization Steps"/> 
<li>NOTE: This means that if a Sev-C comes through Friday 3pm<br>there are 2 business hours left Friday and another 6 hours Monday starting at 8am to resolve this ticket.</li>  
<img src="https://imgur.com/mxOjHWN.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>

<h2>Configure <a href="https://docs.osticket.com/en/latest/Admin/Manage/Help%20Topic.html">Help Topics</a></h2>
Here you will create the following new Help Topics:<br>
<ul>
  <li type =circle>Business Critical Outage<br>
  <li type =circle>Personal Computer Issues<br>
  <li type =circle>Equipment Request<br>
  <li type =circle>Password Reset
    
</ul>    

<p>
      
<li> Go to Admin Panel -> Manage -> Help Topics</li>
<li>Here you will see the default Help Topics. Click "Add New Help Topic"</li>
<img src="https://imgur.com/70F1TtB.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<li>In the topic section type "Business Critical Outage" and click "Add Topic"</li>
<img src="https://imgur.com/cyuvt5M.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<li>Click "Help Topics" and continue to do this for all four making each one a "Parent Topic":
  <ul>
  <li type =circle>Business Critical Outage<br>
  <li type =circle>Personal Computer Issues<br>
  <li type =circle>Equipment Request<br>
  <li type =circle>Password Reset</li>  
  </ul>
