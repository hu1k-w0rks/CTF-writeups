**Tools Used: Volatility workbench, strings** <br><br>

Q1. What is the name of the suspicious process? <br>

A. Use the command windows.pslist.PsList and check the processes with Wow64 value set to True - ( oneetx.exe )

----------------------------------------------------------------------------------------------------------------------------------------
<img width="1121" height="714" alt="q1-redline" src="https://github.com/user-attachments/assets/5e58d039-5895-40b8-b76b-e82c9241a8b1" /> <br>

----------------------------------------------------------------------------------------------------------------------------------------

Q2. What is the child process name of the suspicious process? <br>

A. In the same process check the process with PPID of 5896 - ( rundll32.exe )

---------------------------------------------------------------------------------------------------------------------------------------
<img width="1091" height="42" alt="q2-redline" src="https://github.com/user-attachments/assets/f79eda44-1c4b-4a27-8a52-60dc6ce76e51" /> <br>

---------------------------------------------------------------------------------------------------------------------------------------

Q3. What is the memory protection applied to the suspicious process memory region? <br>

A. use the command windows.malfind.MalFind with PID of 5896 - ( PAGE_EXECUTE_READWRITE )

----------------------------------------------------------------------------------------------------------------------------------------
<img width="1124" height="723" alt="q3-redline" src="https://github.com/user-attachments/assets/deab27e9-4e16-4be3-920a-70e2346e31ee" /> <br>

----------------------------------------------------------------------------------------------------------------------------------------

Q4. What is the name of the process responsible for the VPN connection? <br>

A. when running the command windows.netscan.NetScan i thought tun2socks.exe but then checked the parent process of tun2socks.exe in pslist - ( Outline.exe )

----------------------------------------------------------------------------------------------------------------------------------------
<img width="1098" height="74" alt="q4-redline" src="https://github.com/user-attachments/assets/ff8ee016-607c-4cb4-8086-627a596526a2" /> <br>

----------------------------------------------------------------------------------------------------------------------------------------

Q5. What is the attacker's IP address? <br>

A.For searching the attacker IP address, we should see the IP address of the suspicious process with the command windows.netscan.NetScan - ( 77.91.124.20 )

----------------------------------------------------------------------------------------------------------------------------------------
<img width="1125" height="723" alt="q5-redline" src="https://github.com/user-attachments/assets/4b48815a-2d5b-45df-920f-ca43db9f1935" /> <br>

----------------------------------------------------------------------------------------------------------------------------------------

Q6. What is the full URL of the PHP file that the attacker visited? <br>

A. search with strings of the memory dump file with the attacker's IP - ( http://77.91.124.20/store/games/index.php )

-----------------------------------------------------------------------------------------------------------------------------------
<img width="1101" height="272" alt="image" src="https://github.com/user-attachments/assets/2b178129-05b4-415b-9110-8b18d085fd07" /> <br>

-----------------------------------------------------------------------------------------------------------------------------------

Q7. What is the full path of the malicious executable? <br>

A. check the pstree of the PID 5896 - ( C:\Users\Tammam\AppData\Local\Temp\c3912af058\oneetx.exe )

----------------------------------------------------------------------------------------------------------------------------------------
<img width="1098" height="427" alt="q7-redline" src="https://github.com/user-attachments/assets/423884d5-c11c-40c6-a218-8afd06ea93bb" /> <br>

----------------------------------------------------------------------------------------------------------------------------------------
