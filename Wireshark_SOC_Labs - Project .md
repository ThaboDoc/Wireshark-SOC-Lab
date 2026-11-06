## Overview

This document a practical SOC investigation using Wireshark to capture and analyse network traffic.
The objective is to identify unusual network behaviour, investigate suspicious connections and detect 
potential malicious activity.

## Investigation Evidence Results

## Wireshark SOC LAB 3
<img src="lab3.PNG" width="300" height="300"  alt="Lab 3">

## Identify the Attackers IP.
I have managed to track and find the IP address of the attacker and the opened/closed Ports that were 
tested by the intruder. I also manage to learn more about the port scan investigation using wireshark.

What I learned is that attackers often scan multiple ports on a target system to identify open
ports and potential vulnerabilities. If the same IP address appears repeatedly while
attempting to communicate through multiple ports, it may indicate suspicious activity or a
possible port-scanning attack. 

Attackers commonly use TCP to establish connections and probe target systems for accessible
services. Monitoring repeated connection attempts, source IP addresses and TCP traffic
patterns can help identify potential reconnaissance activities during network traffic analysis.

## Wireshark SOC LAB 4

<img src="lab4.PNG" width="300" height="300" alt="Lab 4">

## Follow TCP Stream Part 1

I learned that conversations and data transmitted over HTTP are not encrypted,
which means sensitive information such as usernames, passwords and private messages 
can potentially be intercepted and exposed by attackers.
This highlights the importance of using HTTPS with TLS encryption to protect data in transit
ensuring that communication between users and web servers remains confidential and secure.

## Wireshark SOC Lab 5

<img src="lab5.PNG" width="300" height="350" alt="Lab 5">

## Follow TCP Stream Part 2

In this lab, I managed to identify hidden information embedded within a file. 
I learned that information can be concealed in HTML files using comments
such as "<!-- Hidden -->". 
which are not displayed on the webpage but can still be viewed by inspecting the HTML 
source code. This demonstrates how hidden information can be discovered through basic file 
and source code analysis.

## Wireshark SOC LAB 6
<img src="lab6.PNG" width="300" height="350" alt="Lab 6">

## HTTP plain text credentials

HTTPS uses TLS encryption to protect data transmitted between users and web servers, 
ensuring that sensitive information cannot easily be read if network traffic is 
captured using tools such as Wireshark. 

Instead of exposing credentials in plain text, the encrypted traffic appears unreadable to
anyone attempting to intercept it without the appropriate decryption keys. 
This helps maintain data confidentiality and protect users against credential theft 
and unauthorised access.

## Wireshark SOC LAB 7
<img src="lab7.PNG" width="300" height="350" alt="Lab 7">

## Brute force catch

## Wireshark SOC LAB 8
<img src="lab8.PNG" width="300" height="350" alt="Lab 8">

## Overall results and summary
<img src="SOC_Labs.png" width="300" height="350" alt="SOC_Labs">

This is the summarized report of the results for my LAB Projects
LAB 3 =  Identify the Attackers IP :  90/100 Outstanding

lab 4 = Follow TCP Stream Part 1   :  90/100 Outstanding

lab 5 = Follow TCP Stream Part 2   :  100/100 outstanding

lab 6 = HTTP plain text credentials:  90/100 Outstanding

lab 7 = Brute force catch          :  100/100 outstanding

Lab 8 = VoIP call replay           : 90/100 Outstanding

