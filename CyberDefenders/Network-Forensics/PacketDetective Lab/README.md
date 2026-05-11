**Tools Used: Wireshark** <br><br><br>

Q1. The attacker’s activity showed extensive SMB protocol usage, indicating a potential pattern of significant data transfer or file access.
What is the total number of bytes of the SMB protocol?  <br>

A. In Traffic-1.pcapng, Navigate to Statistics tab -> Protocol Hierarchy -> SMB - ( 4406 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1524" height="214" alt="image" src="https://github.com/user-attachments/assets/f798944d-7455-431a-af30-8b5304d8c062" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q2. Authentication through SMB was a critical step in gaining access to the targeted system. Identifying the username used for this authentication will help determine if a privileged account was compromised.
Which username was utilized for authentication via SMB? <br>

A. Navigate to Edit tab -> Find Packet -> Packet Details, string -> search for auth - ( Administrator )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1870" height="651" alt="image" src="https://github.com/user-attachments/assets/e4527c0f-fd14-4fe4-b1a6-0dda7c9b8d01" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q3. During the attack, the adversary accessed certain files. Identifying which files were accessed can reveal the attacker's intent.
What is the name of the file that was opened by the attacker? <br>

A. Naviagte through the SMB traffic and keep an eye on Info tab in the wireshark - ( eventlog )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1870" height="651" alt="image" src="https://github.com/user-attachments/assets/804883c5-e684-4d58-a8aa-f707820ab823" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q4. Clearing event logs is a common tactic to hide malicious actions and evade detection. Pinpointing the timestamp of this action is essential for building a timeline of the attacker’s behavior.
What is the timestamp of the attempt to clear the event log? (24-hour UTC format) <br>

A. Search for eventlog and check for the timestamp of the event log request - ( 2020-09-23 16:50 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1870" height="485" alt="image" src="https://github.com/user-attachments/assets/30b74737-17dd-490d-b7b0-263c75d4f11d" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q5. The attacker used "named pipes" for communication, suggesting they may have utilized Remote Procedure Calls (RPC) for lateral movement across the network. RPC allows one program to request services from another remotely, which could grant the attacker unauthorized access or control.
What is the name of the service that communicated using this named pipe? <br>

A. In Traffic-2.pcapng, filter out the protocol DCERPC and then follow TCP stream and for better visibility use UTF-16 - ( atsvc )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1870" height="485" alt="image" src="https://github.com/user-attachments/assets/5788b28b-7d1a-439a-9ef1-fb47504e5bcb" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q6. Measuring the duration of suspicious communication can reveal how long the attacker maintained unauthorized access, providing insights into the scope and persistence of the attack.
What was the duration of communication between the identified addresses 172.16.66.1 and 172.16.66.36? <br>

A. Navigate to the Statistics tab -> Conversations -> IPV4 -> Duraction of communication between 172.16.66.1 and 172.16.66.36 - ( 11.7247 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1858" height="260" alt="image" src="https://github.com/user-attachments/assets/ff147571-594c-4c2a-a3e2-676cc7b926b1" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q7. The attacker used a non-standard username to set up requests, indicating an attempt to maintain covert access. Identifying this username is essential for understanding how persistence was established.
Which username was used to set up these potentially suspicious requests? <br>

A. In Traffic-3.pcapng, Search in the info tab for User - ( backdoor )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1858" height="565" alt="image" src="https://github.com/user-attachments/assets/2e70047b-2265-4fef-b81c-8ffdc4ea8076" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q8. The attacker leveraged a specific executable file to execute processes remotely on the compromised system. Recognizing this file name can assist in pinpointing the tools used in the attack.
What is the name of the executable file utilized to execute processes remotely? <br>

A. Search in the Info tab for File name - ( PSEXESVC.exe )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1858" height="527" alt="image" src="https://github.com/user-attachments/assets/6364222b-aa48-4369-b6c4-a97114942957" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------
