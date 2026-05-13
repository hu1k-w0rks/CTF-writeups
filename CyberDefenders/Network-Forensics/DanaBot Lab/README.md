**Tools Used: tshark**

Q1. Which IP address was used by the attacker during the initial access? <br>

A. Check the DNS requests, observe the response of the dns requests which gives us the ip address - ( 62.173.142.148 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1832" height="148" alt="image" src="https://github.com/user-attachments/assets/869e2b4e-7349-4bec-ba26-6358caa90cbf" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q2. What is the name of the malicious file used for initial access? <br>

A. check the response in the http reposne or follow http stream - ( allegato_708.js )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1832" height="148" alt="image" src="https://github.com/user-attachments/assets/d5a169cd-94ef-40da-afba-ad850d6cbbfc" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q3. What is the SHA-256 hash of the malicious file used for initial access? <br>

A. Export the http objects and check the sha256 hash of the first file - ( 847b4ad90b1daba2d9117a8e05776f3f902dda593fb1252289538acf476c4268 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1058" height="89" alt="image" src="https://github.com/user-attachments/assets/73252dfd-ed4e-4ec4-b34e-59628020ea7c" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q4. Which process was used to execute the malicious file? <br>

A. check in the php file - ( wscript )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1198" height="112" alt="image" src="https://github.com/user-attachments/assets/308844ed-9a2e-4ab1-bdfd-9e3a04fa69a3" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q5. What is the file extension of the second malicious file utilized by the attacker? <br>

A. check the exported objects to find it out - ( dll )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1226" height="201" alt="image" src="https://github.com/user-attachments/assets/b0b3d816-f914-49e9-a19d-edb6ee27d722" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q6. What is the MD5 hash of the second malicious file? <br>

A. use md5sum for the dll file - ( e758e07113016aca55d9eda2b0ffeebe )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1071" height="85" alt="image" src="https://github.com/user-attachments/assets/8ce232e8-29ea-481f-80c9-486a2b9b9410" /> <br>
-----------------------------------------------------------------------------------------------------------------------------------------
