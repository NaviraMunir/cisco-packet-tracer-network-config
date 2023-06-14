# cisco-packet-tracer-network-config
This project, implemented in Cisco Packet Tracer, demonstrates the configuration of a network using various routing protocols and network services. The network topology consists of multiple blocks, each utilizing different routing protocols and network configurations.

# Block Configurations

**First Block:**
Routing Protocol: EIGRP
Area: N/A
DHCP Server: Provides IP addresses to hosts in EIGRP block.

**Second Block:**
Routing Protocol: OSPF (Area 1)
Area: 1
DHCP Server: Provides IP addresses to hosts in OSPF Area 1.

**Third Block:**
Routing Protocol: RIP
Area: N/A
DHCP Server: Provides IP addresses to hosts in RIP block.

**Last Block:**
Routing Protocol: OSPF (Area 0)
Area: 0
DHCP Server: Provides IP addresses to hosts in OSPF Area 0 (Web Server block).

# Redistribution
Router6 and Router13 perform redistribution to connect EIGRP with OSPF and OSPF with RIP.
Router11 performs redistribution to connect OSPF Area 1 with OSPF Area 0.

# IP Address Assignment
Hosts in EIGRP, OSPF Area 1, and RIP blocks receive IP addresses from the "DHCP Server" in the first block.
Hosts in OSPF Area 0 (Web Server block) receive IP addresses from the "DHCP Server" within their own block.

# VLSM
Variable Length Subnet Masking (VLSM) is used in each network of the topology to optimize IP address allocation.

# Access Control
One PC in Network L is not allowed to access the TFTP server.
One PC in Network E is not allowed to access the Data server in the first block.
All hosts connected in Network A are not allowed to access the "Web Server".

# Servers
The TFTP and Data servers do not require running services; they are treated as hosts.
Access to these servers from respective networks is blocked using Access Control Lists.
