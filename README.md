Enterprise Network Security Architecture Lab

Overview

This project demonstrates the design and immplementation of a segmented enterprise network architecture using Cisco Packet Tracer. The lab model a realistic corporate environment consisting of departmental networks, a centralized data center, and a demilitarized zone (DMZ) used to host public-facing services. The goal of this project was to practice enterprise network design concepts including VLAN segmentation, Layer-3 switching, trunking, routing, and basic security controls.

Network Topology

The topology located under screenshots represents a multi-tier enterprise network with distinct layers responsible for routing, switching, and access control.

Network Architecture

The network follows a hierarchial enterprise model, commonly used in corporate infrastructure environments.
Internet
   │
Edge Routers
   │
Core Layer (Layer 3 Switching)
   │
Access Layer (Department Networks)
   │
Data Center + DMZ

Core Layer

The core layer is responsible for high-speed routing between VLANs and acts as the central point of communication between all internal network segments.

Access Layer

Access switches connect end user devices such as PCs. Each department operates within its own VLAN to maintain traffic segmentation.

Data Center

A dedicated VLAN hosts enterprise services including DNS, Web, Mail, File, and DHCP servers.

DMZ

The DMZ network allows external users or networks to access specific services without exposing the entire internal network to potential threats.

VLAN Design
| VLAN | Network      | Purpose         |
| ---- | ------------ | --------------- |
| 10   | 10.10.0.0/24 | HR Network      |
| 20   | 10.20.0.0/24 | Finance Network |
| 30   | 10.30.0.0/24 | IT Network      |
| 50   | 10.50.0.0/24 | Data Center     |
| 60   | 10.60.0.0/24 | DMZ             |

Key Networking Concepts Implemented

VLAN Segmentation

Departmental networks were separated using VLANs to isolate broadcast domains and improve traffic organization.

Inter-VLAN Routing

Layer-3 switching enables communication between internal VLAN networks.

802.1Q Trunking

Trunk links were configured between switches to allow multiple VLANs to traverse a single physical connection.

Data Center Infrastructure

Internal enterprise services are hosted within a dedicated data center network.

DMZ Network

The DMZ hosts externally accessible services while protecting the internal enterprise network.

Access Control Lists (ACL)

ACL rules were implemented to control traffic flow between internal networks and the DMZ.

Network Validation

Connectivity followed by configuration were verified with:
VLAN and Trunk Verfication
Inter-VLAN Connectivity Test
DMZ Connectivity Test
ACL Security Rules

Respository Structure
enterprise-network-security-lab
│
├── configs
│   ├── core-sw1-config.txt
│   ├── core-sw2-config.txt
│   └── edge-router-config.txt
│
├── Screenshots
│   ├── topology.png
│   ├── vlan-verification.png
│   ├── inter-vlan-test.png
│   ├── dmz-connectivity.png
│   └── acl-rules.png
│
├── Enterprise_Security_Network.pkt
└── README.md

Nehemiah Frazier
Cybersecurity & Digital Forensics
