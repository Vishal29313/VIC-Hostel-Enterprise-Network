
# VIC Hostel Enterprise Network

## Problem Statement

Design and simulate a reliable, secure, and scalable network infrastructure for a multi-floor hostel. The network should provide proper department-wise segmentation, inter-network communication, automatic IP address assignment, dynamic routing, secure remote administration, and protection against unauthorized device access.

## Project Overview

VIC Hostel Enterprise Network is an enterprise network simulation developed using Cisco Packet Tracer. The network is designed across multiple floors with separate VLANs for different departments.

The project demonstrates practical implementation of VLAN segmentation, 802.1Q trunking, inter-VLAN routing, DHCP, OSPF, SSH, and switch port security.

## Objectives

- Design a multi-floor hostel network infrastructure.
- Separate departments using VLANs.
- Enable communication between different VLANs using inter-VLAN routing.
- Automate IP address assignment using DHCP.
- Implement dynamic routing using OSPF.
- Enable secure remote administration using SSH.
- Protect switch ports against unauthorized devices.
- Test and verify end-to-end network connectivity.

## Technologies Used

- Cisco Packet Tracer
- IPv4
- VLAN
- 802.1Q Trunking
- Router-on-a-Stick
- Inter-VLAN Routing
- DHCP
- OSPF
- SSH
- Port Security

## Network Architecture

The network consists of multiple floors, routers, and switches. Each department is assigned a separate VLAN and IP subnet.

The routers are interconnected using serial links and OSPF is used for dynamic routing between networks.

## Key Features

### VLAN Segmentation
Different departments are separated into dedicated VLANs to improve network organization and security.

### Inter-VLAN Routing
Router-on-a-Stick is implemented to allow communication between different VLANs.

### DHCP
Routers provide automatic IP address configuration to end devices.

### OSPF
OSPF is configured to dynamically exchange routing information between the routers.

### SSH
SSH provides secure remote access to network devices for administration.

### Port Security
Switch port security is used to restrict unauthorized devices from accessing protected switch ports.

## Testing and Verification

The network was verified using:

- VLAN verification
- Trunk verification
- Interface status verification
- DHCP verification
- OSPF neighbor verification
- Routing table verification
- Inter-VLAN connectivity testing
- SSH remote access testing
- Port security verification

## Project File

The Cisco Packet Tracer simulation file is included in this repository:

`VIC-Hostel-Enterprise-Network.pkt`

## Author

**Vishal**