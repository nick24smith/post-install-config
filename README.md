<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Configuration Steps</h2>

Access the Admin and Agent Panels. You'll need to access the Admin login page and the end user page for users to submit their tickets. Admin Login: http://localhost/osTicket/scp/login.php
End User Ticket Portal:  http://localhost/osTicket

<img width="545" height="411" alt="image" src="https://github.com/user-attachments/assets/41dd8938-a248-4568-ad4d-91c7b24a477f" />

<img width="1015" height="387" alt="image" src="https://github.com/user-attachments/assets/c691ab64-8948-445e-ad87-a6b89810ad53" />

Agent Panel vs Admin Panel - Agent Panel is used by support agents to handle tickets. Admin Panel gives you full control of osTicket.

<img width="1188" height="860" alt="image" src="https://github.com/user-attachments/assets/ba386f7a-2eab-48ec-b500-db9f740d5854" />

<img width="1196" height="431" alt="image" src="https://github.com/user-attachments/assets/4faa749a-e170-442f-8d30-c952d085addd" />

Configure Roles: Admin Panel -> Agents -> Roles. We're going to create a Supreme Admin, give it permission to everything in the "tickets" and "tasks" tabs.

<img width="410" height="43" alt="image" src="https://github.com/user-attachments/assets/1b677aff-e2fd-4c63-b2c9-4895b6872bd0" />


<img width="1206" height="513" alt="image" src="https://github.com/user-attachments/assets/e0d28a5a-efac-402e-ae70-fe1a7c5f6cd2" />

<img width="471" height="236" alt="image" src="https://github.com/user-attachments/assets/16df4774-4945-43a8-bdb5-539d4bf9a5c2" />

<img width="619" height="467" alt="image" src="https://github.com/user-attachments/assets/31ec8115-01c6-4593-86d1-75e5e6e032b8" />

<img width="509" height="304" alt="image" src="https://github.com/user-attachments/assets/c1544b6a-dd14-4d1a-9a10-bb3f916e11e2" />

Configure Departments: Admin Panel -> Agents -> Departments. We're creating a Support/System Admins Department (SysAdmins).

<img width="1052" height="116" alt="image" src="https://github.com/user-attachments/assets/88c8128d-cc6e-4ae6-86fa-c5ed36c2b51c" />

<img width="700" height="899" alt="image" src="https://github.com/user-attachments/assets/459d22e6-9e73-466c-8b9e-df5cde24a05f" />
>

<img width="497" height="252" alt="image" src="https://github.com/user-attachments/assets/573fe999-bd9c-41bf-8ff6-de48a7c563e6" />

Configure Teams: Admin Panel -> Agents -> Teams. In this example, we're creating an 
"Online Banking" team. 

<img width="1175" height="225" alt="image" src="https://github.com/user-attachments/assets/4a5a1793-b566-4375-9474-692ec16ef83c" />

<img width="614" height="351" alt="image" src="https://github.com/user-attachments/assets/9dafd55d-886b-4de6-9d26-63f19fd23852" />

Allow everyone to create tickets: Admin Panel -> Settings -> User Settings. Make sure that “Require registration and login to create tickets” is UNCHECKED.

<img width="850" height="646" alt="image" src="https://github.com/user-attachments/assets/79beee3d-b5f2-491a-91bb-5626d6b4e6e3" />

Configure Agents (workers) -> Admin Panel -> Agents -> Add New. We're making 2 agents, one for the SysAdmins Dept. and one for the Support Dept. Below is Jane for SysAdmins. Follow the same steps for the Support Dept. agent except give the Support Dept. VIEW Access instead of Supreme Admin. 

<img width="1071" height="278" alt="image" src="https://github.com/user-attachments/assets/f91b66e8-f903-4f90-aa73-acb28608f009" />

<img width="897" height="408" alt="image" src="https://github.com/user-attachments/assets/d5cf0abc-ef60-406c-8806-4b23de2b3da7" />

<img width="460" height="240" alt="image" src="https://github.com/user-attachments/assets/52fac57c-b5c0-494d-aff8-ccb74dddf162" />

<img width="540" height="286" alt="image" src="https://github.com/user-attachments/assets/c2b424ca-831e-4c9d-a435-5aba3024fe52" />

<img width="295" height="138" alt="image" src="https://github.com/user-attachments/assets/9e3b5bae-7dfc-4429-8d21-96542b72f0af" />

Configure Users (Customers): Swap to Agent Panel -> Users -> Add New

<img width="952" height="252" alt="image" src="https://github.com/user-attachments/assets/ad554b87-3eff-4052-b8a4-107d72e24243" />

<img width="801" height="359" alt="image" src="https://github.com/user-attachments/assets/b1d1d4ea-0810-4c9e-b8e3-fb8eac7ae511" />

Configure SLA: Admin Panel -> Manage -> SLA. Sev-A (Grace Period: 1 Hour, Schedule: 24/7), Sev-B (Grace Period: 4 Hours, Schedule: 24/7), Sev-C (Grace Period: 8 Hours, Schedule: Business Hours M-F)

<img width="1180" height="232" alt="image" src="https://github.com/user-attachments/assets/f5a90017-78d2-4fff-8e51-deacc9743ae3" />

<img width="968" height="389" alt="image" src="https://github.com/user-attachments/assets/c68056a8-361c-45a9-afcc-4d731f3602a2" />

<img width="496" height="196" alt="image" src="https://github.com/user-attachments/assets/833f324e-d122-446d-aee6-a2fdf691fa59" />

<img width="503" height="199" alt="image" src="https://github.com/user-attachments/assets/a7b181d9-61e9-476a-9a97-ba9bc40afa76" />

Configure Help Topics (This is for users when they create tickets): Admin Panel -> Manage -> Help Topics -> Add New. The list of topics we're creating are: Business Critical Outage, Personal Computer Issues, Equipment Request, Password Reset, and Other. 

<img width="539" height="317" alt="image" src="https://github.com/user-attachments/assets/b47de7d6-9631-4d7a-9c91-42ab5c507ac5" />

<img width="455" height="211" alt="image" src="https://github.com/user-attachments/assets/dccdadce-818d-4257-9c5e-6dd255fdd08f" />

<img width="519" height="137" alt="image" src="https://github.com/user-attachments/assets/c02d6b3b-b325-4aa9-9667-d76b9b64aa0a" />

<img width="515" height="142" alt="image" src="https://github.com/user-attachments/assets/6c858b1e-df5e-42fa-8998-4460c10d79c2" />

<img width="511" height="126" alt="image" src="https://github.com/user-attachments/assets/17cbe7cb-7849-420f-acb9-e71eabf1d294" />

<img width="902" height="386" alt="image" src="https://github.com/user-attachments/assets/b5bb3a71-6a35-472a-8945-53b2c2af36d3" />
