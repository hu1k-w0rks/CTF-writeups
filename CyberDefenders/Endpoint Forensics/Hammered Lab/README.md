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

A.

------------------------------------------------------------------------------------------------------------------------------------------
<br>
------------------------------------------------------------------------------------------------------------------------------------------

Q6. How many requests were sent to the Apache Server? <br>

A. The access log in the apache directory contains the number of requests sent - ( 365 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="983" height="99" alt="image" src="https://github.com/user-attachments/assets/12a6443c-12a2-431b-95f4-b47fc85e03c3" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q7. How many rules have been added to the firewall? <br>

A.

------------------------------------------------------------------------------------------------------------------------------------------
<br>
------------------------------------------------------------------------------------------------------------------------------------------

Q8. One of the downloaded files on the target system is a scanning tool. What is the name of the tool? <br>

A.

------------------------------------------------------------------------------------------------------------------------------------------
<br>
------------------------------------------------------------------------------------------------------------------------------------------

Q9. When was the last login from the attacker with IP 219.150.161.20? Format: MM/DD/YYYY HH:MM:SS <br>

A.

------------------------------------------------------------------------------------------------------------------------------------------
<br>
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

A.

------------------------------------------------------------------------------------------------------------------------------------------
<br>
------------------------------------------------------------------------------------------------------------------------------------------
