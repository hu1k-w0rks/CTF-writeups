**Tools used: Volatility** <br><br><br>

Q1. What is the name of the process responsible for the suspicious activity? <br>

A. List the processes where Wow64 is True - ( ChromeSetup.exe )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1559" height="146" alt="image" src="https://github.com/user-attachments/assets/1106e34b-e0af-495f-a3af-bdfc4882c67e" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q2. What is the exact path of the executable for the malicious process? <br>

A. Use the CmdLine command and filter out the results containing ChromeSetup process - ( C:\Users\alex\Downloads\ChromeSetup.exe )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1045" height="93" alt="image" src="https://github.com/user-attachments/assets/9c736c43-e263-4a98-bb79-7e7210eb6c17" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q3. Identifying network connections is crucial for understanding the malware's communication strategy. What IP address did the malware attempt to connect to? <br>

A. Use the NetScan command and filter out the results containing ChromeSetup process - ( 58.64.204.181 )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1652" height="155" alt="image" src="https://github.com/user-attachments/assets/bcf88a2c-4344-46d6-bfe0-6392ed9b95c7" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q4. To determine the specific geographical origin of the attack, Which city is associated with the IP address the malware communicated with? <br>

A. We can check the ip origin using ipinfo - ( Hong Kong )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1030" height="339" alt="image" src="https://github.com/user-attachments/assets/4ff6b568-ac65-4490-8eaa-cbcefbe46ebb" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q5. Hashes serve as unique identifiers for files, assisting in the detection of similar threats across different machines. What is the SHA1 hash of the malware executable? <br>

A. To get the SHA1 hash of the malware executable, we first have to dump the file for that search for Chrome Setup in File Scan command and then get the virtual address of it and then find dump files 
using the dumpfiles command and then get the SHA1 hash of the file - ( 280c9d36039f9432433893dee6126d72b9112ad2 )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1661" height="741" alt="image" src="https://github.com/user-attachments/assets/baace5b3-a784-47a4-b06b-0e81180c86db" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q6. Examining the malware's development timeline can provide insights into its deployment. What is the compilation timestamp for the malware? <br>

A. Use the obtained sha1 hash for Threat analysis in the VirusTotal and then Navigate to Details tab -> History section -> creation date - ( 2019-12-01 08:36 )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1751" height="814" alt="image" src="https://github.com/user-attachments/assets/f75dfdc6-2c76-4b47-a7fa-83eae6a833da" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q7. Identifying the domains associated with this malware is crucial for blocking future malicious communications and detecting any ongoing interactions with those domains within our network. Can you provide the domain connected to the malware? <br>

A. Navigate to Relations tab -> Contacted Domains - ( dnsnb8.net )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1718" height="190" alt="image" src="https://github.com/user-attachments/assets/3d2a9994-5cd4-4aa9-9643-ae31fa812d58" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------



