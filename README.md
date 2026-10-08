# Cisco Packet Tracer – Enterprise VLAN Network

## Project Overview

This project demonstrates the design and configuration of a **VLAN-based enterprise network** using Cisco Packet Tracer.

The network is designed to separate different departments and user groups into dedicated VLANs while allowing controlled communication between them. Network security, traffic isolation, dynamic IP addressing, secure device management, and Layer 2 protection mechanisms are implemented as part of the project.

## Network Departments

The enterprise network is divided into the following logical departments:

* **HR**
* **IT**
* **Finance**
* **Guest**
* **Server**

Each department is assigned to a separate VLAN to provide logical network segmentation and improve security and network management.

## Key Features Implemented

* Designed a VLAN-based enterprise network for **HR, IT, Finance, Guest, and Server departments**.
* Implemented **802.1Q trunking** for carrying multiple VLANs between network devices.
* Configured **inter-VLAN routing** to enable controlled communication between different VLANs.
* Implemented **DHCP** for automatic IP address allocation to network clients.
* Configured **STP (Spanning Tree Protocol)** to prevent Layer 2 switching loops.
* Implemented **ACLs (Access Control Lists)** to control and restrict network traffic.
* Configured **SSH** for secure remote management of Cisco network devices.
* Configured **PortFast** to allow end devices to transition quickly to the forwarding state.
* Implemented **BPDU Guard** to protect access ports from unauthorized BPDU messages.
* Disabled unused switch ports to reduce potential security risks.
* Tested **inter-VLAN connectivity** between authorized departments.
* Tested **Guest traffic isolation** to prevent unauthorized access to internal departmental resources.

## VLAN Design

The network uses separate VLANs for different departments.

| Department | VLAN | Purpose          |
| ---------- | ---: | ---------------- |
| HR         | VLAN | HR users         |
| IT         | VLAN | IT users         |
| Finance    | VLAN | Finance users    |
| Guest      | VLAN | Guest users      |
| Server     | VLAN | Server resources |

> The exact VLAN IDs and IP addressing can be viewed in the Packet Tracer project file.

## 802.1Q Trunking

802.1Q trunking is configured on appropriate switch-to-switch and switch-to-router links.

A trunk allows traffic from multiple VLANs to travel through a single physical link using VLAN tags.

This enables the different departmental VLANs to communicate with the appropriate Layer 3 device for routing.

## Inter-VLAN Routing

Because each VLAN represents a separate logical network, devices in different VLANs require Layer 3 routing to communicate.

Inter-VLAN routing is configured to allow communication between authorized VLANs.

For example:

```text
HR VLAN
   ↓
Inter-VLAN Routing
   ↓
IT VLAN
```

Access between VLANs is controlled according to the configured network security policies.

## DHCP Configuration

DHCP is implemented to automatically assign network configuration information to client devices.

DHCP can provide:

* IP address
* Subnet mask
* Default gateway
* DNS information

This reduces the need to manually configure IP addresses on every client.

## STP – Spanning Tree Protocol

STP is implemented to prevent Layer 2 switching loops in the network.

It helps prevent problems such as:

* Broadcast storms
* Duplicate frames
* MAC address instability
* Network loops

STP determines the appropriate forwarding and blocking paths when redundant links exist.

## ACL – Access Control Lists

ACLs are configured to control network traffic between different parts of the network.

ACLs can be used to:

* Permit authorized traffic
* Deny unauthorized traffic
* Restrict access to sensitive resources
* Isolate Guest traffic from internal networks

This provides an additional layer of network security.

## Guest Network Isolation

The Guest VLAN is separated from internal departmental networks.

Traffic is tested to ensure that guest users cannot access restricted internal resources such as:

* HR systems
* Finance systems
* IT resources
* Internal servers

At the same time, permitted network services can remain accessible according to the configured ACL rules.

## SSH Secure Management

SSH is configured to provide secure remote access to Cisco network devices.

SSH provides encrypted communication between the administrator and the network device, making it more secure than unencrypted remote-management methods.

## PortFast

PortFast is configured on appropriate access ports connected to end devices.

It allows a connected end device to move to the forwarding state more quickly instead of going through the normal STP transition process.

## BPDU Guard

BPDU Guard is configured on appropriate PortFast-enabled access ports.

It helps protect the network from unauthorized switches or devices sending BPDU messages through an end-device port.

This improves Layer 2 network security.

## Unused Port Security

Unused switch ports are disabled to reduce the possibility of unauthorized devices being connected to the network.

This is a basic but important network-hardening practice.

## Testing and Verification

The network was tested to verify that the configured services and security controls work correctly.

### Connectivity Testing

Connectivity was tested using:

```text
ping <destination-IP>
```

### VLAN Verification

VLAN configuration can be verified using:

```text
show vlan brief
```

### Trunk Verification

Trunk configuration can be checked using:

```text
show interfaces trunk
```

### STP Verification

STP status can be checked using:

```text
show spanning-tree
```

### MAC Address Verification

The switch MAC address table can be viewed using:

```text
show mac address-table
```

### ACL Verification

Configured ACLs can be examined using:

```text
show access-lists
```

### SSH Verification

SSH configuration can be checked using:

```text
show ip ssh
```

## Testing Results

The following network scenarios were tested:

* Inter-VLAN connectivity between authorized departments.
* Communication between clients and the Server VLAN.
* DHCP-based IP address assignment.
* VLAN segmentation.
* Guest traffic isolation.
* ACL-based traffic filtering.
* STP operation.
* Secure SSH-based device management.
* PortFast and BPDU Guard security mechanisms.

## Security Measures

The project incorporates multiple network-security practices:

1. **VLAN segmentation** – Separates departments into different logical networks.
2. **ACLs** – Controls traffic between networks.
3. **Guest isolation** – Prevents guest users from accessing restricted internal resources.
4. **SSH** – Provides encrypted remote device management.
5. **BPDU Guard** – Protects access ports against unauthorized BPDU messages.
6. **PortFast** – Optimizes end-device access ports.
7. **Unused-port shutdown** – Reduces the attack surface of switches.

## Technologies and Concepts

* Cisco Packet Tracer
* Cisco IOS
* VLAN
* 802.1Q Trunking
* Inter-VLAN Routing
* DHCP
* STP
* ACL
* SSH
* PortFast
* BPDU Guard
* MAC Address Learning
* Network Security
* IP Addressing
* Network Troubleshooting

## How to Open the Project

1. Download the `.pkt` file from this repository.
2. Install Cisco Packet Tracer.
3. Open the downloaded `.pkt` file using Cisco Packet Tracer.
4. Explore the network topology and device configurations.
5. Use the Cisco IOS commands mentioned above to verify the configuration.

## Project File

**Cisco Packet Tracer Project:** `.pkt`

## Learning Outcomes

Through this project, I gained practical experience in designing and configuring an enterprise-style Cisco network.

I learned how to:

* Design a structured VLAN-based network.
* Segment departments using VLANs.
* Configure 802.1Q trunking.
* Implement inter-VLAN routing.
* Configure DHCP.
* Configure and verify STP.
* Implement ACL-based traffic control.
* Configure SSH for secure device management.
* Apply Layer 2 security using PortFast and BPDU Guard.
* Disable unused switch ports.
* Troubleshoot network connectivity.
* Test and verify network security and Guest traffic isolation.

## Author

**Tamanna Saini**

MCA Student

GitHub: **tamannahr07**
