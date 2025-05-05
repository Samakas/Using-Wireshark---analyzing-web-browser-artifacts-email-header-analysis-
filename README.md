# Using-Wireshark---analyzing-web-browser-artifacts-email-header-analysis
## AIM:
To use Wireshark to analyze web browser activities and inspect email headers from captured network traffic.

## DESIGN STEPS:
### Step 1:
Launch Wireshark and start capturing traffic on the appropriate network interface.

### Step 2:
Use filters like http, dns, or tcp.port == 80 to monitor web browser artifacts such as visited URLs, cookies, and user-agent strings.

### Step 3:
Apply filters like smtp, pop, or imap to locate and analyze email header details (e.g., sender, receiver, subject) from email communications.

## PROGRAM:
Wireshark Web and Email Traffic Filtering Steps

## OUTPUT:
Captured Web Activity and Email Header Information
A. Capturing Traffic in Wireshark

Open Wireshark and start capturing on the active interface (Wi- Fi/Ethernet).

Perform activities like opening a website or sending an email through a client (e.g., Gmail via browser or Thunderbird).

Stop the capture once done.

![image](https://github.com/user-attachments/assets/b1c5d654-16f6-40c2-9b25-9dfd25995f8d)

Analyze DNS Queries: o Filter: dns

o Reveal domains the browser tried to resolve.

![image](https://github.com/user-attachments/assets/80b9512f-87db-4a7e-b60f-7e526c111646)

Email Header Analysis

Apply relevant filters:
o For POP3: tcp.port == 110

o For SMTP: tcp.port == 25 or 587

o For IMAP: tcp.port == 143 or 993

Locate email data:
o Look for SMTP packets to see sender/receiver email addresses.

o Use "Follow TCP Stream" to view the full email headers and body if unencrypted.

Extract Email Header Fields:

o Analyze From, To, Subject, Date, Message-ID, and relay servers used in sending the email.

![image](https://github.com/user-attachments/assets/69aa1843-d7c6-4d56-bc8f-d08e5a35e625)

![image](https://github.com/user-attachments/assets/7bc59d61-290d-40ac-9976-03fbe5464aa8)

![image](https://github.com/user-attachments/assets/b5734407-c9a8-41f8-b011-13375e32a107)





## RESULT:
Web browser artifacts and email headers were successfully analyzed using Wireshark.

