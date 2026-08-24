# Small Business Cisco Network

A small business network designed and implemented in Cisco Packet Tracer.

The network consists of two sites connected through Cisco routers, with separate VLANs for Administration, Staff, and IT. DHCP provides automatic IP addressing, an internal DNS server provides name resolution, static routes connect the two sites, and an extended ACL restricts Staff access to the IT network.

## Network Topology

                         10.0.0.0/30
                  ┌─────────────────────┐
                  │                     │
             ┌────┴────┐           ┌────┴────┐
             │   R1    │           │   R2    │
             │10.0.0.1 │           │10.0.0.2 │
             └────┬────┘           └────┬────┘
                  │                     │
              802.1Q                 802.1Q
               TRUNK                  TRUNK
                  │                     │
             ┌────┴────┐           ┌────┴────┐
             │   SW1   │           │   SW2   │
             └────┬────┘           └────┬────┘
                  │                     │
        ┌─────────┼─────────┐   ┌───────┼─────────┐
        │         │         │   │       │         │
      VLAN 10   VLAN 20   VLAN 30 VLAN 10 VLAN 20 VLAN 30
      ADMIN     STAFF       IT    ADMIN   STAFF    IT
