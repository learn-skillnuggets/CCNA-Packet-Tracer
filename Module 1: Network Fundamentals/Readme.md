# Module 1: Network Fundamentals

CCNA 200-301 Hands-On Labs with Cisco Packet Tracer
Labs 01-06 | Beginner to Intermediate

================================================================================

OVERVIEW

This module provides comprehensive hands-on practice for the Network Fundamentals domain of the CCNA 200-301 certification exam. These labs are designed for students who have already studied the theory and need practical experience applying their knowledge in realistic network scenarios.

What makes these labs different:

- Ready-to-use Packet Tracer files - No need to build topologies from scratch
- Pre-configured initial states - Jump straight into configuration tasks
- Complete answer keys - Full device configurations provided
- Video walkthroughs - Watch and learn as you build
- Professional documentation - Clear instructions and verification steps
- Time-saving - 70-80% faster than building labs from zero

================================================================================

WHO ARE THESE LABS FOR?

These labs are designed for:

- CCNA students who need hands-on practice
- Network engineers preparing for the CCNA 200-301 exam
- Students enrolled in CCNA theory courses who need practical exercises
- Self-learners who want structured, professional-grade labs
- Anyone who wants to build real-world Cisco configuration skills

NOTE: These labs focus on practical application, not theory instruction. Students should have basic understanding of networking concepts before attempting these exercises.

================================================================================

MODULE CONTENTS

This module contains 6 hands-on labs covering the Network Fundamentals domain (20% of CCNA exam):

--------------------------------------------------------------------------------
Lab 01: Basic Device Configuration and CLI Navigation
--------------------------------------------------------------------------------
Difficulty: Beginner
Estimated Time: 45-60 minutes

Exam Topics Covered:
- 1.1 Explain the role and function of network components
- 5.3 Configure device access control using local passwords

What You Will Learn:
- Navigate the Cisco IOS CLI (User EXEC, Privileged EXEC, Global Config modes)
- Configure hostname and banner messages
- Configure enable secret and console/VTY line passwords
- Create local user accounts with privilege levels
- Configure IP addresses on router GigabitEthernet interfaces
- Configure static routes for basic inter-network connectivity
- Save configuration to NVRAM
- Use basic show commands for verification

Equipment Used:
- 2 x Cisco 2911 Routers
- 2 x Cisco 2960-24TT Switches
- 4 x PCs

Files Provided:
- Lab01_Initial.pka (starting topology)
- Lab01_Guide.pdf (student instructions)
- Lab01_Topology.pdf (network diagram)
- Lab01_Final_Configs.txt (answer key)
- Video walkthrough (YouTube)

--------------------------------------------------------------------------------
Lab 02: IPv4 Addressing and Subnetting
--------------------------------------------------------------------------------
Difficulty: Beginner
Estimated Time: 50-70 minutes

Exam Topics Covered:
- 1.6 Configure and verify IPv4 addressing and subnetting
- 1.7 Describe the need for private IPv4 addressing
- 1.10 Verify IP parameters for Client OS (Windows, Mac OS, Linux)

What You Will Learn:
- Configure IPv4 addresses on router GigabitEthernet interfaces
- Understand subnet masks and CIDR notation (/24, /30)
- Configure default gateways on end devices
- Understand the purpose of /30 subnets for point-to-point WAN links
- Configure static routes in a multi-router topology
- Verify connectivity between different subnets
- Interpret IP addressing information from show commands
- Use ipconfig/ifconfig on client operating systems

Equipment Used:
- 3 x Cisco 2911 Routers
- 3 x Cisco 2960-24TT Switches
- 6 x PCs

Topology:
- Triangle router topology with full mesh connectivity
- Each router has its own LAN segment
- WAN links use efficient /30 subnetting

Files Provided:
- Lab02_Initial.pka
- Lab02_Guide.pdf
- Lab02_Topology.pdf
- Lab02_Final_Configs.txt
- Video walkthrough (YouTube)

--------------------------------------------------------------------------------
Lab 03: IPv4 Subnetting Practice (VLSM)
--------------------------------------------------------------------------------
Difficulty: Intermediate
Estimated Time: 60-90 minutes

Exam Topics Covered:
- 1.6 Configure and verify IPv4 addressing and subnetting
- 3.3 Configure and verify IPv4 and IPv6 static routing

What You Will Learn:
- Design an IP addressing scheme using Variable Length Subnet Masking (VLSM)
- Calculate subnet addresses, broadcast addresses, and usable host ranges
- Apply VLSM subnetting to efficiently allocate IP addresses
- Determine appropriate subnet sizes based on host requirements
- Configure routers and switches with the calculated addressing scheme
- Configure static routes to enable full connectivity
- Verify connectivity across all subnets

Equipment Used:
- 3 x Cisco 2911 Routers (HQ, Branch1, Branch2)
- 4 x Cisco 2960-24TT Switches
- 8 x PCs (distributed across LANs)

Challenge:
Students must subnet the 172.16.0.0/16 network to accommodate:
- HQ LAN: 60 hosts
- Branch1 LAN-A: 30 hosts
- Branch1 LAN-B: 14 hosts
- Branch2 LAN: 6 hosts
- 2 x Point-to-point WAN links

