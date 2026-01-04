# Switched-network-design-and-L3-forwarding
Designed a redundant switched network with VLAN segmentation, trunking, and STP, then configured two routed networks and analyzed frame changes across a switch vs router using Packet Tracer simulation and PDU inspection.

Overview

This project demonstrates the design and implementation of a switched enterprise network with VLAN-based traffic segmentation, redundancy, and Layer 3 packet forwarding analysis using Cisco Packet Tracer.

The objective was to replace legacy hubs with switches to reduce collisions, improve resiliency through redundant links, and isolate departmental traffic for security purposes. The project also examines how packets are handled differently at Layer 2 (switching) versus Layer 3 (routing) by observing frame transformations as traffic traverses a router.

The work emphasizes network performance, security segmentation, and protocol behavior, combining VLAN configuration, trunking, Spanning Tree Protocol (STP), IP addressing, dynamic routing, and packet inspection.

Scope & Objectives

Design a switched network for a multi-floor building with multiple departments

Replace hubs with switches to eliminate collisions and improve network stability

Implement VLAN-based segmentation for departmental traffic isolation

Configure trunk links and allow only required VLANs across the backbone

Provide redundancy and failover using Spanning Tree Protocol (STP)

Configure Layer 3 addressing and routing between separate networks

Observe and analyze frame behavior as packets traverse switches and routers


Platform & Technology
Platform

Cisco Packet Tracer

Technologies & Concepts

Layer 2 switching and MAC address learning

VLAN configuration and access port assignment

802.1Q trunking

Spanning Tree Protocol (STP) for loop prevention and redundancy

IPv4 addressing (Class A and Class C private networks)

Layer 3 routing and default gateway configuration

RIP version 2 (RIPv2) dynamic routing

ICMP connectivity testing

Frame and packet inspection using PDU simulation



Part 1: Switched Network Design 

<img width="1522" height="1074" alt="image" src="https://github.com/user-attachments/assets/dd27a6b8-15af-48ad-92e9-9efdedcba7fa" />

Key Observations

Replacing hubs with switches eliminated collision-related performance issues by separating collision domains at each switch port.

VLAN segmentation successfully isolated departmental traffic, preventing unauthorized communication between Marketing, Sales, and Administration networks.

Trunk links enabled multiple VLANs to traverse a single backbone connection while maintaining logical separation of traffic.

Spanning Tree Protocol (STP) effectively prevented Layer 2 loops and ensured continued connectivity by activating alternate paths during link failures.

Centralizing servers within a dedicated VLAN allowed controlled access while simplifying network management and security enforcement.


Part 2: Layer 3 Configuration and Packet Switching


<img width="1636" height="986" alt="image" src="https://github.com/user-attachments/assets/9f2bb73b-56a5-48b1-83a8-13482497d352" />

Implementation Summary

Configured two private IPv4 networks (Class A and Class C) connected via a router

Assigned IP addresses, subnet masks, and default gateways to end hosts and router interfaces

Verified end-to-end connectivity using ICMP (ping) testing

Used Packet Tracer’s PDU simulation to observe frame behavior across switches and routers

Key Observations

IP addresses remain unchanged end-to-end during packet delivery

MAC addresses remain unchanged when frames pass through a switch

MAC addresses are rewritten when frames pass through a router

Routers forward traffic based on Layer 3 (IP) information, while switches forward traffic based on Layer 2 (MAC) information



