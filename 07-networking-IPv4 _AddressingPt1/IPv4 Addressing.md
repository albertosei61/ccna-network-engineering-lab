========================

IPv4 ADDRESSING NOTES

========================



WHAT IS IPv4?

\- Internet Protocol Version 4

\- Layer 3 protocol

\- Used for identifying devices and routing packets

\- 32-bit address

\- Written in decimal format

\- 4 octets separated by periods



Example:

192.168.1.10



Binary:

11000000.10101000.00000001.00001010





\------------------------

IPv4 STRUCTURE

\------------------------



\[ Network Portion ] \[ Host Portion ]



\- Network portion identifies the network

\- Host portion identifies the device



Example:

IP Address: 192.168.1.10

Subnet Mask: 255.255.255.0



Network = 192.168.1

Host = 10





\------------------------

BINARY BASICS

\------------------------



Bit Values:

128 64 32 16 8 4 2 1



Example:

192 = 128 + 64



Binary:

11000000





\------------------------

DECIMAL TO BINARY

\------------------------



88 in binary:



128 64 32 16 8 4 2 1

&#x20;0   1  0  1 1 0 0 0



Result:

01011000



Example IP:

88.46.90.91



Binary:

01011000.00101110.01011010.01011011





\------------------------

IPv4 ADDRESS CLASSES

\------------------------



Class A

\- Range: 1–126

\- Default Mask: 255.0.0.0



Class B

\- Range: 128–191

\- Default Mask: 255.255.0.0



Class C

\- Range: 192–223

\- Default Mask: 255.255.255.0



Class D

\- Range: 224–239

\- Multicast



Class E

\- Range: 240–255

\- Experimental





\------------------------

PRIVATE IPv4 RANGES

\------------------------



Class A:

10.0.0.0 – 10.255.255.255



Class B:

172.16.0.0 – 172.31.255.255



Class C:

192.168.0.0 – 192.168.255.255



\- Not routable on the internet





\------------------------

APIPA

\------------------------



Automatic Private IP Addressing



Range:

169.254.0.0 – 169.254.255.255



Used when:

\- DHCP server unavailable

\- Device cannot obtain IP





\------------------------

LOOPBACK ADDRESS

\------------------------



127.0.0.1



Hostname:

localhost



Purpose:

\- Tests local TCP/IP stack





\------------------------

NETWORK vs BROADCAST ADDRESS

\------------------------



Network Address:

\- Identifies the network

\- Cannot be assigned to hosts



Example:

192.168.1.0/24



Broadcast Address:

\- Sends traffic to all hosts

\- Cannot be assigned to hosts



Example:

192.168.1.255





\------------------------

USABLE HOST RANGE

\------------------------



Network:

192.168.1.0



Broadcast:

192.168.1.255



Usable Hosts:

192.168.1.1 – 192.168.1.254





\------------------------

SUBNET MASKS

\------------------------



/8  = 255.0.0.0

/16 = 255.255.0.0

/24 = 255.255.255.0

/25 = 255.255.255.128

/26 = 255.255.255.192

/27 = 255.255.255.224

/28 = 255.255.255.240

/29 = 255.255.255.248

/30 = 255.255.255.252





\------------------------

CIDR NOTATION

\------------------------



Format:

IP/prefix-length



Example:

192.168.1.10/24



\- /24 means first 24 bits are network bits





\------------------------

HOST CALCULATION

\------------------------



Formula:

2^host\_bits - 2



Subtract 2 for:

\- Network address

\- Broadcast address



Example:

/24



32 - 24 = 8 host bits



2^8 - 2 = 254 hosts





\------------------------

COMMON PREFIXES

\------------------------



/24 = 254 hosts

/25 = 126 hosts

/26 = 62 hosts

/27 = 30 hosts

/28 = 14 hosts

/29 = 6 hosts

/30 = 2 hosts





\------------------------

STATIC vs DYNAMIC IP

\------------------------



Static IP:

\- Manually configured

\- Used for servers, printers, routers



Dynamic IP:

\- Assigned automatically by DHCP





\------------------------

DHCP

\------------------------



Dynamic Host Configuration Protocol



Assigns:

\- IP Address

\- Subnet Mask

\- Default Gateway

\- DNS Server



DORA Process:

1\. Discover

2\. Offer

3\. Request

4\. Acknowledge





\------------------------

DEFAULT GATEWAY

\------------------------



\- Router interface used to reach other networks



Example:

PC = 192.168.1.10

Gateway = 192.168.1.1



Without gateway:

\- Only local communication works





\------------------------

UNICAST / BROADCAST / MULTICAST

\------------------------



Unicast:

\- One-to-one communication



Broadcast:

\- One-to-all communication



Multicast:

\- One-to-many group communication



Multicast Range:

224.0.0.0 – 239.255.255.255





\------------------------

PUBLIC vs PRIVATE IP

\------------------------



Public IP:

\- Routable on internet

\- Assigned by ISP



Private IP:

\- Used internally

\- Requires NAT for internet access





\------------------------

NAT

\------------------------



Network Address Translation



Purpose:

\- Converts private IPs to public IPs

\- Conserves IPv4 addresses





\------------------------

IPv4 LIMITATIONS

\------------------------



\- Limited address space

\- IPv4 exhaustion

\- Heavy NAT usage



Led to:

IPv6





\------------------------

TROUBLESHOOTING COMMANDS

\------------------------



Windows:

ipconfig

ipconfig /all

ping

tracert



Linux/macOS:

ip addr

ifconfig

ping

traceroute

