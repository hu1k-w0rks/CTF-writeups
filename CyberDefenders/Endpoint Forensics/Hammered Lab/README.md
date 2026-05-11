**Tools Used: Linux command line** <br><br><br>

Q1. Which service did the attackers use to gain access to the system? <br>

A. I did a reccursive search for accepted or failed password - ( ssh )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1285" height="311" alt="image" src="https://github.com/user-attachments/assets/a979d6a0-39c6-4541-aad4-aaa8126fae90" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q2. What is the operating system version of the targeted system? <br>

A. Do a reccursive search for linux version - ( 4.2.4-1ubuntu3 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="983" height="110" alt="image" src="https://github.com/user-attachments/assets/479317bc-7c1b-45e9-bbb1-473cbe0bb912" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q3. What is the name of the compromised account? <br>

A. check for the user who executed the most commands - ( root )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="983" height="147" alt="image" src="https://github.com/user-attachments/assets/9fb504b7-41a4-493d-95ad-67f4bee709ee" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q4. How many attackers, represented by unique IP addresses, were able to successfully access the system after initial failed attempts? <br>

A. search for accepted password and then sort out basing on the distinct usernames - ( 6 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="983" height="217" alt="image" src="https://github.com/user-attachments/assets/5e0e91c6-5b1f-41b4-b2eb-6ae2871a4328" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q5. Which attacker's IP address successfully logged into the system the most number of times? <br>

A. check for the accepted passwords for the compromised account and check for the ip address that logged in most of the times - ( 219.150.161.20 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1132" height="507" alt="image" src="https://github.com/user-attachments/assets/f593151a-f675-43ab-b818-69d875c8b2d3" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q6. How many requests were sent to the Apache Server? <br>

A. The access log in the apache directory contains the number of requests sent - ( 365 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="983" height="99" alt="image" src="https://github.com/user-attachments/assets/12a6443c-12a2-431b-95f4-b47fc85e03c3" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q7. How many rules have been added to the firewall? <br>

A. search for the linux firewall system and filter out accepted/allowed commands and find the distinct ports - ( 6 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1526" height="211" alt="image" src="https://github.com/user-attachments/assets/6c38c573-1158-4d73-b118-d6bafdbfa366" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q8. One of the downloaded files on the target system is a scanning tool. What is the name of the tool? <br>

A. The term.log contains the FULL terminal session output, installation messages/errors, search for tool related to scanning - ( nmap )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="988" height="552" alt="image" src="https://github.com/user-attachments/assets/953beb57-d400-45d0-95ba-74fb6aaacc8c" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q9. When was the last login from the attacker with IP 219.150.161.20? Format: MM/DD/YYYY HH:MM:SS <br>

A. Search the last Accepted password event for the ip adrress and check the file modification time of the auth.log file and correlate both - ( 2010-04-19 05:56 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1279" height="192" alt="image" src="https://github.com/user-attachments/assets/7fde3b70-5dd4-4719-853b-9e06090d5f09" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q10. The database showed two warning messages. Please provide the most critical and potentially dangerous one. <br>

A. Grep the warning from the daemon log and check the warning - ( mysql.user contains 2 root accounts without password! )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="991" height="190" alt="image" src="https://github.com/user-attachments/assets/db8f493b-48dd-4929-9db4-9665f9520333" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q11. Multiple accounts were created on the target system. Which account was created on April 26 at 04:43:15? <br>

A. search for useradd in auth.log and filter out the time needed - ( wind3str0y )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1497" height="99" alt="image" src="https://github.com/user-attachments/assets/c224d182-40f1-420b-b57b-25f3fb9da741" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q12. Few attackers were using a proxy to run their scans. What is the corresponding user-agent used by this proxy? <br>

A. User-Agent can be found for web responses sent and the every web response returns a status code, so filter out the status codes from the apache directory and then find the unique user-agent - ( pxyscand/2.1 ) 

------------------------------------------------------------------------------------------------------------------------------------------
<img width="988" height="260" alt="image" src="https://github.com/user-attachments/assets/af90094b-a6fe-4d52-8e3c-6e38b4eef4c0" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------
