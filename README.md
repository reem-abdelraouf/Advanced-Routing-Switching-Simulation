#  CCNA & CCNP Comprehensive Practice Lab

## 📝 Project Overview
This project is an **educational practice lab** specifically designed for networking students, CCNA/CCNP candidates, and IT professionals. It provides a fully functional, simulated enterprise environment in **Cisco Packet Tracer** to practice and master advanced networking topics. 

Whether you want to train on complex routing scenarios, inter-VLAN routing, wireless integration, or network management services like **NTP** and **Syslog**, this topology has it all.

##  Network Topology
![TOPOLGY 2.png]

## 🚀 Key Learning Objectives & Features

### 1.  Advanced Routing (Redistribution & Virtual Links)
*   **Educational Focus:** The routing domain is intentionally designed to practice **Mutual Route Redistribution**, **OSPF Virtual Links**, and **Routing Authentication**.
*   **Multi-Area OSPF:** Configured with Area 0 (Backbone), Area 50, and Area 100. Includes **Virtual Link** configuration to connect disconnected areas to the backbone.
*   **EIGRP (AS 200) & RIPv2:** Configured in different wings of the network to simulate a multi-vendor/legacy integrated environment.
*   **Route Redistribution:** Centralized ISR4331 router acts as the core hub, successfully redistributing routes between OSPF, EIGRP, and RIP.
*   **Routing Security:** Secured routing updates using **MD5 Authentication** for both OSPF and EIGRP neighbors.

### 2.  Network Management (NTP & Syslog)
*   **NTP (Network Time Protocol):** A central server is deployed to synchronize the clocks of all routers and switches across the network.
*   **Syslog:** All network devices are configured to forward event messages, errors, and interface status logs to a centralized Syslog Server for monitoring and troubleshooting.

### 3.  Layer 2, Switching & Security
*   **VLANs & Trunks:** Segmented broadcast domains (VLAN 10, VLAN 20) with IEEE 802.1Q trunking.
*   **Inter-VLAN Routing:** Handled by Cisco 3560 Multilayer Switches using Switch Virtual Interfaces (SVIs).
*   **EtherChannel (PAgP):** Link aggregation configured between core Multilayer Switches for redundancy and higher bandwidth.
*   **Switch Port Security:** Configured to restrict unauthorized access at the access layer.

### 4.  Enterprise Wireless (WLC & CAPWAP)
*   **Wireless LAN Controller (WLC):** Centralized management for the wireless infrastructure.
*   **Lightweight Access Points (LAPs):** Configured to dynamically discover and join the WLC.
*   **Wireless DHCP:** The WLC manages internal DHCP scopes to lease IP addresses to management LAPs and wireless clients.

## 💻 How to Use This Lab
1. Download the `.pkt` file from this repository.
2. Open it using **Cisco Packet Tracer** (Version 8.0 or later recommended).
3. Allow a few seconds for the network to converge (STP states, OSPF/EIGRP adjacencies, and LAP-to-WLC associations).
4. **Practice:** Delete the routing configurations, redistribution, or Syslog commands and try to build them from scratch!
5. Access the central router's CLI and use `show ip route` to view the redistributed external routes (`O E2`, `D EX`, `R`).

---
*Created by [Reem Abdelraouf] - Feel free to fork this repository, practice the topics, and reach out if you have any questions!*
