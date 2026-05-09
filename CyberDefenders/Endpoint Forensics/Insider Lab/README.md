**Tools Used: FTK imager, linux command line** <br><br><br>

**Prequesite**: Open FTK iamger, Navigate to File tab and Select the option of "Decrypt AD1 image" and decrupt the .AD1 file of the lab and choose your desired output location. Now Navigate to the Output Folder location and complete the lab. <br><br>

Q1. Which Linux distribution is being used on this machine? <br>

A. Navigate to Your_Output_Location -> [root] directory -> boot. We can see the Linux distribution and its architecture - ( kali )

-------------------------------------------------------------------------------------------------------------------------------------------
<img width="1472" height="97" alt="q1-insider-lab" src="https://github.com/user-attachments/assets/f7343672-66ae-40c9-acb5-92532b17f18c" /> <br>
-------------------------------------------------------------------------------------------------------------------------------------------

Q2. What is the MD5 hash of the Apache access.log file? <br>

A. In Linux FileSystem, access.log will be located at /var/log/access.log. Used MD5sum to get the hash value - ( d41d8cd98f00b204e9800998ecf8427e )

-------------------------------------------------------------------------------------------------------------------------------------------
<img width="580" height="95" alt="q2-insider-lab" src="https://github.com/user-attachments/assets/41fa464f-01b5-4dfa-b2b8-0ddb91b86c9e" /> <br>
-------------------------------------------------------------------------------------------------------------------------------------------

Q3. It is suspected that a credential dumping tool was downloaded. What is the name of the downloaded file? <br>

A. Check the Downloads Folder in the root Directory - ( mimikatz_trunk.zip )

-------------------------------------------------------------------------------------------------------------------------------------------
<img width="1137" height="78" alt="q3-insider-lab" src="https://github.com/user-attachments/assets/8955599c-bc53-4aa3-a8dc-54eaecf1115a" /> <br>
-------------------------------------------------------------------------------------------------------------------------------------------

Q4. A super-secret file was created. What is the absolute path to this file? <br>

A. In the root directory, check the bash_history file to see files/folders created/modified/deleted/accessed - ( /root/Desktop/SuperSecretFile.txt )

--------------------------------------------------------------------------------------------------------------------------------------------
<img width="1186" height="297" alt="q4-insider-lab" src="https://github.com/user-attachments/assets/9427c9c2-0465-41cc-a74e-ec147e918978" /> <br>
--------------------------------------------------------------------------------------------------------------------------------------------

Q5. What program used the file didyouthinkwedmakeiteasy.jpg during its execution? <br>

A. In the root directory, check the bash_history file to see files/folders created/modified/deleted/accessed - ( binwalk )

--------------------------------------------------------------------------------------------------------------------------------------------
<img width="1179" height="296" alt="q5-insider-lab" src="https://github.com/user-attachments/assets/49deafbe-1d56-4f16-b975-891c55062c11" /> <br>
--------------------------------------------------------------------------------------------------------------------------------------------

Q6. What is the third goal from the checklist Karen created? <br>

A. In the root directory, check everything for "checklist" - ( profit )

--------------------------------------------------------------------------------------------------------------------------------------------
<img width="1191" height="608" alt="q6-insider-lab" src="https://github.com/user-attachments/assets/e3f3157e-ed5a-40c6-a535-df3e44e73ddf" /> <br>
--------------------------------------------------------------------------------------------------------------------------------------------

Q7. How many times was Apache run? <br>

A. The logs for apache are usually stored in /var/log/apache2 folder as the size indicates 0, apache never ran on the Endpoint - ( 0 )

-------------------------------------------------------------------------------------------------------------------------------------------
<img width="828" height="209" alt="q7-insider-lab" src="https://github.com/user-attachments/assets/73c581ce-dc24-4925-a62f-bc831c1b54d8" /> <br>
-------------------------------------------------------------------------------------------------------------------------------------------

Q8. This machine was used to launch an attack on another. Which file contains the evidence for this? <br>

A. There is a individual file in the root directory which caught my attention, when opened it has the evidence for launch of an attack - ( irZLAohL.jpeg )

-------------------------------------------------------------------------------------------------------------------------------------------
<img width="1185" height="88" alt="q8-insider-lab" src="https://github.com/user-attachments/assets/5e50a5a6-0f70-412e-902a-2f4623f1d2d4" /> <br>
-------------------------------------------------------------------------------------------------------------------------------------------

Q9. It is believed that Karen was taunting a fellow computer expert through a bash script within the Documents directory. Who was the expert that Karen was taunting? <br>

A. Check everything karen has created in her Documents Folder and file named firstscript_fixed reveals who she was taunting - ( Young )

-------------------------------------------------------------------------------------------------------------------------------------------
<img width="711" height="243" alt="q9-insider-lab" src="https://github.com/user-attachments/assets/eae0926f-b7fa-4709-b14f-38ff0f933bc1" /> <br>
-------------------------------------------------------------------------------------------------------------------------------------------

Q10. A user executed the su command to gain root access multiple times at 11:26. Who was the user? <br>

A. Login commands executions are stored at /var/log/auth.log in linux, check for user who used "su" command - ( postgres )

---------------------------------------------------------------------------------------------------------------------------------------------
<img width="1040" height="212" alt="q10-insider-lab" src="https://github.com/user-attachments/assets/4280831a-54a6-47e4-a46e-4b1d9f33d927" /> <br>
---------------------------------------------------------------------------------------------------------------------------------------------

Q11. Based on the bash history, what is the current working directory? <br>

A. User has changed his directory to root and also reveals us which file he wants to access and its location in bash history - ( /root/Documents/myfirsthack/ ) 

---------------------------------------------------------------------------------------------------------------------------------------------
<img width="1181" height="309" alt="q11-insider-lab" src="https://github.com/user-attachments/assets/388188f5-3393-4af0-ac89-cd906e089e4f" /> <br>
---------------------------------------------------------------------------------------------------------------------------------------------
