Q1. In KB, what is the size of the malicious file? <br>

A. Upload the hash in ViruTotal and Navigate to Details tab -> File Size ( 921.36 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1609" height="423" alt="image" src="https://github.com/user-attachments/assets/2d1aabd4-1cf9-4e8d-a077-703dc8ad8daf" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q2. What word do the threat actors use in log messages to describe their victims, based on the name of an ancient hunted creature? <br>
 
A. Couldn't find this in Virustotal, Hybrid Analysis, Malware bazaar. So used the hints and found the answer inside summary section in Securelist.com by Kaspersky - ( mammoth )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="700" height="142" alt="image" src="https://github.com/user-attachments/assets/7e75ac47-6321-4eca-93f8-850e4908e592" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q3. The threat actor set up a malicious website to mimic a platform designed for creating and managing decentralized autonomous organizations (DAOs) on the MultiversX blockchain (peerme.io). What is the name of the malicious website the attacker created to simulate this platform? <br>

A. Check for the first sub-campaign in the securelist.com - ( tidyme.io )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="679" height="169" alt="image" src="https://github.com/user-attachments/assets/d6bc073d-102a-413f-9b67-ce0c99432f40" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q4. Which cloud storage service did the campaign operators use to host malware samples for both macOS and Windows OS versions? <br>

A. We can find this under the image of Malicious webserver routine to download the appropriate malware version depending on the user’s operating system - ( Dropbox )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="679" height="62" alt="image" src="https://github.com/user-attachments/assets/93b98aaa-c04a-4f9b-bd85-7dde9a83704f" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q5. The malicious executable contains a configuration file that includes base64-encoded URLs and a password used for archived data decompression, enabling the download of second-stage payloads. What is the password for decompression found in this configuration file? <br>

A. The password can be found in the image in the Downloader routine section - ( newfile2024 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="679" height="104" alt="image" src="https://github.com/user-attachments/assets/687a7d46-5314-4a20-b3f3-f16a7b6ccc15" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q6. What is the name of the function responsible for retrieving the field archive from the configuration file? <br>

A. Under the table of Decoded URLs we can find the name of the function - ( downloadAndExtractArchive )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="679" height="104" alt="image" src="https://github.com/user-attachments/assets/4c4d3ad4-a8fa-47c0-900a-79a60a18d0f0" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q7. In the third sub-campaign carried out by the operators, the attacker mimicked an AI translator project. What is the name of the legitimate translator, and what is the name of the malicious translator created by the attackers? <br>

A. We can find this right under the Third Sub-Campaign - ( yous.ai, voico.io )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="689" height="122" alt="image" src="https://github.com/user-attachments/assets/4f9877b1-8348-4db2-a391-a9f0455215e3" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q8. The downloader is tasked with delivering additional malware samples to the victim’s machine, primarily infostealers like StealC and Danabot. What are the IP addresses of the StealC C2 servers used in the campaign? <br>

A. Navigate to the Network IoCs Section and check for IP Address with details mentioned as StealC C2 Server - ( 46.8.238.240,23.94.225.177 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="535" height="237" alt="image" src="https://github.com/user-attachments/assets/01b78426-6a18-4c7b-b718-3495fee5ec82" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q9. What is the address of the Ethereum cryptocurrency wallet used in this campaign? <br>

A. Navigate to the Crypto currency wallet address section find wallet address of ETH - ( 0xaf0362e215Ff4e004F30e785e822F7E20b99723A )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="484" height="237" alt="image" src="https://github.com/user-attachments/assets/964337cf-1fb0-43e0-a339-abc616e1a2e0" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------
