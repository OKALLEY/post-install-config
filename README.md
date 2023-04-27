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
<li>Go to Admin Panel -> Agents -> Add New <img src="https://imgur.com/MSvSyRa.png" height=".05%" width=".05%" alt="Disk Sanitization Steps"/> </li>
