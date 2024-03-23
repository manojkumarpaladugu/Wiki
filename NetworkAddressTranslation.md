## NAT (Network Address Translation)
* NAT stands for Network Address Translation
* It is a service used in routers
* It translates local IP addresses into public IP addresses and vice versa
  * Router uses public IP address to communicate with internet
  * Whereas several devices connected to that router have assigned with local IP addresses. Whenever these devices wants to communicate with internet, router translates local IP addresses into public IP addresses and vice versa
* When device shoots a packet to the internet, the router's NAT service modifies only source IP address from local to public in packet's L3 header

## PAT (Port Address Translation)
* PAT is part of NAT service
* In this many local IP addresses can be translated to a single registered public address. That is achieved by using port numbers
* Port numbers are used to distinguish the traffic that belongs to which IP address
* This is very useful in case many users connected to the internet using only one registered public address
* When device shoots a packet to the internet, the router's PAT service modifies both,
  * source IP address from local to public in packet's L3 header
  * source port number in packet's L4 header

## Why NAT
* There are limited public IPv4 address registered in the world than the number of devices. NAT helps preserving them

## NAT Terms
* Static:
  * Explicit mapping between PRE-translation and POST-translation
  * For example translate 192.168.0.10 to 72.12.78.2
    * That means, when device shoots a packet to the internet, router's NAT service replaces specific local IP address (192.168.0.10) to specific public IP address (72.12.78.2) and vice versa in the packet
* Dynamic:
  * PRE-translation attributes defined by admin
  * POST-translation attributes selected by translation device
  * For example, translate anything in the range 192.168.6.0/24 to 72.12.78.2, 72.12.78.3, 72.12.78.4
    * That means, when a device shoots a packet to the internet, router's NAT service replaces any local IP address in the range 192.168.6.0/24 with any of the public IP addresses (72.12.78.2, 72.12.78.3, 72.12.78.4)

## Types of NAT
* Static NAT
* Static PAT
* Dynamic NAT
* Dynamic PAT