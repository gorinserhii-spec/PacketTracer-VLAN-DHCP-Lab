# 🌐 Packet Tracer Network Lab — VLAN + Routing + DHCP
=================================================

## 📌 Description
-----------
This educational project demonstrates the setup of a functional corporate network in Cisco Packet Tracer,
showcasing the use of VLANs, inter-VLAN routing, DHCP, and static routing to connect two branches.
The goal is to create a segmented, secure, and scalable network environment that illustrates foundational
networking concepts.

## 🎯 Objectives
----------
- Configure VLAN10 and VLAN20 to segment network traffic.
- Implement inter-VLAN routing using Router-on-a-Stick.
- Set up DHCP servers on routers for automated IP address assignment.
- Connect two branches using static routing for inter-router communication.

## 🛠 Equipment Used
--------------
- 2x Cisco 4331 Router
- 2x Cisco 2960 Switch
- 3x PC
- Cisco Packet Tracer 8.x

## Key Concepts
------------
- VLANs (Virtual Local Area Networks): The network is segmented into VLAN10 and VLAN20 to isolate traffic,
  enhance security, and reduce broadcast traffic.
  + VLAN 10: Assigned to PC1 in the main branch and PC3 in the branch office.
  + VLAN 20: Assigned to PC2 in the main branch.
- Router-on-a-Stick: On Router1, a single physical interface (GigabitEthernet0/0/0) is configured with logical
  sub-interfaces to route traffic between VLAN10 and VLAN20, optimizing resource use without requiring multiple physical ports.
- Inter-Router Communication: The two routers are connected via a dedicated link (GigabitEthernet).

## 🔧 Configuration Summary
---------------------
- Router1: Manages inter-VLAN routing for VLAN10 and VLAN20 and provides DHCP services for these subnets.
- Switch1: Segments the main branch network, assigning PC1 to VLAN10 and PC2 to VLAN20, and connects to Router1 via a trunk port.
- Router2: Manages the branch office network, provides DHCP services for PC3, and handles routing to the main branch network.
- Switch2: Connects PC3 to Router2 using a trunk port with a native VLAN to process DHCP requests correctly.
- Configurations are located in the [configs/] folder.

## 📷 Screenshots
-----------
- Network Diagram: diagram.png
- Vlan Config: screenshots/vlan_config.png
- Ping Test: screenshots/ping_test_pc.png

## 🚀 How to Run
----------
1. Open lab.pkt in Cisco Packet Tracer.
2. Start the simulation.
3. Verify connectivity using the ping command.

## Summary
-------
This project successfully demonstrates how to build a scalable and well-organized corporate network infrastructure
using VLANs, Router-on-a-Stick, DHCP, and static routing. It highlights the principles of network segmentation,
efficient routing, and automated IP management for a secure and functional network environment.

---
# Author: Serhii Gorin 
# Date: 10.08.2025
