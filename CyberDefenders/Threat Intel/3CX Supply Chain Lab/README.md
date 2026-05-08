**Tools Used: Virus Total** <br><br>

Q1. Understanding the scope of the attack and identifying which versions exhibit malicious behavior is crucial for making informed decisions if these compromised versions are present in the organization. How many versions of 3CX running on Windows have been flagged as malware? <br>

A. check "How many versions of 3CX are running on windows" in a any of the search engine - ( 2 )

------------------------------------------------------------------------------------------------------------------------------------------------
<img width="685" height="267" alt="q1-supplychain" src="https://github.com/user-attachments/assets/0d3573d7-0d00-49ed-8d35-88260712edb1" /> <br>

------------------------------------------------------------------------------------------------------------------------------------------------

Q2. Determining the age of the malware can help assess the extent of the compromise and track the evolution of malware families and variants. What's the UTC creation time of the .msi malware? <br>

A. Get the hash of the .msi file and analyze it in Virus Total and in Details Tab navigate to History section - ( 2023-03-13 06:33 )

------------------------------------------------------------------------------------------------------------------------------------------------
<img width="565" height="183" alt="q2-supplychain" src="https://github.com/user-attachments/assets/64141456-3ea1-401b-b756-9bd14f86ffe6" /> <br>

------------------------------------------------------------------------------------------------------------------------------------------------

Q3. Executable files (.exe) are frequently used as primary or secondary malware payloads, while dynamic link libraries (.dll) often load malicious code or enhance malware functionality. Analyzing files deposited by the Microsoft Software Installer (.msi) is crucial for identifying malicious files and investigating their full potential. Which malicious DLLs were dropped by the .msi file? <br>

A. In the Relations tab, navigate to bundled files - ( ffmpeg.dll,d3dcompiler_47.dll )

---------------------------------------------------------------------------------------------------------------------------------------
<img width="879" height="128" alt="image" src="https://github.com/user-attachments/assets/e9a51b04-f036-4866-ae97-181e37731d2f" /> <br>

----------------------------------------------------------------------------------------------------------------------------------------

Q4. Recognizing the persistence techniques used in this incident is essential for current mitigation strategies and future defense improvements. What is the MITRE Technique ID employed by the .msi files to load the malicious DLL? <br>

A. In the Behavior tab, Navigate to MITRE ATT&CK Tactics and Techniques and check for techniques related to DLL. - ( T1574 )

------------------------------------------------------------------------------------------------------------------------------------------------
<img width="278" height="406" alt="q4-supplychain" src="https://github.com/user-attachments/assets/c0e17c53-6a65-4467-8bc0-538daf03ae8a" /> <br>

-------------------------------------------------------------------------------------------------------------------------------------------------

Q5. Recognizing the malware type (threat category) is essential to your investigation, as it can offer valuable insight into the possible malicious actions you'll be examining. What is the threat category of the two malicious DLLs? <br>

A. Get the file hashes of the DLL's from Files Dropped sections of the Behavior tab and navigate to Detection tab and search for threat categories - ( Trojan )

-------------------------------------------------------------------------------------------------------------------------------------------------
<img width="1866" height="403" alt="q5-supplychain" src="https://github.com/user-attachments/assets/31922792-2134-4eac-8375-a3e24582c08c" /> <br>

-------------------------------------------------------------------------------------------------------------------------------------------------

Q6. As a threat intelligence analyst conducting dynamic analysis, it's vital to understand how malware can evade detection in virtualized environments or analysis systems. This knowledge will help you effectively mitigate or address these evasive tactics. What is the MITRE ID for the virtualization/sandbox evasion techniques used by the two malicious DLLs? <br>

A. In the Behavior tab, Navigate to MITRE ATT&CK Tactics and Techniques and check for techniques related to sandbox evasion - ( T1497 )

------------------------------------------------------------------------------------------------------------------------------------------------
<img width="320" height="392" alt="q6-supplychain" src="https://github.com/user-attachments/assets/99090661-ec7f-4352-ac61-c2daae9b6925" /> <br>

------------------------------------------------------------------------------------------------------------------------------------------------

Q7. When conducting malware analysis and reverse engineering, understanding anti-analysis techniques is vital to avoid wasting time. Which hypervisor is targeted by the anti-analysis techniques in the ffmpeg.dll file? <br>

A. In the Virustotal Analysis of ffmpeg.dll, Navigate to behavior tab -> capabilities -> Anti-Analysis - ( VMware )

------------------------------------------------------------------------------------------------------------------------------------------------
<img width="319" height="260" alt="q7-supplychain" src="https://github.com/user-attachments/assets/086d2d78-0a70-4438-a756-0d21dbed4544" /> <br>

------------------------------------------------------------------------------------------------------------------------------------------------

Q8. Identifying the cryptographic method used in malware is crucial for understanding the techniques employed to bypass defense mechanisms and execute its functions fully. What encryption algorithm is used by the ffmpeg.dll file? <br>

A. In the Virustotal Analysis of ffmpeg.dll, Navigate to behavior tab -> capabilities -> Data-Manipulation ( RC4 )

------------------------------------------------------------------------------------------------------------------------------------------------
<img width="304" height="379" alt="q8-supplychain" src="https://github.com/user-attachments/assets/d46119c3-4782-4ed3-b724-166d28056541" /> <br>

------------------------------------------------------------------------------------------------------------------------------------------------

Q9. As an analyst, you've recognized some TTPs involved in the incident, but identifying the APT group responsible will help you search for their usual TTPs and uncover other potential malicious activities. Which group is responsible for this attack? <br>

A. In the Community tab of the Analysis for the .msi file there is mentioned "Wanna Cry Kill Switch" any guess which APT this is linked to ? or Search through the web - ( Lazarus )
