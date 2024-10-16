# Active-Directory-Project
[Brief Objective - Remove this afterwards]

The Active Direcory Porject is designed to get hands on practice to build a fully functional domain environment. The project includes setting up and managing an AD environment, user and group management, security practices, and best practices for administration. 

Skills Learned


Strengthened understanding of SIEM concepts and injestion.
Information Technology (IT) administration through AD.
Ability to generate and recognize attack signatures and patterns.
Enhanced knowledge of network IPs and communication between them.
Creating telemetry amongst multiple virtual machines.
Tools Used


Splunk Security Information and Event Management (SIEM) system for log ingestion and analysis.
Active Directory for management and security of users in an environment.
Telemetry generation tools to mimic legitimate traffic.
Crowbar to attempt to brute force accounts.
Atomic Red Team to gain information about potential vulnerabilities on machine.
Steps


Step 1: Created four (4) virtual machines and manually assigned a static IP to each machine
Windows 10 Target PC: DHCP
Splunk Server: 192.168.10.10
Active Directory: 192.168.10.7
Kali Attacking Machine: 192.168.10.250



Step 2: Installed and configured Splunk on the Splunk server granting access to the Splunk Enterprise website.



Step 3: Installed and configured Splunk Universal Forwarder and Sysmon on both the target machine as well as the Active Directory server to create telemetry between the machines.



Step 4: Created a new domain in which new organizational units and users were generated.



Step 5: Changed domain on target machine to newly created domain and signed in with new user account.



Step 6: Enabled Remote Desktop Protocol (RDP) on target machine.



Step 7: Created a document with common passwords and added the password of the newly created user account. Then installed Crowbar, to successfully brute force password.





Step 8: Installed Atomic Red Team with Powershell on target machine to identify gaps in visibility.





