# ARP Spoofing and MITM Security Lab



## Overview



This project explores network-layer attacks and defensive mechanisms in an

isolated virtual network environment. The initial phase focuses on ARP

spoofing and Man-in-the-Middle (MITM) attacks, including packet capture and

traffic analysis using Wireshark.



A later extension of the project will investigate TCP session security and

session hijacking techniques in a controlled environment.



## Lab Environment



The experiment is conducted entirely within an isolated VirtualBox network.



| Machine | Role | Operating System | Lab IP |

|---|---|---|---|

| Kali Linux | Attacker | Kali Linux 2024.2 | 192.168.50.10 |

| Ubuntu Desktop | Victim | Ubuntu Linux | 192.168.50.20 |

| Ubuntu Server | Server | Ubuntu Server | 192.168.50.1 |



The machines communicate through a VirtualBox Internal Network named

`arp-lab`.



Internet access is separated from the experimental network using an

additional NAT adapter.



## Project Roadmap



\- \[x] Build isolated virtual network

\- \[x] Establish normal communication between hosts

\- \[x] Capture baseline ARP traffic with Wireshark

\- \[ ] Demonstrate ARP cache poisoning

\- \[ ] Establish a controlled MITM position

\- \[ ] Analyze intercepted network traffic

\- \[ ] Investigate detection and defensive mechanisms

\- \[ ] Explore TCP session security as an advanced extension


## Baseline ARP Analysis



Before introducing ARP spoofing, normal ARP resolution was captured between

the hosts to establish a baseline.



The victim correctly associates the server IP address:



`192.168.50.1`



with the server's legitimate MAC address.



This baseline will later be compared against the ARP cache during the

spoofing experiment.

### Normal ARP Resolution

![Normal ARP Resolution](screenshots/01-normal-arp-resolution.png)

Wireshark shows the normal ARP request and reply process before any
ARP poisoning is introduced.


