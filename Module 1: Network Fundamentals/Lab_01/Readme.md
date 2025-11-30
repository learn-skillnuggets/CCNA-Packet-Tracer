CCNA 200-301 | Module 1: Network Fundamentals
================================================================================

EXAM TOPICS COVERED:
- 1.1 Explain the role and function of network components
- 5.3 Configure device access control using local passwords

OBJECTIVES:
-----------
1. Navigate the Cisco IOS CLI (User EXEC, Privileged EXEC, Global Config)
2. Configure hostname and banner messages
3. Configure enable secret and console/VTY passwords
4. Configure IP addresses on router GigabitEthernet interfaces
5. Save configuration to NVRAM
6. Use basic show commands for verification

TOPOLOGY:
---------
Refer to Lab01_Topology.pdf for the visual diagram.

EQUIPMENT REQUIRED:
-------------------
- 2 x Cisco 2911 Routers
- 2 x Cisco 2960-24TT Switches
- 4 x PCs
- Straight-through Ethernet cables
- Crossover cable (for router-to-router connection, or use switch)

IP ADDRESSING TABLE:
--------------------
Device    Interface    IP Address        Subnet Mask       Gateway
------    ---------    ----------        -----------       -------
R1        G0/0         192.168.10.1      255.255.255.0     -
R1        G0/1         10.0.0.1          255.255.255.252   -
R2        G0/0         192.168.20.1      255.255.255.0     -
R2        G0/1         10.0.0.2          255.255.255.252   -
SW1       VLAN1        192.168.10.2      255.255.255.0     192.168.10.1
SW2       VLAN1        192.168.20.2      255.255.255.0     192.168.20.1
PC1       NIC          192.168.10.10     255.255.255.0     192.168.10.1
PC2       NIC          192.168.10.20     255.255.255.0     192.168.10.1
PC3       NIC          192.168.20.10     255.255.255.0     192.168.20.1
PC4       NIC          192.168.20.20     255.255.255.0     192.168.20.1

CABLING TABLE:
--------------
Connection                    Cable Type          Ports
----------                    ----------          -----
R1 to SW1                     Straight-through    R1 G0/0 to SW1 G0/1
R2 to SW2                     Straight-through    R2 G0/0 to SW2 G0/1
R1 to R2                      Crossover           R1 G0/1 to R2 G0/1
PC1 to SW1                    Straight-through    PC1 NIC to SW1 Fa0/1
PC2 to SW1                    Straight-through    PC2 NIC to SW1 Fa0/2
PC3 to SW2                    Straight-through    PC3 NIC to SW2 Fa0/1
PC4 to SW2                    Straight-through    PC4 NIC to SW2 Fa0/2
