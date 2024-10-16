<h1>Active Directory Project</h1>

<h2>Objective</h2>
The Active Directory (AD) Project is designed to get hands-on practice to build a fully functional domain environment. The project includes setting up and managing an AD environment, user and group management, security practices, and best practices for administration. 
<br />


<h2>Skills Learned</h2>

- <b>Strengthened understanding of SIEM concepts and ingestion.</b> 
- <b>Information Technology (IT) administration through AD.</b>
- <b>Ability to generate and recognize attack signatures and patterns.</b>
- <b>Enhanced knowledge of network IPs and communication between them.</b>
- <b>Creating telemetry amongst multiple virtual machines.</b>

<h2>Tools Used </h2>

- <b>Splunk Security Information and Event Management (SIEM) system for log ingestion and analysis.</b>
- <b>Active Directory for management and security of users in an environment.</b>
- <b>Telemetry generation tools to mimic legitimate traffic.</b>
- <b>Crowbar to attempt to brute force accounts.</b>
- <b>Atomic Red Team to gain information about potential vulnerabilities on machines.</b>

<h2>Project Walkthrough:</h2>

**Step 1:** Created four (4) virtual machines and manually assigned a static IP to each machine:

- Windows 10 Target PC: DHCP
- Splunk Server: 192.168.10.10
- Active Directory: 192.168.10.7
- Kali Attacking Machine: 192.168.10.250

![ad ipv4 upd](https://github.com/user-attachments/assets/4dff52ca-6b65-4763-89a9-02e28c821156)

![kali ipv4](https://github.com/user-attachments/assets/fb37030a-5114-4766-9203-abdce3347958)


**Step 2:** Installed and configured Splunk on the Splunk server granting access to the Splunk Enterprise website.


**Step 3:** Installed and configured Splunk Universal Forwarder and Sysmon on both the target machine as well as the Active Directory server to create telemetry between the machines.

![Inputs](https://github.com/user-attachments/assets/c5f6e7a3-38ba-46ea-a17e-5facdb9d358b)


**Step 4:** Created a new domain in which new organizational units and users were generated.

![ad user](https://github.com/user-attachments/assets/bb93e76c-50e8-4c6a-8689-8c0eb778c87e)


**Step 5:** Changed domain on target machine to newly created domain and signed in with new user account.

![jennysmith login](https://github.com/user-attachments/assets/0659fc0f-6536-465e-936d-e83272e839c0)


**Step 6:** Enabled Remote Desktop Protocol (RDP) on target machine.

![allow rdp](https://github.com/user-attachments/assets/404a37cf-42f8-41d6-bc58-6be50ee57f9e)


**Step 7:** Created a document with common passwords and added the password of the newly created user account. Then installed Crowbar, to successfully brute force password.

![passwordstxt](https://github.com/user-attachments/assets/0daa2360-af42-48f2-9e1b-37a798d9b334) ![rdp success](https://github.com/user-attachments/assets/d730e053-f56d-40f7-a547-84c3a2bf1658)![tsmith failed](https://github.com/user-attachments/assets/39997b5b-d92b-490a-aabd-6d58c68d46ef)


**Step 8:**  Installed Atomic Red Team with Powershell on target machine to identify gaps in visibility.

![NewLocal User ss](https://github.com/user-attachments/assets/6c7cb84f-5ade-4ed1-bce6-bcb920ad530c)


**Step 9:** Continued to monitor and review Splunk events.

![splunkmonit](https://github.com/user-attachments/assets/c2c9cda8-b21e-468e-bd7d-13fe96be1430)

