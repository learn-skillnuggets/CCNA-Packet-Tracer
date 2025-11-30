*** R1 FINAL CONFIG ***
-----------------------

hostname R1

no ip domain-lookup

username YouTube secret 5 $1$mERr$ikPvZ8Uh.Sbt9UC87b5Xb.

banner motd #
*************************************************
*  Authorized Access Only!                      *
*  Disconnect Immediately if Unauthorized!      *
*************************************************
#

enable secret class

line console 0
 password cisco
 login
 logging synchronous
 exit

line vty 0 4
 password cisco
 login
 exit

interface GigabitEthernet0/0
 description LAN Connection to SW1
 ip address 192.168.10.1 255.255.255.0
 no shutdown
 exit

interface GigabitEthernet0/1
 description WAN Link to R2
 ip address 10.0.0.1 255.255.255.252
 no shutdown
 exit

ip route 192.168.20.0 255.255.255.0 10.0.0.2

end



*** R2 FINAL CONFIG ***
-----------------------

hostname R2

no ip domain-lookup

username YouTube secret 5 $1$mERr$ikPvZ8Uh.Sbt9UC87b5Xb.

banner motd #
*************************************************
*  Authorized Access Only!                      *
*  Disconnect Immediately if Unauthorized!      *
*************************************************
#

enable secret class

line console 0
 password cisco
 login
 logging synchronous
 exit

line vty 0 4
 password cisco
 login
 exit

interface GigabitEthernet0/0
 description LAN Connection to SW2
 ip address 192.168.20.1 255.255.255.0
 no shutdown
 exit

interface GigabitEthernet0/1
 description WAN Link to R1
 ip address 10.0.0.2 255.255.255.252
 no shutdown
 exit

ip route 192.168.10.0 255.255.255.0 10.0.0.1

end



*** SW1 FINAL CONFIG ***
------------------------

hostname SW1

no ip domain-lookup

username YouTube secret 5 $1$mERr$ikPvZ8Uh.Sbt9UC87b5Xb.

enable secret class

line console 0
 password cisco
 login
 logging synchronous
 exit

line vty 0 4
 password cisco
 login
 exit

interface vlan 1
 ip address 192.168.10.2 255.255.255.0
 no shutdown
 exit

ip default-gateway 192.168.10.1

end



*** SW2 FINAL CONFIG ***
------------------------

hostname SW2

no ip domain-lookup

username YouTube secret 5 $1$mERr$ikPvZ8Uh.Sbt9UC87b5Xb.

enable secret class

line console 0
 password cisco
 login
 logging synchronous
 exit

line vty 0 4
 password cisco
 login
 exit

interface vlan 1
 ip address 192.168.20.2 255.255.255.0
 no shutdown
 exit

ip default-gateway 192.168.20.1

end

