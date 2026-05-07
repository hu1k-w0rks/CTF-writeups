**Tools Used: Wireshark, Windows Event Viewer** <br><br>

Q1. Knowing the source IP of the attack allows security teams to respond to potential threats quickly. Can you identify the source IP responsible for potential port scanning activity? <br>

A. Open pcap file -> Statistics -> Endpoints -> IPV4 -> Sort by highest Tx Packets - ( 87.96.21.84 )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1228" height="205" alt="image" src="https://github.com/user-attachments/assets/89178347-0a14-4b4a-9d28-641aa2d61c19" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q2. During the investigation, it's essential to determine the account targeted by the attacker. Can you identify the targeted account username? <br>

A. In the PCAP file -> Edit -> Find Packet select Packet Details and select string and search for username - ( sa )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1906" height="940" alt="image" src="https://github.com/user-attachments/assets/36c309da-007e-4433-a55c-56b9a7c5b96b" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q3. We need to determine if the attacker succeeded in gaining access. Can you provide the correct password discovered by the attacker? <br>

A. In the PCAP file -> Edit -> Find Packet select Packet Details and select string and search for password - ( cyb3rd3f3nd3r$ )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1907" height="935" alt="image" src="https://github.com/user-attachments/assets/b42e1b1f-6c9b-4d24-b463-ca99cd2b2edc" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q4. Attackers often change some settings to facilitate lateral movement within a network. What setting did the attacker enable to control the target host further and execute further commands? <br>

A. Open the TCP stream for the TDS login packet found previously - ( xp_cmdshell )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1916" height="939" alt="image" src="https://github.com/user-attachments/assets/7b9c2256-2d6e-469b-b80d-f44c84d16a1d" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q5. Process injection is often used by attackers to escalate privileges within a system. What process did the attacker inject the C2 into to gain administrative privileges? <br>

A. While navigating the event viewer logs this image looked suspicious as the Host name of the Host Application is unsual - ( winlogon.exe ) 

----------------------------------------------------------------------------------------------------------------------------------------
<img width="1309" height="935" alt="q5-bluesky" src="https://github.com/user-attachments/assets/f3bbc2e1-1e65-4d71-b8a8-1d4678c8a023" /> <br>

----------------------------------------------------------------------------------------------------------------------------------------

Q6. Following privilege escalation, the attacker attempted to download a file. Can you identify the URL of this file downloaded? <br>

A. search for HTTP requests with GET method and in packet details pane navigate to Full request UrI - ( http://87.96.21.84/checking.ps1 ) 

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1920" height="986" alt="image" src="https://github.com/user-attachments/assets/55f23190-ac96-4712-9d33-7db17e2398ab" /> <br>

------------------------------------------------------------------------------------------------------------------------------------

Q7. Understanding which group Security Identifier (SID) the malicious script checks to verify the current user's privileges can provide insights into the attacker's intentions. Can you provide the specific Group SID that is being checked? <br>

A. In the PCAP file, Navigate to File Header -> Export Objects -> HTTP -> open checking.ps1 or Follow HTTP Stream - ( S-1-5-32-544 )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1226" height="364" alt="image" src="https://github.com/user-attachments/assets/4cc06846-37c6-45ed-aff1-f900a7ac6cd5" /> <br>

------------------------------------------------------------------------------------------------------------------------------------

Q8. Windows Defender plays a critical role in defending against cyber threats. If an attacker disables it, the system becomes more vulnerable to further attacks. What are the registry keys used by the attacker to disable Windows Defender functionalities? Provide them in the same order found. <br>

A. In the same file search for registry keys related to defender - ( DisableAntiSpyware,DisableRoutinelyTakingAction,DisableRealtimeMonitoring,SubmitSamplesConsent,SpynetReporting )

----------------------------------------------------------------------------------------------------------------------------------
<img width="630" height="141" alt="image" src="https://github.com/user-attachments/assets/474a61f4-ee98-4b6a-b3e2-55ad65efd145" /> <br>

----------------------------------------------------------------------------------------------------------------------------------

Q9. Can you determine the URL of the second file downloaded by the attacker? <br>

A. search for HTTP requests with GET method and search for next powershell script after checking.ps1, in packet details pane navigate to Full request UrI - ( http://87.96.21.84/del.ps1 )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1920" height="990" alt="image" src="https://github.com/user-attachments/assets/8b809100-436b-4a9f-bcd3-8ac8e4d9d75b" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q10. Identifying malicious tasks and understanding how they were used for persistence helps in fortifying defenses against future attacks. What's the full name of the task created by the attacker to maintain persistence? <br>

A. Ransomware processes usually maintain persistence by disabling defense and create scheduled tasks for lateral movement. check for schtasks that are created. - ( \Microsoft\Windows\MUI\LPupdate )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1244" height="117" alt="image" src="https://github.com/user-attachments/assets/6d611487-8ac5-4091-b73c-64e89d9170f2" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q11. Based on your analysis of the second malicious file, What is the MITRE ID of the main tactic the second file tries to accomplish? <br>

A. Upon examining del.ps1, I see that it is stopping processes which helps us identify malicious/unusual process running on the system - ( TA005 )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1364" height="270" alt="image" src="https://github.com/user-attachments/assets/a80cb7f6-2990-4334-9069-1b1a7620a50b" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q12. What's the invoked PowerShell script used by the attacker for dumping credentials? <br>

A. check for "dump" in the exported objects - ( Invoke-PowerDump.ps1 )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1577" height="195" alt="image" src="https://github.com/user-attachments/assets/1bc5c0c6-12a3-4921-8b24-2fdb00a56942" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q13. Understanding which credentials have been compromised is essential for assessing the extent of the data breach. What's the name of the saved text file containing the dumped credentials? <br>

A. Follow the HTTP stream - ( hashes.txt )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1273" height="647" alt="image" src="https://github.com/user-attachments/assets/dc507895-7be0-4c77-ab8a-a9d305df14e5" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q14. Knowing the hosts targeted during the attacker's reconnaissance phase, the security team can prioritize their remediation efforts on these specific hosts. What's the name of the text file containing the discovered hosts? <br>

A. Follow HTTP stream - ( extracted_hosts.txt )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1920" height="996" alt="image" src="https://github.com/user-attachments/assets/806b3733-d3d0-4697-aa27-5a7e046fe31d" /> <br>

------------------------------------------------------------------------------------------------------------------------------------

Q15. After hash dumping, the attacker attempted to deploy ransomware on the compromised host, spreading it to the rest of the network through previous lateral movement activities using SMB. You’re provided with the ransomware sample for further analysis. By performing behavioral analysis, what’s the name of the ransom note file? <br>

A. After Executing the .exe file ( make sure Defender allow this and do this in a contained environment ) the files will be renamed - ( # DECRYPT FILES BLUESKY # )

---------------------------------------------------------------------------------------------------------------------------------------
<img width="630" height="69" alt="q15-bluesky" src="https://github.com/user-attachments/assets/2aef7b0a-8346-4251-ac52-b04892a8e030" /> <br>

---------------------------------------------------------------------------------------------------------------------------------------

Q16. In some cases, decryption tools are available for specific ransomware families. Identifying the family name can lead to a potential decryption solution. What's the name of this ransomware family? <br>

A. check the File name - ( Bluesky )

-----------------------------------------------------------------------------------------------------------------------------------------
<img width="1185" height="416" alt="q16-bluesky" src="https://github.com/user-attachments/assets/bd44143b-6f79-4492-b789-49548bf85723" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------------
