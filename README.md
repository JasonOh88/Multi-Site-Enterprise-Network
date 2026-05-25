Multi-Site Enterprise Network Infrastructure

📌 Project Overview
This project demonstrates the design and configuration of a multi-site enterprise network using Cisco Packet Tracer. The objective was to build a fully functional, routed infrastructure from a single Class C IP block, connecting a Headquarters (HQ) and two remote branch offices (Branch A and Branch B) while providing centralized web and DNS services.

🎯 Skills & Technologies Demonstrated
Subnetting (VLSM): Efficiently carved a 192.168.50.0/24 block into multiple subnets to support specific host requirements across different sites without wasting IP addresses.

Routing: Established end-to-end Layer 3 connectivity across isolated LANs using explicit static routes and default routes.

Cisco IOS Configuration: Configured router interfaces, assigned IP addresses, and enabled Layer 1/2 connectivity across serial WAN links.

Systems Integration: Deployed a central server to handle DNS resolution (hq.local) and host internal HTTP web services for remote clients.

Network Troubleshooting: Verified connectivity using ICMP (ping) and ARP processes to ensure successful packet delivery across the WAN.


🏗️ Network Topology

<img width="1911" height="705" alt="Screenshot 2026-05-25 081404" src="https://github.com/user-attachments/assets/c7e47b2d-221f-491f-beb6-950c9f7e5877" />


The network utilizes a daisy-chain WAN topology (HQ ➔ Branch A ➔ Branch B) requiring careful static route configuration for the "middleman" router (Branch A) to ensure packets reach their correct destinations on either side of the network.

📊 IP Addressing & VLSM Scheme
The entire infrastructure is built using the 192.168.50.0/24 network block.
Subnet Name,Network Address,CIDR,Subnet Mask,Usable Host Range,Broadcast Address
HQ LAN (60 Hosts),192.168.50.0,/26,255.255.255.192,.1 - .62,.63
Branch A LAN (28 Hosts),192.168.50.64,/27,255.255.255.224,.65 - .94,.95
Branch B LAN (14 Hosts),192.168.50.96,/28,255.255.255.240,.97 - .110,.111
HQ to BR-A WAN (2 Hosts),192.168.50.112,/30,255.255.255.252,.113 - .114,.115
BR-A to BR-B WAN (2 Hosts),192.168.50.116,/30,255.255.255.252,.117 - .118,.119

Repository Contents
Multi-Site-Enterprise.pkt: The fully configured Cisco Packet Tracer project file.

Router_Configs/: Directory containing the raw CLI configuration .txt scripts for HQ, Branch A, and Branch B routers.

Images/: Network diagrams and screenshots verifying connectivity (Ping tests to endpoints and successful DNS/HTTP resolution).

✅ Verification

<img width="1919" height="1018" alt="Screenshot 2026-05-25 081343" src="https://github.com/user-attachments/assets/b1baa57b-3ea5-417d-9dd7-5d0f28bc4340" />

