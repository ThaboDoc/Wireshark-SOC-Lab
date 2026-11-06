## Overview

This document a practical SOC investigation using Wireshark to capture and analyse network traffic.
The objective is to identify unusual network behaviour, investigate suspicious connections and detect 
potential malicious activity.

## Investigation Evidence Results

## Wireshark SOC Lab 3
<img src= "lab3.PNG" width ="450" alt"LAB 3">

## Identify the Attackers IP.
I have managed to track and find the IP address of the attacker and the opened/closed Ports that were 
tested by the intruder. I also manage to learn more about the port scan investigation using wireshark.

What I learned is that attackers often scan multiple ports on a target system to identify open ports and potential vulnerabilities. 
If the same IP address appears repeatedly while attempting to communicate through multiple ports,
it may indicate suspicious activity or a possible port-scanning attack. Attackers commonly use TCP to establish connections 
and probe target systems for accessible services. Monitoring repeated connection attempts, source IP addresses and TCP traffic patterns 
can help identify potential reconnaissance activities during network traffic analysis.
