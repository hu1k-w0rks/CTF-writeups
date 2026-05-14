**Tools used: Volatility3** <br><br><br>

Q1. Identifying the name of the malicious process helps in understanding the nature of the attack. What is the name of the malicious process? <br>

A. Use the malfind plugin to check the name of the malicious process - ( powershell.exe )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1373" height="194" alt="image" src="https://github.com/user-attachments/assets/ea70547a-0c49-48ff-b42d-570dc40e6c7e" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q2. Knowing the parent process ID (PPID) of the malicious process aids in tracing the process hierarchy and understanding the attack flow. What is the parent PID of the malicious process? <br>

A. Use the pslist plugin to check the ppid of the powershell - ( 4120 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1583" height="167" alt="image" src="https://github.com/user-attachments/assets/599ec814-ecda-4288-a8be-1281cdb06759" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q3. Determining the file name used by the malware for executing the second-stage payload is crucial for identifying subsequent malicious activities. What is the file name that the malware uses to execute the second-stage payload? <br>

A. Use the windows commandline plugin to check for the what all the malware has executed. - ( 3435.dll )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1850" height="88" alt="image" src="https://github.com/user-attachments/assets/50955e9f-c3b7-494d-88bb-57ea81cecdcb" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q4. Identifying the shared directory on the remote server helps trace the resources targeted by the attacker. What is the name of the shared directory being accessed on the remote server? <br>

A. You can check the previous answer for this too - ( davwwwroot )

----------------------------------------------------------------------------------------------------------------------------------------

Q5. What is the MITRE ATT&CK sub-technique ID that describes the execution of a second-stage payload using a Windows utility to run the malicious file? <br>

A. As we saw in previous image it used rundll32 and it felt suspicious when checked in pslist and dlllist for this process the output returned nothing so searched in web for it - ( T1218.011 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="699" height="319" alt="image" src="https://github.com/user-attachments/assets/3555f335-ef7b-4994-93ee-a28d13ed3743" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q6. Identifying the username under which the malicious process runs helps in assessing the compromised account and its potential impact. What is the username that the malicious process runs under? <br>

A. We can use the getsids plugin to see the Users/Accounts a particular process interacted with - ( Elon )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1195" height="175" alt="image" src="https://github.com/user-attachments/assets/52c3868a-878d-4168-a5b1-ae43c369a86a" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q7. Knowing the name of the malware family is essential for correlating the attack with known threats and developing appropriate defenses. What is the name of the malware family? <br>

A. Use the obtained ip address and search it on Threat Intelligence platforms like VirusTotal - ( STRELASTEALER )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1799" height="451" alt="image" src="https://github.com/user-attachments/assets/9a18d0ca-af0f-4e1f-8458-2fa71af028c4" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------
