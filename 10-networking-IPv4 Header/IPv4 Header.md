IPv4 Header
Version Field: 4 bits 
- Identifies the version IPv4 (0100)
- IPv6 (0110)

IHL (Internet Header Length)
- Length: 4 bits
- final field options variable ( indicates the total length of the header)
- In 4 byte increments so if value is 5 then 5*4 bytes = 20bytes
- Minimum value is 5
- Maximum value is 15

DSCP field (Differentiated services code point)
- length: 6 bytes
- Used for quality of service QoS

ECN Field ( Explicit congestion notification 
- length: 2 bits
- Provides end to end notification of network congestion without dropping packets.

Total Length
- Length: 16 bits
- Indicates the total length of the packet (L3 header + L4 segment)
- Measured in bytes
- Minimum value of 20 = this is an ipv3 header with not encapsulated data
- Maximum value of 65,535 ( maximum 16-bit value)

Identification Field 
- length: 16 bits
- packets are fragmented if larger than the MTU (Maximum transmission unit) MTU usually 1500 bytes
- fragmented packets have their own IPv4 header

Flags
- length: 3 bits
- used to control identify fragments
- bit 0: reserved , always set to 0
- bit 1: dont fragment (DF bit), used to indicate a packet that should not be fragmented

IPv4 Packet Structure

Fields of the IPv4 header

OSI Model - PDUs

Data	= Data
Data + L4 header =  Segment
Data + L4 header + L3 header = Packet
L2 trailer + Data + L4 header + L3 header + L2 header = Frame 





































