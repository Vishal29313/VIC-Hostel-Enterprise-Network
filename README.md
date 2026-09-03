# VIC Hostel Enterprise Network

## Problem Statement

Design and simulate a reliable, secure, and scalable network infrastructure for a multi-floor hostel. The network should provide department-wise segmentation, communication between different networks, automatic IP address assignment, dynamic routing, secure remote administration, and protection against unauthorized device access.

## Project Overview

VIC Hostel Enterprise Network is an enterprise network simulation developed using Cisco Packet Tracer.

The network is designed across three floors with separate VLANs for different departments. Each floor contains a router and switch, while the routers are interconnected using serial links in a triangular topology.

The project demonstrates practical implementation of VLAN segmentation, 802.1Q trunking, Router-on-a-Stick inter-VLAN routing, DHCP, OSPF, SSH, and switch port security.

## Network Architecture

The network consists of:

- **3 Routers** — one router for each floor
- **3 Switches** — one switch for each floor
- **8 Departments**
- **8 VLANs**
- **3 Router-to-Router serial links**
- Department-specific end devices
- Router-on-a-Stick inter-VLAN routing
- OSPF dynamic routing between routers

### Departments, VLANs and IP Addressing

| Floor | Department | VLAN | Network | Default Gateway |
|---|---|---:|---|---|
| Floor 1 | Reception | 80 | 192.168.8.0/24 | 192.168.8.1 |
| Floor 1 | Store | 70 | 192.168.7.0/24 | 192.168.7.1 |
| Floor 1 | Logistics | 60 | 192.168.6.0/24 | 192.168.6.1 |
| Floor 2 | Sales | 30 | 192.168.3.0/24 | 192.168.3.1 |
| Floor 2 | HR | 40 | 192.168.4.0/24 | 192.168.4.1 |
| Floor 2 | Finance | 50 | 192.168.5.0/24 | 192.168.5.1 |
| Floor 3 | IT | 10 | 192.168.1.0/24 | 192.168.1.1 |
| Floor 3 | Admin | 20 | 192.168.2.0/24 | 192.168.2.1 |

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

## Key Features

### VLAN Segmentation

Each department is assigned a separate VLAN to logically segment the network and improve network organization.

### Inter-VLAN Routing

Router-on-a-Stick is implemented using 802.1Q subinterfaces to enable communication between different VLANs.

### DHCP

DHCP is configured to automatically assign IP addresses, default gateways, and DNS information to end devices.

### OSPF Dynamic Routing

OSPF is configured between the three routers to dynamically exchange routing information and provide connectivity between different floor networks.

### SSH Remote Administration

SSH is configured for secure remote administration of network devices. SSH provides encrypted communication compared with unencrypted Telnet access.

### Port Security

Switch port security is implemented on the required access port to restrict unauthorized devices. Sticky MAC learning is used to allow the authorized Test-PC.

## Network Connectivity Testing

The network was tested using Cisco Packet Tracer end devices and router/switch verification commands.

### Local Network Testing

For each department, connectivity can be verified by checking:

- DHCP-assigned IP address
- Default gateway connectivity
- Communication with devices in the same VLAN

### Inter-VLAN Testing

Connectivity was tested between devices belonging to different VLANs, including networks across different floors.

Example:

```text
IT → Admin       ✅
IT → Sales       ✅
IT → Finance     ✅
IT → Reception   ✅

## Network Topology

### Complete Network

The complete network consists of three floor-wise networks connected through three routers. The routers are interconnected using serial links to provide communication between different floor networks.

![Complete Network Topology](screenshots/complete-network-topology.png)

### Floor 1

Floor 1 contains the Reception, Store, and Logistics departments.

![Floor 1 Topology](screenshots/floor-1-topology.png)

### Floor 2

Floor 2 contains the Sales, HR, and Finance departments.

![Floor 2 Topology](screenshots/floor-2-topology.png)

### Floor 3

Floor 3 contains the IT and Admin departments. The IT network also contains the Test-PC used for SSH and security testing.

![Floor 3 Topology](screenshots/floor-3-topology.png)

### Router Interconnection

The three routers are interconnected using serial links in a triangular topology. This design provides multiple paths between routers and allows OSPF to dynamically determine available routes.

![Three Router Topology](screenshots/3-router-topology.png)