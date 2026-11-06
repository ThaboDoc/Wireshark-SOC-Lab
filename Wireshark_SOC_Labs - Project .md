## Overview

This project document a practical SOC investigation using Wireshark to capture and analyze network traffic.
The objective is to identify unusual network behaviour, investigate suspicious connections and detect 
potential malicious activity.

## Investigation Evidence Results

## Wireshark SOC LAB 3
<img src="lab3.PNG" width="350" height="300"  alt="Lab 3">

## Identify the Attackers IP.
I have managed to track and find the IP address of the attacker and the opened/closed Ports that were 
tested by the intruder. I also manage to learn more about the port scan investigation using wireshark.

What I learned is that attackers often scan multiple ports on a target system to identify open
ports and potential vulnerabilities. If the same IP address appears repeatedly while
attempting to communicate through multiple ports, it may indicate suspicious activity or a
possible port-scanning attack. 

## Suggested Solution
The organisation should implement a properly configured firewall to monitor and restrict
unauthorised connection attempts to exposed ports. Unnecessary ports should be closed while
access to essential services should be restricted to authorised IP addresses wherever possible. 

An Intrusion Detection and Prevention System should also be deployed to detect and alert
security teams about repeated connection attempts and potential port-scanning activities. 
Continuous network monitoring and IP address investigation can help SOC analysts identify
potential attackers and respond to suspicious activities before they exploit vulnerabilities.

## Wireshark SOC LAB 4

<img src="lab4.PNG" width="350" height="300" alt="Lab 4">

## Follow TCP Stream Part 1

I learned that conversations and data transmitted over HTTP are not encrypted,
which means sensitive information such as usernames, passwords and private messages 
can potentially be intercepted and exposed by attackers.

This highlights the importance of using HTTPS with TLS encryption to protect data in transit
ensuring that communication between users and web servers remains confidential and secure.

## Wireshark SOC Lab 5

<img src="lab5.PNG" width="350" height="350" alt="Lab 5">

## Follow TCP Stream Part 2

In this lab, I managed to identify hidden information embedded within a file. 
I learned that information can be concealed in HTML files using comments
inside the file. 

The comments as a message are not displayed on the webpage but can still be viewed by
inspecting the HTML source code. 
This demonstrates how hidden information can be discovered through basic file 
and source code analysis.

Information that is hidden from the webpage is not necessarily secure. 
Anything delivered tothe browser should be treated as potentially accessible to the user.

## Suggested Solution

Developers must avoid storing passwords, usernames, confidential messages, API keys or
internal information within HTML comments or client-side code.
Regular source code reviews, security assessments and secure coding practices should be
implemented to identify and remove hidden information before websites are deployed.

## Wireshark SOC LAB 6
<img src="lab6.PNG" width="350" height="350" alt="Lab 6">

## HTTP plain text credentials

HTTPS uses TLS encryption to protect data transmitted between users and web servers, 
ensuring that sensitive information cannot easily be read if network traffic is 
captured using tools such as Wireshark. 

Instead of exposing credentials in plain text, the encrypted traffic appears unreadable to
anyone attempting to intercept it without the appropriate decryption keys. 
This helps maintain data confidentiality and protect users against credential theft 
and unauthorised access.

## Wireshark SOC LAB 7
<img src="lab7.PNG" width="350" height="350" alt="Lab 7">

## Brute Force Catch
During this investigation I used Wireshark's Protocol Hierarchy feature under Statistics 
to identify FTP traffic within the captured network packets. I ascertained multiple failed FTP 
login attempts involving repeated password guesses against the same user account
followed by a successful login. 

This behaviour is consistent with a brute-force attack where an attacker systematically attempts different passwords until the correct credentials are discovered.

Identifying suspicious login behaviour is an important skills for SOC analysts when investigating possible credential compromises.

## Suggested Solution

The organisation should disable standard FTP and replace it with secure alternatives such as
SFTP or FTPS. Account lockout policies such as multi-factor authentication (MFA).
login attempt monitoring should be implemented to reduce the risk of brute-force attacks. An
IDS/IPS solution can help detect repeated authentication failures and alert the SOC team to
suspicious login activity.

## Wireshark SOC LAB 8
<img src="lab8.PNG" width="350" height="350" alt="Lab 8">

## VOIP Call replay

I analysed VoIP network traffic using Wireshark and identified the protocols responsible for
establishing and carrying a phone call. I discovered that Session Initiation Protocol was used
to initiate the call while Real-time Transport Protocol carried the voice data through
multiple small packets transmitted approximately every 60 milliseconds.

By inspecting the SIP INVITE message I have identified extension number 101 as the caller.
Voice conversations can potentially be intercepted and replayed when voice packets are
transmitted without encryption. This creates a confidentiality risk because attackers
monitoring network traffic may be able to capture and listen to private conversations.

## Key findings:

Call setup protocol          : SIP.

Voice transmission protocol  : RTP.

Calling extension            : 101.

Security risk in here is that unencrypted voice packets can potentially be captured and replayed.

## Recommended Solution

The company should implement Secure Real-time Transport Protocol (SRTP) to encrypt voice 
packets and protect conversations from interception. SIP signalling should be protected using
TLS to secure call setup messages. These security measures help maintain the confidentiality
and integrity of VoIP communications and reduce the risk of unauthorised access to private
conversations.

VoIP communication can expose sensitive conversations when encryption is not implemented.
Using SRTP for voice traffic and TLS for SIP signalling is essential for securing business
phone communications and protecting confidential information.

## Overall results and summary
<img src="SOC_Labs.png" width="550" height="450" alt="SOC_Labs">

## <h2><u>This is the summarized report of the results for my LAB Projects</u></h2>

LAB 3 = Identify the Attacker's IP     </> <br>   : <span style="color:orange">90/100 – Outstanding</span>

LAB 4 = Follow TCP Stream Part 1          : <span style="color:orange">90/100 – Outstanding</span>

LAB 5 = Follow TCP Stream Part 2          : <span style="color:green">100/100 – Outstanding</span>

LAB 6 = HTTP Plain Text Credentials       : <span style="color:orange">90/100 – Outstanding</span>

LAB 7 = Brute Force Catch                 : <span style="color:green">100/100 – Outstanding</span>

LAB 8 = VoIP Call Replay                  : <span style="color:orange">90/100 – Outstanding</span>



## AVERAGE SCORE: 93.33/100 – OUTSTANDING

