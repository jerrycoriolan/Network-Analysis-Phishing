# Network Analysis (Malware)
![wireshark](https://github.com/jerrycoriolan/Network-Analysis-Phishing/assets/168882662/d7d6ce17-cdca-482f-a3c7-092ab1bfa457)
![zui-social-image](https://github.com/jerrycoriolan/Network-Analysis-Phishing/assets/168882662/f5008e22-da07-4a1d-9e03-58f892c89ff5)


## Introduction

In this project, I investigate packet captures for analysis of connections to a known malicious domain. 

- Wireshark
- TCPDump
- Tshark
- Zui


## Checking to ensure that the PCAP is within the correct timeframe.
<img width="1147" alt="Screenshot 2024-05-25 at 11 52 52 PM" src="https://github.com/jerrycoriolan/Network-Analysis-Phishing/assets/168882662/51f2d039-e370-4aa7-aef4-25f015a72067">


## Checking to see what protocols that exist within the PCAP
<img width="1147" alt="Screenshot 2024-05-25 at 11 53 27 PM" src="https://github.com/jerrycoriolan/Network-Analysis-Phishing/assets/168882662/3231c861-2ebc-49aa-aeed-65d8b343f0de">


## Checking the conversations for any communications to investigate
<img width="1147" alt="Screenshot 2024-05-25 at 11 54 26 PM" src="https://github.com/jerrycoriolan/Network-Analysis-Phishing/assets/168882662/06900dc5-6d45-4a79-a46e-3ab3e350b340">



## Investigate the HTTP stream to investigate the files that are being sent
<img width="1147" alt="Screenshot 2024-05-25 at 11 55 50 PM" src="https://github.com/jerrycoriolan/Network-Analysis-Phishing/assets/168882662/2d44eb2e-5137-451c-82c1-66c2b55c2d26">


## Analyze the domain and IP address using a tool like Virustotal
<img width="1147" alt="Screenshot 2024-05-25 at 11 57 03 PM" src="https://github.com/jerrycoriolan/Network-Analysis-Phishing/assets/168882662/cc783097-48e3-4382-9acb-f343a961a1b5">
<img width="1147" alt="Screenshot 2024-05-25 at 11 58 12 PM" src="https://github.com/jerrycoriolan/Network-Analysis-Phishing/assets/168882662/ae2fb3d2-46d3-45a9-911d-de97aa694eaf">



## Investigate the first HTTP GET request, follow the HTTP stream, and view the request. We see a file towards spet10.spr and the file response shows an MZ header with a 'This program cannot be run in DOS mode' commonly known as a portable executable.
![Screenshot 2024-05-29 at 11 19 30 PM](https://github.com/jerrycoriolan/Network-Analysis-Phishing/assets/168882662/4f20ead9-fef0-4432-8a28-b7bc713445b1)
<img width="1147" alt="Screenshot 2024-05-25 at 11 59 10 PM" src="https://github.com/jerrycoriolan/Network-Analysis-Phishing/assets/168882662/ff33bf97-1bcc-45a4-b471-d53e15dc4682">


## Can also utilize the tool Zui, which will explore and query packets 
![Screenshot 2024-05-26 at 12 16 25 AM](https://github.com/jerrycoriolan/Network-Analysis-Phishing/assets/168882662/bc4a7bd4-4554-4795-83bd-10a681ce623a)
<img width="960" alt="Screenshot 2024-05-29 at 11 46 54 PM" src="https://github.com/jerrycoriolan/Network-Analysis-Phishing/assets/168882662/5f487427-6c9e-40a4-8d66-6cf2272a37ee">



## Conclusion

After investigating the packet captures using Wireshark and Zui in this project, we can conclude that this user is likely infected with the Dridex malware. The Zui tool was able to view 'Alerts' generated within Zui to investigate, which is why it is always good to have an IDS readily available to look at any PCAP that it is fed. 
