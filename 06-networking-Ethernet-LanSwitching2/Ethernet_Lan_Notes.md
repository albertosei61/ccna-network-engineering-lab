Ethernet Frame
Ethernet header = Preamble + SFD + Destination + Source + Type
- The Preamble + SFD is usally not cosidered part of the Ethernet header
- Therefore the size of the Ethernet header + trailer is 18 bytes (6 + 6 + 2 + 4)
- The mininum size for an Ethernet frame ( Header + Payload [packet] + Trailer )_ is 64 bytes.
- 64 bytes - 18 bytes ( header + trailer size ) = 46 bytes
- Therefore the mininum payload (packet) size is 46 bytes
- If the payload is less than 46 bytes, padding bytes are added.

ARP ( Address Resolution Protocol)
- used to discover the layer 2 address MAC address of a known layer 3 address (ip address)
- consists of two messages: 
    ARP Request from source device
    ARP Reply from destination device
-  ARP Request is broadcast = sent to all hosts on the network 
- ARP Reply is unicast = sent only to one host (the host that sent the request)
- FFFF.FFFF.FFFF broadcast address
- How to view ARP table
    Use arp -a to view the ARP table (Windows, macOS, Linux)
    Internet address = IP address ( Layer 3 address)
    Physical address = MAC address ( Layer 2 address)
    Type static = default entry
    Type dynamic = learned via ARP
Ping 
- A network utility that is used to test reachability
- Measures round trip time
- Uses two messages:
    ICMP Echo Request
    ICMP Echo Reply
ICMP (Internet Control Message Protocol ) is a network layer protocol used primarily for error reporting and diagnostic functions in IP networks.

MAC Address Table
- commands on cisco switch:
    show mac address-table
    clear mac address-table dynamic address mac-address
    clear mac address-table dynamic interfacce interface-id
