# Lab Environment



## Network Architecture



VirtualBox Internal Network: `arp-lab`



### Kali Linux - Attacker



- Lab Interface: eth1

- IPv4: 192.168.50.10/24

- Role: Attacker and packet analysis

- Tools: Wireshark



### Ubuntu Desktop - Victim



- Lab Interface: enp0s8

- IPv4: 192.168.50.20/24

- Role: Victim



### Ubuntu Server - Server



- Lab Interface: enp0s8

- IPv4: 192.168.50.1/24

- Role: Server



## Network Isolation



Each VM uses two virtual network adapters:



- Adapter 1: NAT

- Adapter 2: VirtualBox Internal Network (`arp-lab`)



The internal network is used exclusively for security experiments.

