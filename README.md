<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

# osTicket - System Administration Configuration
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

## Environments and Technologies Used

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- [osTicket Documentation (View Panel)](https://docs.osticket.com/en/latest/index.html)

## Operating Systems Used

- Windows 10</b> (21H2)
- MacOS Ventura 13.0.1

## List of System Administration Configurations

1. [Helpdesk Roles](https://github.com/reynaldomata/post-install-config#configure-helpdesk-roles)
2. [Helpdesk Departments](https://github.com/reynaldomata/post-install-config#configure-helpdesk-departments)
3. [Helpdesk Teams](https://github.com/reynaldomata/post-install-config#configure-helpdesk-teams)
4. [Helpdesk Agents](https://github.com/reynaldomata/post-install-config#configure-helpdesk-agents)
5. [Helpdesk SLA (Service Level Agreements)](https://github.com/reynaldomata/post-install-config#configure-helpdesk-sla)
6. [Help Topics](https://github.com/reynaldomata/post-install-config#configure-help-topics)
7. [Helpdesk Users](https://github.com/reynaldomata/post-install-config#configure-helpdesk-users)

## Configuration Steps

### Configure Helpdesk Roles
>**Note:**
>osTicket Roles are a specific set of permissions assigned to helpdesk employees based on the department they are associated with. Organizations can create an unlimited number of roles.

<p>

https://github.com/dtaylor15/osTicket-SystemAdmin-Config/assets/101889571/9d68abda-7acb-46f6-9eb0-0c0c4544b6ab

</p>

<p>
Login with the Admin User credentials configured during installation. 
  
Arrive at Roles: Admin panel -> Agents -> Add new role -> Name the role -> Set the appropriate permissions based on your organization.
</p>
<br />

### Configure Helpdesk Departments
>**Note:**
> Tickets are routed through departments in the helpdesk. Several settings can be configured for each department.

<p>
<img width="501" alt="config_departments" src="https://github.com/dtaylor15/osTicket-SystemAdmin-Config/assets/101889571/7e2dd3b2-5a5a-40b8-9cee-32ced8d912e3">

</p>

<p>
Arrive at Departments: Admin panel -> Agents -> Department -> Complete fields based on your organization. 

For this example, I created a System Administration Department and made myself the manager. I provided this department with  full control of the ticketing system. I set my schedule to 24/7 to allow access during non-operation hours, for emergencies.
</p>
<br />

### Configure Helpdesk Teams
>**Note:**
>Teams organizes helpdesk employees from various departments enabling them to address specific issues or users via Help Topics or Ticket Filters.

<p>
<img width="958" alt="ost_teams" src="https://github.com/dtaylor15/osTicket-SystemAdmin-Config/assets/101889571/ecce4b04-77ba-4a73-9ee3-ff08290e39f8">

<img width="682" alt="addteams" src="https://github.com/dtaylor15/osTicket-SystemAdmin-Config/assets/101889571/2f04a73b-0ce8-4977-80a1-9e33c0d18674">

</p>

<p> Arrive at Teams: Admin panel -> Agents -> Add new team -> Name your team -> Save changes

For this example, I added two teams: Level 1 suppport and Level 2 support (not shown).
</p>
<br />

### Configure Helpdesk Agents
>**Note**
>osTicket Agents are the helpdesk employees. They service each ticket submitted to the system.

<p> 

https://github.com/dtaylor15/osTicket-SystemAdmin-Config/assets/101889571/10c18eca-d9ef-44f5-be29-867fa3dad46e
</p>

<p> Arrive at Agents: Admin panel -> Agents -> Add new agent -> Enter employee creditials -> Set password -> Set -> Access -> Configure department -> Configure Permissions and Teams applicable to your organization.

For this example, I set a passowrd for this sample agent so I can log in and tutorial a ticket lifecycle. However, standard operations in many organizations require the agent to set their own password at intial log in. <p/>
<br /> 

### Configure Helpdesk SLA
>**Note:**
>Service Level Agreements (SLA) outlines a specific length of time in which administrators expect tickets to be resolved. SLAs are commonly determined by the severity of the reported issue (i.e., how impactful the problem is to business operations)

<p> 

https://github.com/dtaylor15/osTicket-SystemAdmin-Config/assets/101889571/3e553421-7b08-4d52-81db-4b951c49806b

</p>

<p> Arrive at SLA Plans: Admin panel -> Manage -> SLA -> Add new SLA plan -> Name your service levels and configure according to your organization's standards.

For this example I used service levels (severity) SEV-A, SEV-B, SEV-C with SEV-A being the most severe (impactful on business operations). For SEV-A I set a grace period for 1 hour, this indicates that the ticket must be closed within 1 hour of receving. I set the schedule to 24/7 allowing the ticket to be addressed after hours for emergencies. 
</p>
<br />

### Configure Help Topics 
>**Note:**
>Help Topics are used to efficiently catergorize tickets. They assist in directing tickets to specific departments and determining the ticket's configurations, including SLAs and priority levels.

<p> 
<img width="957" alt="ost_helptopic" src="https://github.com/dtaylor15/osTicket-SystemAdmin-Config/assets/101889571/7237df05-34ec-4af2-a851-615120184542">

<img width="955" alt="completedhelptopics" src="https://github.com/dtaylor15/osTicket-SystemAdmin-Config/assets/101889571/1e98b5c6-fb4d-438b-8e22-da11112bae2d">
</p>

<p> Arrive at Help Topics: Admin Panel -> Manage -> Help Topics -> Add new help topic -> Configure according to your organization's standards.

For this example, I used three topics: Business Critical Outage, Personal Computer Issues, Equipment Requests, and Password Reset. I configured "Business Critical Outage" tickets to be automatically categorized with a SEV-A SLA plan. These types of tickets are automatically assigned to the system admin.  </p>

<br />

### Configure Helpdesk Users
>**Note**
> Helpdesk users are the organization's employees and/or customers who will be submitting tickets. Users can be guests or registered in osTicket. Registered users can login or use their email to track their ticket's progress and view submission history.

<p> 

https://github.com/dtaylor15/osTicket-SystemAdmin-Config/assets/101889571/a7c7185c-0ec6-4a43-9dfc-fe3d0072b9a6

</p>

<p> Arrive at Users: Agent panel -> Users -> Add new user -> input user's credentials -> Register -> Set a password or enable the user to set one themselves. </p>


### osTicket - System Administration Configuration Complete!👏🏾
Continue to [helpdesk ticket lifecycle examples.](https://github.com/reynaldomata/osTicket-LifeCycle)
