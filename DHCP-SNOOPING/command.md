## DHCP Snooping – Definition

DHCP Snooping is a Layer 2 security feature on network switches that monitors and controls DHCP traffic within a Local Area Network (LAN). It works by allowing DHCP messages only from trusted interfaces while blocking unauthorized or rogue DHCP servers.

By building and maintaining a DHCP binding table that maps IP addresses to MAC addresses, VLANs, and switch ports, DHCP Snooping helps prevent attacks such as rogue DHCP servers, DHCP starvation, and man-in-the-middle (MITM) attacks.

This feature is commonly used in enterprise networks to improve overall network reliability, integrity, and access control.

## What DHCP Snooping Is Used For

DHCP Snooping is used to secure a network by controlling how DHCP traffic flows between clients and servers. It ensures that only authorized DHCP servers can assign IP addresses to devices on the network.

Specifically, DHCP Snooping is used to:
- Prevent rogue DHCP servers from distributing incorrect or malicious IP configurations
- Protect against DHCP starvation attacks that exhaust the IP address pool
- Block man-in-the-middle (MITM) attacks by validating DHCP messages
- Build a trusted DHCP binding table for IP-to-MAC address verification
- Serve as a foundation for additional security features such as Dynamic ARP Inspection (DAI) and IP Source Guard

Overall, DHCP Snooping improves network security, stability, and trust at the access layer of a switched network.

## Virtual Lab Environment

This project was implemented in a virtual lab environment using **Cisco Packet Tracer**.  
The simulation represents a real-world enterprise network scenario, with the difference being that all devices are virtualized.

The environment includes standard networking devices configured as they would be in a physical setup, allowing for realistic testing and validation of security configurations such as DHCP Snooping.

Although the devices are virtual, the configurations, behavior, and security concepts applied directly reflect real-life network implementations.

## Devices Used in the Virtual Lab

The following devices were used to simulate a real-world LAN environment in **Cisco Packet Tracer**:

- **Cisco Catalyst 2960 Switch**
  - Used as the access layer switch
  - Configured with DHCP Snooping and Port Security

- **DHCP Server**
  - Acts as the legitimate DHCP server
  - Connected to a trusted switch interface

- **End-User Devices (PCs)**
  - Configured as DHCP clients
  - Used to test IP address assignment and security enforcement

All devices were configured using industry-standard Cisco IOS commands, ensuring that the lab closely reflects real-life enterprise network behavior.



## Cisco IOS Configuration – DHCP Snooping & Port Security

```bash
enable
configure terminal

! Enable DHCP Snooping globally
ip dhcp snooping

! Enable DHCP Snooping on VLAN 1
ip dhcp snooping vlan 1

! Configure trusted interface (Connected to the real DHCP Server)
interface GigabitEthernet0/1
 description Trusted DHCP Server Port
 ip dhcp snooping trust
 exit

! Configure access ports with DHCP rate limiting
interface range GigabitEthernet0/2 - 24
 description End-User Access Ports
 switchport mode access
 ip dhcp snooping limit rate 15

 ! Enable Port Security for additional hardening
 switchport port-security
 switchport port-security maximum 2
 switchport port-security violation restrict
 exit

! Save configuration
end
write memory

show ip dhcp snooping
show ip dhcp snooping binding
show ip dhcp snooping statistics
show port-security interface GigabitEthernet0/2






