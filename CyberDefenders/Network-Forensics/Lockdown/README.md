Tools used: Wireshark, Volatility WorkBench, VirusTotal

**PCAP Analysis - Wireshark**




Q1. After flooding the IIS host with rapid-fire probes, the attacker reveals their origin. Which IP address generated this reconnaissance traffic?

A. Open the PCAP file > Navigate to Statistics > Conversations > IPV4, ( 10.0.2.4 )
<img width="1669" height="524" alt="image" src="https://github.com/user-attachments/assets/764e50bb-610d-4196-9aa3-d8cac11ca9db" />



Q2. Zeroing in on a single open service to gain a foothold, the attacker carries out targeted enumeration. Which MITRE ATT&CK technique ID covers this activity?

A. Key points in question - targeting open service, foothold, Enumeration - ( T1046 )
<img width="1356" height="406" alt="image" src="https://github.com/user-attachments/assets/99afb2be-0fda-4bee-a632-c4ffa9384685" />



Q3. While reviewing the SMB traffic, you observe two consecutive Tree Connect requests that expose the first shares the intruder probes on the IIS host. Which two full UNC paths are accessed?

A. Filter out the SMB2 packtes then search for packet details with string containing "connect request" ( \\10.0.2.15\Documents, \\10.0.2.15\IPC$ )
<img width="1920" height="564" alt="image" src="https://github.com/user-attachments/assets/5095342f-aaf1-4a88-b38e-65a441e03b5a" />



Q4. Inside the share, the attacker plants a web-accessible payload that will grant remote code execution. What is the filename of the malicious file they uploaded, and what byte length is specified in the corresponding SMB2 Write Request?

A. Filter out SMB2 packets then search for packet details with write request - ( shell.aspx, 1015024 )
<img width="1920" height="961" alt="image" src="https://github.com/user-attachments/assets/cd94f8ff-82e0-4b5a-9443-6a06c1c68768" />



Q5. The newly planted shell calls back to the attacker over an uncommon but firewall-friendly port. Which listening port did the attacker use for the reverse shell?

A. First check the packet no. when the shell is planted (3573) and then check when the transmission started from the victim to the attacker - ( 4443 )
<img width="1912" height="606" alt="image" src="https://github.com/user-attachments/assets/d975be68-2cac-4259-abd1-fa9d103640ab" />



**Memory Dump Analysis - Volatility WorkBench**




Q6. Your memory snapshot captures the system’s kernel in situ, providing vital context for the breach. What is the kernel base address in the dump?

A. Run the command windows.info.info and search for the Kernel base value - ( 0xf80079213000 )
<img width="1262" height="894" alt="Screenshot 2026-05-06 160830" src="https://github.com/user-attachments/assets/3a353d59-6b79-4670-8117-a3a0f728a0c5" />



Q7. A trusted service launches an unfamiliar executable residing outside the usual IIS stack, signalling a persistence implant. What is the final full on-disk path of that executable, and which MITRE ATT&CK persistence technique ID corresponds to this behaviour?

A. Check the Parent Process ID ( PPID ) for suspected/unusual process and as it is showing persistence mechanism by using the legitimate process - ( C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Startup\updatenow.exe, T1547 )

<img width="1912" height="606" alt="image" src="https://github.com/user-attachments/assets/61cdcafc-f866-44df-9ecf-f85799e5125f" />

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<img width="1915" height="971" alt="q7" src="https://github.com/user-attachments/assets/c76ab587-ade3-4f2f-b28f-2be30b41b21b" />



Q8. The reverse shell’s outbound traffic is handled by a built-in Windows process that also spawns the implanted executable. What is the name of this process, and what PID does it run under?

A. We already know the unsual process - ( w3wp.exe, 4332 )
<img width="503" height="643" alt="q8" src="https://github.com/user-attachments/assets/5b5dd286-cd6c-46ae-9be5-7bc0f6ed3f24" />



**Malware Sample Analysis - VirusTotal**




Q9. Static inspection reveals the binary has been packed to hinder analysis. Which packer was used to obfuscate it?

A. Upload the .exe file to the virustotal and in the Details section seach for packer - ( UPX )
<img width="1912" height="778" alt="image" src="https://github.com/user-attachments/assets/98e30bf6-3447-49ed-879d-5b3f945d4def" />



Q10. Threat-intel analysis shows the malware beaconing to its command-and-control host. Which fully qualified domain name (FQDN) does it contact?

A. Navigate to Relations and check the contacted domains - ( cp8nl.hyperhost.ua )
<img width="1850" height="713" alt="image" src="https://github.com/user-attachments/assets/13f9be52-2505-44ab-8eea-27cb32a5cb5e" />



Q11. Open-source intel associates that hash with a well-known commodity RAT. To which malware family does the sample belong?

A. Navigate to Community and search for Threat Family - ( Agent Tesla ) 
<img width="1051" height="705" alt="image" src="https://github.com/user-attachments/assets/b965efca-ea0c-4609-bbb2-3046cf3cd379" />










