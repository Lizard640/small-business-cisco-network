# Small Business Cisco Network

A small business network built and configured in Cisco Packet Tracer.

## Network Overview

The network contains two sites connected through two Cisco routers.

Each site contains:

- 1 Cisco 2911 router
- 1 Cisco 2960 switch
- 12 PCs

Site 1 also contains an internal DNS server.

## Topology


                    10.0.0.0/30
                 ┌───────────────┐
                 │               │
              ┌──┴──┐         ┌──┴──┐
              │ R1  │         │ R2  │
              │.0.1 │         │.0.2 │
              └──┬──┘         └──┬──┘
                 │                │
               TRUNK            TRUNK
                 │                │
              ┌──┴──┐         ┌──┴──┐
              │ SW1 │         │ SW2 │
              └──┬──┘         └──┬──┘
                 │                │
           ┌─────┼─────┐    ┌────┼─────┐
          VLAN 10 20 30     VLAN 10 20 30
          ADMIN STAFF IT    ADMIN STAFF IT
          

Site 1
| VLAN | Name  | Network         | Gateway      |
| ---- | ----- | --------------- | ------------ |
| 10   | ADMIN | 192.168.10.0/24 | 192.168.10.1 |
| 20   | STAFF | 192.168.20.0/24 | 192.168.20.1 |
| 30   | IT    | 192.168.30.0/24 | 192.168.30.1 |

Site 2
| VLAN | Name  | Network          | Gateway       |
| ---- | ----- | ---------------- | ------------- |
| 10   | ADMIN | 192.168.110.0/24 | 192.168.110.1 |
| 20   | STAFF | 192.168.120.0/24 | 192.168.120.1 |
| 30   | IT    | 192.168.130.0/24 | 192.168.130.1 |

Features
VLAN segmentation
802.1Q trunking
Inter-VLAN routing
DHCP
DNS
Static routing
Extended ACL
Two-site connectivity
----------

Result:

The completed network successfully demonstrates:

VLAN segmentation
Inter-VLAN communication
DHCP address assignment
DNS configuration
Static routing between sites
Cross-site connectivity
Basic network security
-------

Tools:

Cisco Packet Tracer
Cisco IOS
IPv4
VLANs
DHCP
DNS
Static Routing
ACLs
