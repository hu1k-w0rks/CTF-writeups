**Tools Used: Virus Total, Threat Fox, Malware Bazaar** <br><br>

Q1. Categorizing malware enables a quicker and clearer understanding of its unique behaviors and attack vectors. What category has Microsoft identified for that malware in VirusTotal? <br>

A. In the Detection tab check for Threat categories name - ( Trojan )

----------------------------------------------------------------------------------------------------------------------------------
<img width="1416" height="40" alt="image" src="https://github.com/user-attachments/assets/83916b77-4e1f-4fba-9870-ca7d0626c422" /> <br>

----------------------------------------------------------------------------------------------------------------------------------

Q2. Clearly identifying the name of the malware file improves communication among the SOC team. What is the file name associated with this malware? <br>

A. In the Details tab navigate to Names section - ( Wextract )

----------------------------------------------------------------------------------------------------------------------------------
<img width="502" height="298" alt="image" src="https://github.com/user-attachments/assets/7ac7e3f2-808b-4d82-8bbb-d47c9b68f140" /> <br>

----------------------------------------------------------------------------------------------------------------------------------

Q3. Knowing the exact timestamp of when the malware was first observed can help prioritize response actions. Newly detected malware may require urgent containment and eradication compared to older, well-documented threats. What is the UTC timestamp of the malware's first submission to VirusTotal? <br>

A. In the Details tab navigate to History -> First Submission - ( 2023-10-06 04:41 )

----------------------------------------------------------------------------------------------------------------------------------
<img width="520" height="159" alt="image" src="https://github.com/user-attachments/assets/04733f98-8f8c-48e1-84fa-cf5c9e38fa54" /> <br>

----------------------------------------------------------------------------------------------------------------------------------

Q4. Understanding the techniques used by malware helps in strategic security planning. What is the MITRE ATT&CK technique ID for the malware's data collection from the system before exfiltration? <br>

A. In the Behavior tab, navigate to MITRE ATT&CK Tactics and Techniques, search for collection - ( T1005 )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1652" height="424" alt="image" src="https://github.com/user-attachments/assets/89069cb1-48ac-44d8-bf4d-f5bcc847867d" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q5. Following execution, which social media-related domain names did the malware resolve via DNS queries? <br>

A. In the Relations tab, Navigate to contacted domains and search for different social media websites. Only facebook is found - ( facebook.com )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="681" height="743" alt="image" src="https://github.com/user-attachments/assets/d9a10392-515c-4ade-b51b-d45113405266" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q6. Once the malicious IP addresses are identified, network security devices such as firewalls can be configured to block traffic to and from these addresses. Can you provide the IP address and destination port the malware communicates with? <br>

A. In the Behavior tab under network communication section navigate to IP traffic. - ( 77.91.124.55:19071 )

----------------------------------------------------------------------------------------------------------------------------------
<img width="331" height="259" alt="image" src="https://github.com/user-attachments/assets/cd10ba0a-3863-493f-a589-c494f9d43ebc" /> <br>

----------------------------------------------------------------------------------------------------------------------------------

Q7. YARA rules are designed to identify specific malware patterns and behaviors. Using MalwareBazaar, what's the name of the YARA rule created by "Varp0s" that detects the identified malware? <br>

A. After uploading the hash in malwarebazaar, Navigate to YARA tab and search for author named Varp0s - ( detect_Redline_Stealer )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1234" height="208" alt="image" src="https://github.com/user-attachments/assets/519dbf42-20d3-4f63-934c-ad6df3a2d30e" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q8. Understanding which malware families are targeting the organization helps in strategic security planning for the future and prioritizing resources based on the threat. Can you provide the different malware alias associated with the malicious IP address according to ThreatFox? <br>

A. Navigate to Threatfox and search for ioc:77.91.124.55 and navigate to malware alias - ( RECORDSTEALER )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1253" height="464" alt="image" src="https://github.com/user-attachments/assets/17bee629-7a11-41b2-8826-6e0a16039ff6" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q9. By identifying the malware's imported DLLs, we can configure security tools to monitor for the loading or unusual usage of these specific DLLs. Can you provide the DLL utilized by the malware for privilege escalation? <br>

A. In the Details tab of VirusTotal, under Portable Executable Info Section, navigate to Imports pane - ( ADVAPI32.dll )

----------------------------------------------------------------------------------------------------------------------------------
<img width="163" height="285" alt="image" src="https://github.com/user-attachments/assets/fccd471c-06b2-4b98-8781-b25e48f620d9" /> <br>

----------------------------------------------------------------------------------------------------------------------------------