Files Provided:
- Lab03_Initial.pka
- Lab03_Guide.pdf (includes subnetting worksheet)
- Lab03_Topology.pdf
- Lab03_Final_Configs.txt
- Lab03_Subnetting_Solutions.pdf
- Video walkthrough (YouTube)

--------------------------------------------------------------------------------
Lab 04: IPv6 Addressing Basics
--------------------------------------------------------------------------------
Difficulty: Intermediate
Estimated Time: 60-80 minutes

Exam Topics Covered:
- 1.8 Configure and verify IPv6 addressing and prefix
- 1.9 Describe IPv6 address types (GUA, ULA, link-local, unique local)

What You Will Learn:
- Configure IPv6 global unicast addresses (GUA) on router interfaces
- Understand and identify link-local addresses (FE80::/10)
- Understand EUI-64 addressing
- Configure IPv6 on end devices
- Enable IPv6 routing on Cisco routers (ipv6 unicast-routing)
- Configure IPv6 static routes
- Verify IPv6 connectivity using ping and show commands
- Implement dual-stack configuration (IPv4 and IPv6 simultaneously)
- View and understand the IPv6 neighbour table

Equipment Used:
- 2 x Cisco 2911 Routers
- 2 x Cisco 2960-24TT Switches
- 4 x PCs

Key Concepts:
- Dual-stack operation (both IPv4 and IPv6)
- IPv6 address compression and expansion
- Link-local vs Global Unicast addresses
- IPv6 prefix notation

Files Provided:
- Lab04_Initial.pka
- Lab04_Guide.pdf
- Lab04_Topology.pdf
- Lab04_Final_Configs.txt
- Video walkthrough (YouTube)

--------------------------------------------------------------------------------
Lab 05: Cable Types and Interface Verification
--------------------------------------------------------------------------------
Difficulty: Beginner
Estimated Time: 50-70 minutes

Exam Topics Covered:
- 1.3 Compare physical interface and cabling types
- 1.4 Identify interface and cable issues (collisions, errors, duplex/speed mismatch)

What You Will Learn:
- Identify correct cable types for different device connections
- Understand straight-through vs crossover cable usage
- Understand fiber optic cable types (single-mode vs multi-mode)
- Configure and verify interface speed and duplex settings
- Troubleshoot Layer 1 connectivity issues (duplex mismatch scenarios)
- Use show commands to verify interface status and statistics
- Understand Auto-MDIX functionality
- Identify and interpret interface error counters

Equipment Used:
- 2 x Cisco 2960-24TT Switches
- 2 x Cisco 2911 Routers
- 3 x PCs
- 1 x Server

Practical Exercises:
- Cable type identification for entire topology
- Intentional duplex mismatch troubleshooting
- Interface statistics analysis
- Error counter interpretation

Files Provided:
- Lab05_Initial.pka
- Lab05_Guide.pdf
- Lab05_Topology.pdf
- Lab05_Cable_Reference.pdf
- Lab05_Final_Configs.txt
- Video walkthrough (YouTube)

--------------------------------------------------------------------------------
Lab 06: TCP/UDP and Basic Connectivity Testing
--------------------------------------------------------------------------------
Difficulty: Beginner
Estimated Time: 40-60 minutes

Exam Topics Covered:
- 1.5 Compare TCP to UDP

What You Will Learn:
- Understand the difference between TCP and UDP protocols
- Identify common port numbers for network services
- Use ping to test Layer 3 (ICMP) connectivity
- Use traceroute to identify the path packets take through the network
- Test application layer connectivity using Telnet to specific ports
- Use Packet Tracer simulation mode to analyze packet flow
- Understand the TCP three-way handshake process
- Analyse protocol behaviour in Packet Tracer PDU mode

Equipment Used:
- 2 x Cisco 2911 Routers
- 2 x Cisco 2960-24TT Switches
- 4 x PCs
- 1 x Server

Key Protocols Covered:
- TCP (Connection-oriented, reliable)
- UDP (Connectionless, best-effort)
- ICMP (ping, traceroute)
- Common ports: HTTP (80), HTTPS (443), SSH (22), Telnet (23), DNS (53)

Files Provided:
- Lab06_Initial.pka
- Lab06_Guide.pdf
- Lab06_Topology.pdf
- Lab06_Protocol_Reference.pdf
- Lab06_Final_Configs.txt
- Video walkthrough (YouTube)

================================================================================

HOW TO USE THESE LABS

1. Download the Lab##_Initial.pka file from this repository
2. Open the file in Cisco Packet Tracer
3. Download and review the Lab##_Guide.pdf for instructions
4. Follow the step-by-step tasks in the guide
5. Use show commands to verify your configuration
6. Compare your configuration to Lab##_Final_Configs.txt if needed
7. Watch the video walkthrough for detailed explanation

Each lab includes:
- Initial Packet Tracer file with basic setup
- Comprehensive student instruction guide
- Network topology diagram
- Complete final configurations (answer key)
- Video walkthrough on YouTube

================================================================================

PREREQUISITES

Before starting these labs, students should:

