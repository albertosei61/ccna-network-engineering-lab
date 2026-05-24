========================

NETWORK vs BROADCAST ADDRESS NOTES

========================

Router commands
R1#show ip interface brief

Interface Ip-Address Ok? Method Status Protocol

To configure interface use int or interface g0/1 or full interface name

assign ip with ip address or ip add IP subnet mask


Show interfaces description

R1# show interfaces description

R1(config)#int g0/0

R1(config-if)#description ## to SW1 ##

do sh int desc should show the description message



\------------------------

HOW IPv4 ADDRESSES WORK

\------------------------



IPv4 addresses are split into:

\- Network portion

\- Host portion



The subnet mask determines which bits belong to:

\- Network

\- Hosts



Example:

192.168.1.0/24



/24 means:

\- First 24 bits = network bits

\- Last 8 bits = host bits





\------------------------

NETWORK ADDRESS

\------------------------



Definition:

\- The address that identifies the subnet itself

\- Host bits are ALL 0s



Meaning:

“This network”



Example:

192.168.1.0/24



Binary:

11000000.10101000.00000001.00000000



Host bits:

00000000



Because all host bits are 0:

\- This becomes the NETWORK address





\------------------------

WHY ALL 0s = NETWORK ADDRESS

\------------------------



The host portion represents devices.



If host bits are all 0:

\- No individual host is selected

\- It represents the base subnet itself



Think of it as:

\- The identity of the network

\- The starting address of the subnet





\------------------------

USES OF THE NETWORK ADDRESS

\------------------------



1\. Routing

Routers store network routes, not every host.



Example:

192.168.1.0/24 → Interface G0/1



Meaning:

“Any traffic for this network goes here.”



2\. Network Identification

Defines which devices belong to the same subnet.



3\. Subnetting

Used when designing and organizing networks.





\------------------------

BROADCAST ADDRESS

\------------------------



Definition:

\- Address used to communicate with ALL hosts in a subnet

\- Host bits are ALL 1s



Meaning:

“Everyone on this network”



Example:

192.168.1.255



Binary:

11000000.10101000.00000001.11111111



Host bits:

11111111



Because all host bits are 1:

\- This becomes the BROADCAST address





\------------------------

WHY ALL 1s = BROADCAST ADDRESS

\------------------------



Host bits represent all possible hosts.



If all host bits are 1:

\- Every host position is included

\- The address represents ALL hosts in the subnet



Think of it as:

\- Sending traffic to everyone at once





\------------------------

USABLE HOST RANGE

\------------------------



Example subnet:

192.168.1.0/24



Network Address:

192.168.1.0



Broadcast Address:

192.168.1.255



Usable Hosts:

192.168.1.1 – 192.168.1.254





\------------------------

HOST BIT RANGE

\------------------------



All 0s:

00000000

= Network Address



First usable:

00000001

= First Host



Last usable:

11111110

= Last Host



All 1s:

11111111

= Broadcast Address





\------------------------

USES OF BROADCAST ADDRESS

\------------------------



1\. DHCP Discovery

A device without an IP broadcasts:

“Is there a DHCP server?”



2\. ARP Requests

Used to discover MAC addresses.



Example:

“Who has 192.168.1.10?”



3\. Network Announcements

Used for service discovery and some routing protocols.





\------------------------

WHY HOSTS CANNOT USE THESE

\------------------------



Network Address:

\- Represents the subnet itself

\- Not an individual device



Broadcast Address:

\- Represents all devices in subnet

\- Used for network-wide communication



Assigning either to a host would cause network confusion.





\------------------------

KEY RULES

\------------------------



All host bits = 0

→ Network Address

→ “This network”



All host bits = 1

→ Broadcast Address

→ “Everyone on this network”





\------------------------

IMPORTANT CONCEPT

\------------------------



Subnetting works by:

\- Keeping network bits fixed

\- Allowing host bits to vary



Lowest host value:

00000000

= Network Address



Highest host value:

11111111

= Broadcast Address





\------------------------

SIMPLE ANALOGY

\------------------------



Think of a hotel:



Network Address:

\- The hotel building itself



Host Addresses:

\- Individual rooms



Broadcast Address:

\- Announcement sent to every room







