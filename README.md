<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- osTicket

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure New Roles, Departments, and Teams
- Allow Anyone to Create Tickets
- Configure New Agents and Users
- Configure new SLAs (Service Level Agreements)
- Configure New Help Topics

<h2>Configuration Steps</h2>


![image](https://github.com/jamstylr/post-install-config/assets/159660523/33bb2a50-d955-4da7-aee2-f09e473d2922)

<p>
After successfully installing osTicket, you're ready to configure it as a ticketing system. To begin, open your web browser and navigate to http://localhost/osTicket/scp/login.php. Here, you can log in to your Help Desk portal using the credentials you created during the installation process. Once logged in, you'll gain access to various ticket management features and administrative settings.
</p>
<br />


![image](https://github.com/jamstylr/post-install-config/assets/159660523/00ebfbea-d2b2-497a-939e-9c056f043f03)

<p>
In the top right corner of the osTicket interface, you'll find options to switch between the Admin Panel and Agent Panel. Simply click on the displayed panel name, either “Admin Panel” or “Agent Panel”, to switch between them. If you see “Agent Panel”, it indicates that you're currently accessing osTicket as an administrator. Conversely, if “Admin Panel” is displayed, you're in the Agent Panel interface. Each panel offers distinct functionalities tailored to administrative tasks and agent operations.
</p>
<br />

![image](https://github.com/jamstylr/post-install-config/assets/159660523/8573d4fa-a215-410b-a65b-c741937a7f26)
![image](https://github.com/jamstylr/post-install-config/assets/159660523/641b475c-b28f-4d9e-9811-5f36fb8b342d)
![image](https://github.com/jamstylr/post-install-config/assets/159660523/b9eed2e5-10ab-4815-98fc-577f81204f65)
<p>
Roles specify the permissions assigned to agents within the departments they are granted access to. First we will create a new role called Supreme Admin that will be granted all permissions. To do this, you will need to be in the Admin Panel. Then go to Agents->Roles->Add New Role. Name the Supreme Admin, and then click on the “Permissions” tab. To grant this role all permissions, check all the boxes under the Tickets, Tasks, and Knowledgebase tabs. Finally click “Add Role” and save changes.
</p>
<br />

![image](https://github.com/jamstylr/post-install-config/assets/159660523/8c499b25-4998-401c-91ad-396fb1042df4)
<p>
Departments help organize and solve tickets based on their importance or instructions, and each agent is assigned to a specific department based on their role within the Help Desk. To create a new department for System Administrators, navigate to the Admin Panel and select Agents -> Departments -> Add New Department. Name the department “System Administrators”, keep other options as default, and click "Create Dept" to finalize.
</p>
<br />

![image](https://github.com/jamstylr/post-install-config/assets/159660523/18f81d8e-227c-444a-bf15-3f8fcb0607eb)
![image](https://github.com/jamstylr/post-install-config/assets/159660523/a331752b-98de-4b2c-9ee0-3a1f0199734f)
<p>
Next we will set up a new team. The Teams section in osTicket organizes agents from different departments to handle specific issues and override parameter rules, allowing for specialized teams like an "A team" with top technicians from various departments. By default, osTicket creates a Level I Support Team, so we will create a Level II Support Team. From the Admin Panel go to Agents->Teams->Add New. Name it “Level II Support”, then click on the Members tab to add new members (I added myself). Now click Create Team.
</p>
<br />

![image](https://github.com/jamstylr/post-install-config/assets/159660523/fc9ddd36-d1d2-4995-aa73-511c2db353ae)
<p>
To allow anyone to create tickets anonymously, from the Admin Panel go to Settings->User Settings. Under Authentication Settings, make sure that the “Registration Required” box in unchecked. By unchecking this box, users can create anonymous tickets when necessary.
</p>
<br />

![image](https://github.com/jamstylr/post-install-config/assets/159660523/3810b28d-45c0-4abb-9cd5-61c1ab7a80b7)
![image](https://github.com/jamstylr/post-install-config/assets/159660523/a3c5193e-3dbb-4c31-86fa-3b471fdfb8c0)
![image](https://github.com/jamstylr/post-install-config/assets/159660523/d6fb6345-5331-47d6-8e64-7f83d65fbd91)
![image](https://github.com/jamstylr/post-install-config/assets/159660523/40a1bb76-e654-4161-a352-adee477f66ce)
<p>
Moving forward, we'll create new agents representing the employees tasked with resolving tickets. To create new agents, from the Admin Panel go to Agents->Add New Agent. For this tutorial, we will create two new agents Jane Doe and John Doe. We will give them basic usernames, emails, and passwords. When setting their passwords, uncheck the boxes next to "Send the agent a password reset email" and "Require password change at next login”. In the Access tab, you have the option to assign an agent to a department and role, while also being able to assign them to a specific team in the Teams tab. Additionally, within the Permissions tab, you have the ability to configure permissions. For the purposes of this tutorial, we will set Jane Doe with the role of Supreme Admin.
</p>
<br />

![image](https://github.com/jamstylr/post-install-config/assets/159660523/a8792956-67c9-4d72-9c9f-0c262bfeb74e)
![image](https://github.com/jamstylr/post-install-config/assets/159660523/fdc98527-abbf-45df-8785-f35d70918f98)
![image](https://github.com/jamstylr/post-install-config/assets/159660523/1438000d-4926-4eec-978d-47163008d930)
<p>
After creating agents, the next step is to create users. Users, in this context, refer to customers who generate tickets when they encounter issues. Each user is uniquely identified by their email address. To create new users, switch to the Agent Panel, navigate to the Users tab, and click on Add User. For this tutorial we will create two new users Ken Smith and Karen Smith. Give them simple emails such as ken@osticket.com and karen@osticket.com.
</p>
<br />

![image](https://github.com/jamstylr/post-install-config/assets/159660523/cd5b130c-4201-4279-9c49-610b95efe22c)
![image](https://github.com/jamstylr/post-install-config/assets/159660523/4675266b-981a-4be0-a3fd-47dad5da9e32)
<p>
Service Level Agreements (SLAs) outline the timeframe for administrators to close tickets, and they can also be designated for specific departments or help topics to ensure efficient handling. To create a new SLA, switch to the Admin Panel, go to Manage->SLA->Add New SLA Plan. For this tutorial we will create 3 new SLAs. The first SLA will be for the most severe tickets and will be ideal for addressing business critical issues. Give this first SLA the name SEV-A with a grace period of 1 hour and a 24/7 schedule. The second SLA will be ideal for resolving critical issues affecting employees, such as troubleshooting or PC problems. Give the second SLA the name SEV-B with a grace period of 4 hours and a 24/7 schedule. The third SLA will be named SEV-C. SEV-C is ideal for less critical issues or routine requests. SEV-C is less urgent compared to SEV-A and SEV-B, so we will give it a longer response time and tickets should only be addressed during business hours. SEV-C will need an 8 hour grace period and a business hours schedule.
</p>
<br />