- Have basic understanding of networking concepts (OSI model, IP addressing basics)
- Have Cisco Packet Tracer installed (available free via Cisco NetAcad)
- Have completed a CCNA theory course or equivalent study
- Understand basic subnetting concepts (for Labs 02-03)
- Be familiar with command-line interfaces

Recommended CCNA Study Resources:
- Official Cert Guide (Wendell Odom)
- CCNA 200-301 Official Cert Guide Library
- Cisco NetAcad CCNA course
- CBT Nuggets CCNA training
- Any accredited CCNA training provider

================================================================================

EQUIPMENT SPECIFICATIONS

All labs use modern Cisco equipment specifications:

Routers:
- Cisco 2911 Integrated Services Router
- 3 x GigabitEthernet interfaces (G0/0, G0/1, G0/2)
- No legacy FastEthernet or Serial interfaces

Switches:
- Cisco 2960-24TT
- 24 x FastEthernet ports (Fa0/1-24)
- 2 x GigabitEthernet uplink ports (G0/1-2)

This ensures students learn on current equipment specifications rather than outdated legacy hardware.

================================================================================

LEARNING PATH

Recommended order for completing Module 1 labs:

Week 1:
- Lab 01: Basic Device Configuration (Foundation)
- Lab 02: IPv4 Addressing (Build on Lab 01)

Week 2:
- Lab 05: Cables and Interfaces (Physical layer understanding)
- Lab 06: TCP/UDP Connectivity (Transport layer concepts)

Week 3:
- Lab 03: VLSM Subnetting (Advanced addressing)
- Lab 04: IPv6 Basics (Modern IP addressing)

Total estimated time for Module 1: 12-16 hours

================================================================================

ASSESSMENT AND VERIFICATION

Each lab includes:

1. Step-by-step configuration tasks
2. Verification commands to check your work
3. Assessment questions to test understanding
4. Final configuration files to compare against

Students should achieve 100% connectivity before moving to the next lab.

Key verification commands used throughout:
- show running-config
- show ip interface brief
- show ipv6 interface brief
- show ip route
- show ipv6 route
- show interfaces
- show interfaces status
- ping
- traceroute

================================================================================

EXAM COVERAGE

This module covers the following CCNA 200-301 exam topics:

Domain 1: Network Fundamentals (20% of exam)
- 1.1 Explain the role and function of network components
- 1.3 Compare physical interface and cabling types
- 1.4 Identify interface and cable issues
- 1.5 Compare TCP to UDP
- 1.6 Configure and verify IPv4 addressing and subnetting
- 1.7 Describe the need for private IPv4 addressing
- 1.8 Configure and verify IPv6 addressing and prefix
- 1.9 Describe IPv6 address types
- 1.10 Verify IP parameters for Client OS

Additional coverage:
- 3.3 Configure and verify IPv4 and IPv6 static routing (Lab 03)
- 5.3 Configure device access control using local passwords (Lab 01)

================================================================================

SUPPORT AND RESOURCES

GitHub Repository: https://github.com/learn-skillnuggets/CCNA-Packet-Tracer
YouTube Channel: Skillnuggets (video walkthroughs)
Video Playlist: CCNA 200-301 Hands-On Labs - Module 1

For questions, issues, or suggestions:
- Open an issue on GitHub
- Comment on the YouTube videos
- Check the FAQ in the main repository README

================================================================================

ABOUT THIS PROJECT

These labs are created by an 18-year network engineering veteran to provide professional-grade, practical CCNA training materials. The goal is to give students hands-on experience that saves time while building real-world configuration skills.

This is NOT a complete CCNA course - it is a practical supplement for students who have already studied the theory and need hands-on practice.

All labs are tested and verified in Cisco Packet Tracer. Configurations follow Cisco best practices and current exam objectives.

================================================================================

LICENSE AND USAGE

These lab files are provided for educational purposes. Students are free to:
- Download and use the labs for personal study
- Share the GitHub repository link with other students
- Use these labs as part of study groups

Please do not:
- Re-upload the lab files to other platforms without attribution
- Claim these labs as your own work
- Sell or commercialise these materials

If you find these labs helpful, please:
- Star the GitHub repository
- Subscribe to the Skillnuggets YouTube channel
- Share with other CCNA students

================================================================================

NEXT STEPS

After completing Module 1, continue to:

Module 2: Network Access (Switching) - Labs 07-13
- VLANs, Trunking, STP, EtherChannel, Layer 3 Switching

Module 3: IP Connectivity (Routing) - Labs 14-19
- Static Routing, OSPF, HSRP

Module 4: IP Services - Labs 20-24, 31
- DHCP, NAT, NTP, Syslog, DNS, QoS

Module 5: Security Fundamentals - Labs 25-30
- SSH, ACLs, Port Security, AAA

Module 6: Automation and Programmability - Labs 32-34
- Wireless, Python, REST APIs, JSON

================================================================================

Good luck with your CCNA studies!

Remember: Hands-on practice is essential for both passing the exam and becoming a competent network engineer. These labs provide the practical experience you need.

Last Updated: November 2024
CCNA 200-301 Exam Blueprint Version: Current
