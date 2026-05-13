IEEE(Institute of Electrical and Electronics Engineers)
- Ethernet (802.3)
- Wi-Fi (802.11)
IETF (Internet Engineering Task Force)
- TCP, IP, UDP, HTTP, DNS

Publishes standards in documents called RFC (Requests for Comments).

IEEE establishes standards for mostly layer 1-2
IETF is for layers 3-7.

Protocols form a network stack
- Application layer: Telnet, FTP, TFTTP etc.
- Transport Layer: TCP, UDP
- Internet Layer: IPv4, IPv6 (Internet Protocol & ICMP)
- Link Layer: Ethernet, Wi-Fi (Local network protocol)

Layer 1: The physical layer
- sends and receives bits as electrical, optical, or radio signals over the medium
- Defines things like cables, connectors, signal levels, and link speeds.
Examples: UTP cables, fiber-optic cables, Wi-Fi radios and antennas, network interface cards

Layer 2: The network layer
- Provides hop to hop delivery of messages on a local network
- A hop is a step along the path between two devices
- from one router or host, to the next router or host in the path
- switches dont count, they just extend the local network
- Uses MAC (Media Access Control) to identify interfaces.
- Protocols at this layer include: Ethernet (IEEE 802.3),Wi-Fi (IEEE 802.11)

Layer 3: The Internet layer
- provides end to end delivery between hosts across multiple networks
- internet = internetwork (between networks)
- Uses IP addresses to identify hosts in the network.
- Protocols at this layer include: IP (IPv4, IPv6), ICMP (Internet Control Message Protocol)

Layer 4: Transport layer
- Provides end to end communication between application processes. Also calleld process to process, or service to service
- Uses port numbers to identify the processes on each host. When the web client on PC1 wants to send a request to the web server running on SRV1, it addresses the message to port 80. 
- Runs mainly on the communicating hosts (client-PC1 and Server-SRV1); routers normally operate based on IP (layer 3), not on transport-layer information.
- Protocols at this layer include: UDP (User Datagram Protocol): simple and efficient
- TCP (Transmission Control Protocol) more robust features beyond basic message addressing.

Layer 5: The Application layer
- Defines how application processes format, send, and interpret data.
- Protocols at this layer define message formats and rules for specific tasks, such as: Browsing web pages (HTTP/HTTPS), Transferring files (FTP, TFTP), Sending/receiving email (SMTP, POP3, IMAP)

Encapsulation
- As the message moves down the stack, each layer encapsulates the data with a header including the information needed for that layer.
- Layer 2 also addes a trailer that the receiving device uses to check for transmision errors.
- The L2 header is transmitted first, and the L2 trailer is transmitted last.

Decapsulation
- The receiving device receives the message as a stream of bits at Layer 1.
- The device examines the information in the Layer 2 header and trailer, and thenn removes them (decapsulation)
- The decapsulation process continues up the stack: Layerr 3 removes the L3 header, then Layer 4 removes the L4 header, and then the data is delivered to the application layer.

Protocol data units or PDU 
- Segment or datagram is a Layer 4 PDU: L4 header + data
TCP creates segments, UDP creates datagrams.
- Packet is a Layer 3 PDU: L3 header + L4 header + data
- frame is a Layer 2 PDU: L2 header + L3 header + L4 header + data + L2 trailer

The contents of each PDU are called the payload
- A segment or datagram's payload is the application data.
- A packet's payload is a segment or datagram.
- A frame's payload is a packet.
