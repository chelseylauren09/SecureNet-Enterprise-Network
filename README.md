# SecureNet Solutions — Multi-Branch Enterprise Network

## Project Overview

This project involves designing, configuring, and testing a simulated multi-branch enterprise network using Cisco Packet Tracer.

The network connects offices in Johannesburg, Durban, and Cape Town through a routed WAN. It includes departmental VLANs, automatic IP address allocation, dynamic routing, guest network restrictions, secure remote device management, and simulated internet connectivity.

The project demonstrates practical networking and entry-level network security skills.

## Objectives

* Design a multi-branch enterprise network topology.
* Separate departments using Virtual Local Area Networks (VLANs).
* Configure inter-VLAN routing using router subinterfaces.
* Automate IP address allocation using DHCP.
* Enable dynamic routing between branches using OSPF.
* Restrict guest network access using Access Control Lists (ACLs).
* Secure remote router management using SSH.
* Configure Network Address Translation (NAT) for simulated external connectivity.
* Test network connectivity and troubleshoot configuration issues.

## Technologies and Protocols

* Cisco Packet Tracer
* Cisco 2911 routers
* VLANs and trunking
* Inter-VLAN routing
* DHCP
* OSPF
* Access Control Lists (ACLs)
* SSH version 2
* NAT/PAT
* IPv4 addressing and subnetting
* Network troubleshooting

## Network Design

The simulated network consists of three branch offices:

* **Johannesburg:** Multiple departmental VLANs, including Management, Finance, HR, IT, Servers, Guest, and Network Management.
* **Durban:** Staff, IT, and Guest networks.
* **Cape Town:** Staff, IT, and Guest networks.
* **Internet Edge:** Connects the internal network to a simulated external network.
* **Server Farm:** Hosts an internal web server and a DNS/DHCP server.

The branch routers use point-to-point serial links and OSPF to exchange routing information.

## Key Configurations

### 1. VLANs and Inter-VLAN Routing

Created separate VLANs for departments and configured router subinterfaces to enable communication between permitted networks.

### 2. DHCP

Configured DHCP pools to automatically assign IP addresses, default gateways, and DNS settings to client devices across the branch networks.

### 3. OSPF

Configured OSPF in area 0 to exchange routes between the branch routers. Verified OSPF neighbour relationships and learned routes.

### 4. Guest Network Security

Configured extended ACLs to restrict guest networks from accessing designated internal networks while allowing DHCP traffic.

### 5. SSH and Device Security

Configured SSH version 2, local user authentication, restricted VTY access to SSH, enable secrets, and warning banners on the branch routers.

### 6. NAT and External Connectivity

Configured NAT overload at the Internet Edge router to translate internal source addresses for external connectivity. Added the required return route and verified successful connectivity to the simulated external test server.

### 7. Server and Connectivity Testing

Configured internal server addressing and an internal web service. Tested client-to-server connectivity and verified that guest restrictions operated as intended.

## Testing and Verification

The following tests were completed:

* Client devices received IP addresses through DHCP.
* OSPF neighbours reached the FULL state.
* Routes were learned between branch networks.
* Guest ACLs blocked access to designated internal resources.
* SSH configuration was verified on the routers.
* An internal client successfully accessed the internal web server.
* A Durban staff client successfully pinged the simulated external test server through NAT.

## Repository Contents

* **Packet Tracer file:** The simulated network topology and device configurations.
* **Configurations:** Router configuration text files.
* **Documentation:** Network configuration report with labelled screenshots.
* **Screenshots:** Visual evidence of the topology, configurations, and testing.

## Skills Demonstrated

* Network design and configuration
* VLAN segmentation
* IPv4 addressing and subnetting
* DHCP configuration
* Dynamic routing with OSPF
* Network access control
* Secure remote administration
* NAT configuration
* Connectivity testing and troubleshooting
* Technical documentation

## Limitations

This project was developed and tested in Cisco Packet Tracer. It is a simulated environment and does not represent a production deployment.

DNS hostname resolution was not fully completed across all client devices. The internal web server was successfully accessed using its IP address.

## Author

An independent networking and cybersecurity portfolio project developed to practise enterprise network design, configuration, security, and troubleshooting.
