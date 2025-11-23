LAB 01 BASIC DEVICE CONFIGURATION and CLI NAVIGATION


OBJECTIVES:

1. Navigate the Cisco IOS CLI (User EXEC, Privileged EXEC, Global Config)
2. Configure hostname and banner messages
3. Configure enable secret and console/VTY passwords
4. Configure IP addresses on router GigabitEthernet interfaces
5. Save configuration to NVRAM
6. Use basic show commands for verification

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


STUDENT INSTRUCTIONS
================================================================================

PART 1: CLI NAVIGATION
----------------------------------
1. Connect to R1 via console cable
2. Enter User EXEC mode - note the prompt symbol
3. Enter Privileged EXEC mode - what command is used? Note the new prompt
4. Enter Global Configuration mode - what command is used? Note the new prompt
5. Enter Interface Configuration mode for G0/0
6. Return to Privileged EXEC mode using the "end" command
7. Use the "?" to explore available commands at each level

PART 2: CONFIGURE R1
---------------------------------
1. Configure the hostname as "R1"
2. Configure a message-of-the-day banner with the text:
   "Authorized Access Only! Disconnect Immediately if Unauthorized!"
3. Configure an enable secret password: "class"
4. Configure console line 0:
   - Password: "cisco"
   - Require login
   - Enable logging synchronous
5. Configure VTY lines 0-4:
   - Password: "cisco"
   - Require login
6. Configure interface GigabitEthernet0/0:
   - IP address: 192.168.10.1/24
   - Description: "LAN Connection to SW1"
   - Enable the interface
7. Configure interface GigabitEthernet0/1:
   - IP address: 10.0.0.1/30
   - Description: "WAN Link to R2"
   - Enable the interface
8. Configure a static route to reach the 192.168.20.0/24 network via 10.0.0.2
9. Save the configuration to NVRAM

PART 3: CONFIGURE R2
---------------------------------
1. Configure the hostname as "R2"
2. Configure a message-of-the-day banner with the same text as R1
3. Configure an enable secret password: "class"
4. Configure console line with password "cisco" and login required
5. Configure VTY lines 0-4 with password "cisco" and login required
6. Configure interface GigabitEthernet0/0:
   - IP address: 192.168.20.1/24
   - Description: "LAN Connection to SW2"
   - Enable the interface
7. Configure interface GigabitEthernet0/1:
   - IP address: 10.0.0.2/30
   - Description: "WAN Link to R1"
   - Enable the interface
8. Configure a static route to reach the 192.168.10.0/24 network via 10.0.0.1
9. Save the configuration to NVRAM

PART 4: CONFIGURE SWITCHES
---------------------------------------
On SW1:
1. Configure hostname as "SW1"
2. Configure enable secret: "class"
3. Configure console password: "cisco" with login
4. Configure VTY password: "cisco" with login
5. Configure VLAN 1 interface with IP 192.168.10.2/24
6. Configure default gateway: 192.168.10.1
7. Save configuration

On SW2:
1. Configure hostname as "SW2"
2. Configure enable secret: "class"
3. Configure console password: "cisco" with login
4. Configure VTY password: "cisco" with login
5. Configure VLAN 1 interface with IP 192.168.20.2/24
6. Configure default gateway: 192.168.20.1
7. Save configuration

PART 5: VERIFICATION
---------------------------------
1. On R1, use "show ip interface brief" to verify interface status
2. On R1, use "show running-config" to verify your configuration
3. On R1, verify the routing table shows a route to 192.168.20.0/24
4. From R1, ping R2's G0/1 interface (10.0.0.2)
5. From R1, ping R2's G0/0 interface (192.168.20.1)
6. From R1, ping PC3 (192.168.20.10)
7. From PC1, ping PC3 and PC4
8. Telnet from R1 to R2 (10.0.0.2) - verify VTY password works
