```markdown
# College Infrastructure in Cisco Packet Tracer

## Overview
This project focuses on the implementation of a college infrastructure simulation using Cisco Packet Tracer. The goal is to design and simulate a network that reflects the networking needs of a typical college environment. The infrastructure includes various networking devices, such as routers, switches, and end devices, to create a comprehensive and functional network setup.

## Features

- Network Topology: A detailed representation of the college network topology, showcasing the interconnection of different departments, labs, and administrative areas.

- Device Configuration: Configuration of Cisco devices, including routers and switches, to ensure proper communication and data flow within the network.

- Subnetting and IP Addressing: Implementation of subnetting and IP addressing to efficiently manage and organize the IP space for different departments and segments of the college.

- VLAN Setup: Utilization of Virtual LANs (VLANs) to segment the network, providing enhanced security and network management capabilities.

- Routing Protocols: Configuration of routing protocols such as OSPF or EIGRP to enable dynamic routing and efficient data transfer between different parts of the college network.

## General Commands

This is the first command in the CLI of a router, switch, or other networking device in Cisco Packet Tracer.

- `en` (enable):
  - Description: Enters privileged EXEC mode, allowing access to all router commands.

- `conf t` (configure terminal):
  - Description: Enters global configuration mode for making changes to the router's configuration.

## Switch Configuration

- `switchport mode [access/trunk]` (e.g., `switchport mode access/trunk`):
  - Description: Configures an interface as an access or trunk port.

- `switchport access vlan [VLAN_ID]` (e.g., `switchport access vlan 10`):
  - Description: Assigns an access VLAN to an interface.

## DHCP Configuration

- `show ip dhcp pool` :
  - Description: Displays information about configured DHCP pools, including allocated addresses, lease durations, and pool utilization.

## Interface Selection and Configuration

- `interface` or `int [interface_type] [interface_number]` (e.g., `interface GigabitEthernet0/0/0`):
  - Description: Enters the configuration mode for a specific interface.

- `interface range` or `int-range [interface_type] [start_range] - [end_range]` (e.g., `interface range GigabitEthernet0/0/1 - 2`):
  - Description: Enters the configuration mode for a range of interfaces.

## DHCP Pool Configuration

Example:

```bash
>> Router(config)# ip dhcp pool College-Pool
>> Router(dhcp-config)# network 192.168.1.0 255.255.255.0
>> Router(dhcp-config)# default-router 192.168.1.1
>> Router(dhcp-config)# dns-server 8.8.8.8
```

Here,

- `ip dhcp pool College-Pool`:
  - Description: Enters DHCP pool configuration mode and names the DHCP pool "College-Pool."

- `network 192.168.1.0 255.255.255.0`:
  - Description: Specifies the network and subnet mask for the DHCP pool.

- `default-router 192.168.1.1`:
  - Description: Sets the default gateway (router) for clients in the DHCP pool.

- `dns-server 8.8.8.8`:
  - Description: Specifies the DNS server(s) for the DHCP clients.

## `DO WR`

- `do write memory` or `do wr`:
  - Description: Saves the running configuration to the startup configuration file.

Note:
When you enter this command, the switch or router will save the current running configuration to the startup configuration file. The phrase "Building configuration..." will be displayed as output to indicate that the configuration is being saved. This ensures that the changes made in the running configuration are preserved across reboots.

