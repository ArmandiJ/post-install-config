<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computers)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Configuration Steps</h2>

- Log in to osTicket using the credentials you made during the installation tutorial


![image](https://github.com/ArmandiJ/post-install-config/assets/153237878/8a3b4288-c1d7-450f-823d-6425ee6ecb69)


<h2> Configure Roles </h2>

- Inside Admin Panel go to Agents tab then Roles and create a role named Supreme Admin and give the role every permission


![image](https://github.com/ArmandiJ/post-install-config/assets/153237878/4573fc58-9700-471a-a5c3-59388c74bdfc)


<h2> Configure Departments </h2>

- Inside Admin Panel go to Agents tab then Departments and create a department named System Administrators


![image](https://github.com/ArmandiJ/post-install-config/assets/153237878/8c748c6e-cf3b-418b-b145-3c3167e0edc7)


<h2> Configure Teams </h2>

- Admin Panel -> Agents -> Teams
Create a Level II Support Team and add yourself as a member to this team


![image](https://github.com/ArmandiJ/post-install-config/assets/153237878/32a622df-1e12-4c5f-b431-8a234575213e)


<h2> Allow anyone to create tickets </h2>

- Admin Panel -> Settings -> User Settings -> Make sure the following box is unchecked:  Registration Required: Require registration and login to create tickets 


![image](https://github.com/ArmandiJ/post-install-config/assets/153237878/e0299cf1-4118-4ac9-83ee-166b7ba9131d)


<h2> Configure Agents (workers) </h2>

- Admin Panel -> Agents -> Add New -> Create agents Jane and John
- Name: Jane Doe
- Email : jane.doe(@)osticket.com
- Username: jane.doe
- Click Set Password and uncheck the box that says "Send the Agent a Password Reset Email"
- Set your password to anything you like
- Uncheck the box that says "Require Password Change at Next Login"
- Select set
- Inside Access tab -> Select the Department dropdown menu -> System Administrators -> Select the Role dropdown menu -> Supreme Admin
- Inside Team tab -> Select Team dropdown menu -> Level II Support -> Select Add -> Select Create
- Extended Access -> Department dropdown menu -> Support -> Role dropdown menu -> Supreme Admin
![image](https://github.com/ArmandiJ/post-install-config/assets/153237878/7f442695-984c-496b-b56e-fb9e0cd8d864)


- Create another agent and replace Jane with John. Follow the same steps as above, except in Department dropdown menu -> Support and in Role dropdown menu -> View Only


![image](https://github.com/ArmandiJ/post-install-config/assets/153237878/b04d3ace-ce4c-4837-8ccd-da18abd4d165)


<h2>Configure Users (customers) </h2>

- Agent Panel -> Users -> Add Karen and Ken
- Email: Karen(@)osticket.com
- Full Name: Karen Karen
- Select Add User


![image](https://github.com/ArmandiJ/post-install-config/assets/153237878/dca66bb8-97f8-4b8e-873d-539c1fd1d221)


- Repeat steps for Ken just replace the name

<h2> Configure SLA </h2>

- We will create three SLAs
- Admin Panel -> Manage -> SLA
- Name: SEV-A
- Grace Period: 1
- Schedule dropdown menu: 24/7
- Select Add Plan


![image](https://github.com/ArmandiJ/post-install-config/assets/153237878/c375f5ad-f80e-4444-94a8-6bbba172a37b)


- 2nd SLA
- Name: SEV-B
- Grace Period: 4
- Schedule dropdown menu: 24/7
- Select Add Plan

- Last SLA
- Name: SEV-C
- Grace Period: 8
- Schedule dropdown menu: business hours
- Select Add Plan

<h2> Configure Help Topics </h2>

- Admin Panel -> Manage -> Help Topics
- Business Critical Outage
- Personal Computer Issues
- Equipment Request
- Password Reset

![image](https://github.com/ArmandiJ/post-install-config/assets/153237878/2e20a8a8-1ef6-40fc-b1ea-f6e77b75ae3e)
