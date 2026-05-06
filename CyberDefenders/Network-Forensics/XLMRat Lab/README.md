Tools Used : Wireshark 

Q1. The attacker successfully executed a command to download the first stage of the malware. What is the URL from which the first malware stage was installed?


A. Download lab files -> open the txt file -> Edit it to get the desired output - ( http://45.126.209.4:222/mdm.jpg )


<img width="1331" height="153" alt="image" src="https://github.com/user-attachments/assets/a587d511-3dc4-4233-94d2-59ac1c7519bc" />



Q2. Which hosting provider owns the associated IP address?


A. Do whois lookup for the obtained IP address - ( reliableSite.net )


<img width="844" height="124" alt="image" src="https://github.com/user-attachments/assets/df8882e4-01dd-42bd-9c1b-04a0f9b34857" />



Q3.  By analyzing the malicious scripts, two payloads were identified: a loader and a secondary executable. What is the SHA256 of the malware executable?


A. Open the image file there are 2 hexstrings, decode it and upload the file to Virustotal - ( 1eb7b02e18f67420f42b1d94e74f3b6289d92672a0fb1786c30c03d68e81d798 )


<img width="1308" height="73" alt="image" src="https://github.com/user-attachments/assets/b390f0be-9b3d-4ef4-bf2e-bb44f8929494" />

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<img width="799" height="568" alt="image" src="https://github.com/user-attachments/assets/0b582543-e36e-4c8e-9b03-b92f19380ceb" />



Q4. What is the malware family label based on Alibaba?


A. In the Detection, Navigate to Security vendors' analysis and search for Alibaba - ( asyncrat )


<img width="900" height="142" alt="image" src="https://github.com/user-attachments/assets/3a244632-4b0a-4847-b603-97945ed5486c" />



Q5. What is the timestamp of the malware's creation?


A. Navigate to Details tab -> History Section -> Creation Time - ( 2023-10-30 15:08 )


<img width="1863" height="923" alt="image" src="https://github.com/user-attachments/assets/30859b50-4c02-4a47-bf2f-8f50f14b75a2" />



Q6. Which LOLBin is leveraged for stealthy process execution in this script? Provide the full path.


A. We can find this inside the image file - ( C:\Windows\Microsoft.NET\Framework\v4.0.30319\RegSvcs.exe )


<img width="1622" height="102" alt="image" src="https://github.com/user-attachments/assets/8ad04b0d-e3d8-4fea-8fb5-955bc3f889ae" />



Q7. The script is designed to drop several files. List the names of the files dropped by the script.


A. These can also be found in the image file - ( Conted.vbs,Conted.ps1,Conted.bat )


<img width="848" height="215" alt="image" src="https://github.com/user-attachments/assets/a3e33a89-ae43-4d28-8246-d24a47d036fb" />






