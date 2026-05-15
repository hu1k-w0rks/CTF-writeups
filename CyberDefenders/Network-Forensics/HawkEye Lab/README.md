**Tools Used: Wireshark, tshark, linux command line - ( head, tail, grep, sed, nl, wc, awk, sort, cut, md5sum, xxd )** <br><br><br>

Q1. How many packets does the capture have? <br>

A. check the last packet number or count - ( 4003 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1042" height="85" alt="image" src="https://github.com/user-attachments/assets/e9f95388-ac21-496a-9341-bdd57d0c683e" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q2. At what time was the first packet captured (UTC)? <br>

A. Check the UTC time of the first packet - ( 2019-04-10 20:37 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1042" height="85" alt="image" src="https://github.com/user-attachments/assets/5794e38a-6739-4106-8e56-7136727b5569" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q3. What is the duration of the capture? <br>

A. Calculate the time difference between the first and last packet - ( 01:03:41 ) 

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1042" height="183" alt="image" src="https://github.com/user-attachments/assets/5ba23f73-e857-43ce-9476-1440c0c43f59" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q4. What is the most active computer at the link level? <br>

A. If using wireshark, Navigate to Statistics -> Endpoints -> Ethernet ( 00:08:02:1c:47:ae )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1244" height="290" alt="image" src="https://github.com/user-attachments/assets/423f3070-7358-4686-9f6d-29d04fae4257" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q5. Manufacturer of the NIC of the most active system at the link level? <br>

A. Using Wireshark, Navigate to Statistics -> Resolved addresses ( Hewlett-Packard )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="435" height="187" alt="image" src="https://github.com/user-attachments/assets/c0bf50c7-1ba6-448f-8004-0025ebdbd89d" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q6. Where is the headquarter of the company that manufactured the NIC of the most active computer at the link level? <br>

A. Use the Search Engine of your choice and search for Hewlett-packard headquarters - ( Palo Alto )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="439" height="204" alt="image" src="https://github.com/user-attachments/assets/88c3df7a-d0ea-4282-b242-361b633ddfcc" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q7. The organization works with private addressing and netmask /24. How many computers in the organization are involved in the capture? <br>

A. In Wireshark, Navigate to endpoints -> IPv4 [ ignore the ipv4 addresses that ends with 0 or 255 as 0 is used for Gateway and 255 is used for broadcast] - ( 3 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1032" height="382" alt="image" src="https://github.com/user-attachments/assets/52498e2d-0041-41ed-85f0-ed7865197fe6" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q8. What is the name of the most active computer at the network level? <br>

A. DHCP protcol helps us in getting the hostname so use the search filter of dhcp and ip addr = 10.4.10.132 - ( Beijing-5cd1-PC )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1169" height="94" alt="image" src="https://github.com/user-attachments/assets/7eb3f0b2-a1a0-471a-965f-e48680b39ca4" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q9. What is the IP of the organization's DNS server? <br>

A. As Responses for DNS queries are will be given by DNS server check the destination ip for the DNS query packets - ( 10.4.10.4 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1897" height="123" alt="image" src="https://github.com/user-attachments/assets/608b1021-a049-4326-8814-43d72fe8f3d8" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q10. What domain is the victim asking about in packet 204? <br>

A. Search the info for the packet no. 204 - ( proforma-invoices.com )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1726" height="96" alt="image" src="https://github.com/user-attachments/assets/f5de77a3-b863-4f37-9e3f-e8a8633e6006" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q11. What is the IP of the domain in the previous question? <br>

A. Check for the dns response packet associated with the previous mentioned domain - ( 217.182.138.150 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1886" height="119" alt="image" src="https://github.com/user-attachments/assets/5d59b9bc-b678-493a-9ff5-9c4378bc489e" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q12. Indicate the country to which the IP in the previous section belongs. <br>

A. Do an IP lookup - ( France )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1037" height="357" alt="image" src="https://github.com/user-attachments/assets/612aa6d7-8e0a-4916-9d79-6dfdf1c458fd" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q13. What operating system does the victim's computer run? <br>

A. The user-agent often reveals the details in the http response - ( Windows NT 6.1 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1895" height="120" alt="image" src="https://github.com/user-attachments/assets/a353bca6-3f69-42dc-b72e-609915d2e2db" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q14. What is the name of the malicious file downloaded by the accountant? <br>

A. Check the http GET request - ( tkraw_Protected99.exe )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1755" height="92" alt="image" src="https://github.com/user-attachments/assets/79c6e876-c6fc-4de9-a28d-ba38585364a7" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q15. What is the md5 hash of the downloaded file? <br>

A. Retreive the http file using the Export objects and then use md5sum to generate the md5 hash for it - ( 71826ba081e303866ce2a2534491a2f7 ) 

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1039" height="92" alt="image" src="https://github.com/user-attachments/assets/a12c435a-3a05-406c-9bb0-ae3f56bcfb37" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q16. What software runs the webserver that hosts the malware? <br>

A. In Wireshark, follow TCP stream from the packet number of previous question - ( LiteSpeed )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1223" height="92" alt="image" src="https://github.com/user-attachments/assets/3cddaa18-dae0-4d1f-bfe4-d30a7f36e73b" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q17.What is the public IP of the victim's computer?  <br>

A. In wireshark, follow the http stream as the user tried checking his public ip address - ( 173.66.146.112 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1223" height="92" alt="image" src="https://github.com/user-attachments/assets/ffee1f7d-d7ad-4657-ba45-83668008c7a7" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q18. In which country is the email server to which the stolen information is sent? <br>

A. Do IP lookup for the obtained ip address - ( United States )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1038" height="357" alt="image" src="https://github.com/user-attachments/assets/22fddcff-fb20-42a2-af39-bb4161688664" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q19. Analyzing the first extraction of information. What software runs the email server to which the stolen data is sent? <br>

A. As it is an email server check the SMTP response parameters - ( Exim 4.91 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1898" height="110" alt="image" src="https://github.com/user-attachments/assets/81c6fc47-f639-4d56-9ba2-a3a1d1a4c879" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q20. To which email account is the stolen information sent? <br>

A. As the information is being sent the source ip would be the most active computer's ip and search for the receiver's email address - ( sales.del@macwinlogistics.in )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1744" height="234" alt="image" src="https://github.com/user-attachments/assets/12b7b477-c036-46f3-8263-d5e844ca5dd2" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q21. What is the password used by the malware to send the email? <br>

A. Search for the keyword 'pass' in the smtp packets and decode the value - ( Sales@23 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1509" height="333" alt="image" src="https://github.com/user-attachments/assets/074cf699-170e-47fb-9c94-5312757d67c9" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q22. Which malware variant exfiltrated the data? <br>

A. In the SMTP traffic filter out packets with source ip 10.4.10.132 and then follow tcp stream - ( Reborn v9 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1595" height="143" alt="image" src="https://github.com/user-attachments/assets/9a86f301-5bec-402b-8c4c-48660b35b305" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q23. What are the bankofamerica access credentials? (username:password) <br>

A. In the IMF traffic, in the line-based text data check under url == bankofamerica

------------------------------------------------------------------------------------------------------------------------------------------
<img width="504" height="203" alt="image" src="https://github.com/user-attachments/assets/b22c9a4e-7d6b-42b7-b652-f2387960a724" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------

Q24. Every how many minutes does the collected data get exfiltrated? <br>

A. check the interval gap between the IMF data packets [ there is an approximate gap of 600 seconds which is equal to 10 minutes] - ( 10 )

------------------------------------------------------------------------------------------------------------------------------------------
<img width="1033" height="233" alt="image" src="https://github.com/user-attachments/assets/e16aa123-d8f4-45db-ba78-908ecb34cd9c" /> <br>
------------------------------------------------------------------------------------------------------------------------------------------
