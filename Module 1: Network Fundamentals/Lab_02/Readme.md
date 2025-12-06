LAB 02: IPv4 ADDRESSING AND SUBNETTING

EXAM TOPICS COVERED:
- 1.6 Configure and verify IPv4 addressing and subnetting
- 1.7 Describe the need for private IPv4 addressing
- 1.10 Verify IP parameters for Client OS (Windows, Mac OS, Linux)

OBJECTIVES:
-----------
1. Configure IPv4 addresses on router GigabitEthernet interfaces
2. Understand subnet masks and their CIDR notation (/24, /30)
3. Configure default gateways on end devices
4. Verify connectivity between different subnets
5. Interpret IP addressing information from show commands
6. Understand the purpose of /30 subnets for point-to-point links

TOPOLOGY:
---------
Refer to Lab02_Topology.pdf for the visual diagram.

Network Design:
- 3 routers in a triangle topology
- Each router has a LAN segment with 2 PCs
- Router-to-router links use /30 subnets to conserve addresses

EQUIPMENT REQUIRED:
-------------------
- 3 x Cisco 2911 Routers
- 3 x Cisco 2960-24TT Switches
- 6 x PCs
- Straight-through Ethernet cables
- Crossover cables

  IP ADDRESSING TABLE:
--------------------
Device    Interface    IP Address        Subnet Mask       Gateway
------    ---------    ----------        -----------       -------
R1        G0/0         192.168.1.1       255.255.255.0     -
R1        G0/1         10.0.12.1         255.255.255.252   -
R1        G0/2         10.0.13.1         255.255.255.252   -
R2        G0/0         192.168.2.1       255.255.255.0     -
R2        G0/1         10.0.12.2         255.255.255.252   -
R2        G0/2         10.0.23.1         255.255.255.252   -
R3        G0/0         192.168.3.1       255.255.255.0     -
R3        G0/1         10.0.13.2         255.255.255.252   -
R3        G0/2         10.0.23.2         255.255.255.252   -
SW1       VLAN1        192.168.1.2       255.255.255.0     192.168.1.1
SW2       VLAN1        192.168.2.2       255.255.255.0     192.168.2.1
SW3       VLAN1        192.168.3.2       255.255.255.0     192.168.3.1
PC1       NIC          192.168.1.10      255.255.255.0     192.168.1.1
PC2       NIC          192.168.1.20      255.255.255.0     192.168.1.1
PC3       NIC          192.168.2.10      255.255.255.0     192.168.2.1
PC4       NIC          192.168.2.20      255.255.255.0     192.168.2.1
PC5       NIC          192.168.3.10      255.255.255.0     192.168.3.1
PC6       NIC          192.168.3.20      255.255.255.0     192.168.3.1

SUBNET SUMMARY:
---------------
Network          Purpose                    Usable Range           Broadcast
-------          -------                    ------------           ---------
192.168.1.0/24   R1 LAN (Headquarters)      192.168.1.1-254        192.168.1.255
192.168.2.0/24   R2 LAN (Branch 2)          192.168.2.1-254        192.168.2.255
192.168.3.0/24   R3 LAN (Branch 3)          192.168.3.1-254        192.168.3.255
10.0.12.0/30     R1-R2 Link                 10.0.12.1-2            10.0.12.3
10.0.13.0/30     R1-R3 Link                 10.0.13.1-2            10.0.13.3
10.0.23.0/30     R2-R3 Link                 10.0.23.1-2            10.0.23.3

CABLING TABLE:
--------------
Connection        Cable Type          Ports
----------        ----------          -----
R1 to SW1         Straight-through    R1 G0/0 to SW1 G0/1
R2 to SW2         Straight-through    R2 G0/0 to SW2 G0/1
R3 to SW3         Straight-through    R3 G0/0 to SW3 G0/1
R1 to R2          Crossover           R1 G0/1 to R2 G0/1
R1 to R3          Crossover           R1 G0/2 to R3 G0/1
R2 to R3          Crossover           R2 G0/2 to R3 G0/2
PC1 to SW1        Straight-through    PC1 NIC to SW1 Fa0/1
PC2 to SW1        Straight-through    PC2 NIC to SW1 Fa0/2
PC3 to SW2        Straight-through    PC3 NIC to SW2 Fa0/1
PC4 to SW2        Straight-through    PC4 NIC to SW2 Fa0/2
PC5 to SW3        Straight-through    PC5 NIC to SW3 Fa0/1
PC6 to SW3        Straight-through    PC6 NIC to SW3 Fa0/2
