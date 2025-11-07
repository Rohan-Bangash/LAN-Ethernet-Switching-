# LAN Ethernet Switching Lab

Layer 2 networking lab built in Cisco Packet Tracer demonstrating ARP resolution and dynamic switch MAC address learning.

---

## Overview
This lab simulates an Ethernet LAN environment using Cisco Packet Tracer.  
The goal was to test host-to-host communication across two switches and observe how the Address Resolution Protocol (ARP) and ICMP operate within a Layer 2 network.

---

## Network Topology

**Devices:**
- 4 PCs: PC1–PC4  
- 2 Switches: SW1, SW2  
- Network: 192.168.1.0/24  

**Connections:**
- PC1 → SW1 (FastEthernet0/1)  
- PC2 → SW1 (FastEthernet0/2)  
- SW1 → SW2 (GigabitEthernet0/1)  
- PC3 → SW2 (FastEthernet0/1)  
- PC4 → SW2 (FastEthernet0/2)

<img width="1919" height="1027" alt="01" src="https://github.com/user-attachments/assets/4615da33-f7e4-4ae1-9447-b65c56adc462" />

---

## Objectives
- Establish communication between PC1 and PC3.  
- Observe how ARP is used to map IP addresses to MAC addresses before data transmission.  
- Use **show** and **clear** commands to view and reset switch MAC address tables.  
- Monitor ICMP echo requests/replies (pings) in Simulation Mode to visualize data flow.

---

## Commands Used

### On Switches:
show mac address-table

clear mac address-table dynamic

show interfaces status

### On PCs:
ipconfig /all

ping 192.168.1.3

arp -a

---

## Key Observations
- When PC1 pings PC3 for the first time, ARP requests are broadcasted across the LAN.  
- Switches dynamically learn the MAC addresses of connected devices as traffic passes.  
- Once ARP resolves the MAC address of PC3, ICMP Echo Requests/Replies flow directly between the two hosts.  
- Clearing the MAC table forces the switch to relearn addresses, demonstrating dynamic MAC learning in real time.

---

## Concepts Demonstrated
- OSI Model: Focus on Layer 2 (Data Link) and Layer 3 (Network) interaction.  
- ARP operation and MAC learning.  
- Ethernet switching and connectivity testing.  
- Use of simulation tools for network analysis.

---

## Tools Used
- Cisco Packet Tracer  
- Command Prompt / Cisco IOS CLI  

---

## What I Learned
- How Ethernet switches build and maintain MAC address tables dynamically.  
- The role of ARP in enabling IP communication within the same subnet.  
- How to use Cisco IOS commands to monitor and troubleshoot network behavior.  
- How to visualize and interpret packet flow using Cisco Packet Tracer Simulation Mode.
