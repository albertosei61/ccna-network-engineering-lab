Ethernet Frame -  Data Link Layer 2
- Eth. header + Packet (L3 header, L4 header, Data) + Eth. trailer
- Unicast frame: a frame destined for a single target
- Multicast frame: a frame destined for multiple targets
- Unknown unicast frame - Ethernet frame sent to one specific MAC address, but the switch does not yet know which port that MAC address is on in a Cisco network.
- Unkown unicast flooding = sends ethernet frame through all it's interfaces except incoming port. 
    When the destination device replies back then the switch learns and it establishes a known unicast for future transmissions.
- Dynamic MAC addresses are removed from the MAC address table after 5 minutes of inactivity.


Eth. header
- Preamble = 7 bytes (56 bits) Alternating 1's and 0's.
    10101010 * 7 
    Allows devices to synchronize thier receiver clocks 

- SFD = Start frame delimiter
    Length: 1 byte (8 bits)
    10101011
    Marks the end of the preamble, and the beginning of the rest of the frame.

- Destination and Source field
    Indicate the devices sending and receiving the frame
    Consist of the destination and source 'MAC (Media Access Control) address'
    6 byte (48 bit) address of the physical device. 
    
- Type
    2 byte (16 bit) field 
    Can be used to represent the type of length of the encapsulated packet (in bytes)
    
    - EtherType (Modern Ethernet – Ethernet II)

        If the value is ≥ 0x0600 (1536), the field represents the protocol type of the payload.

        Common EtherTypes:

        0x0800 (2048 decimal) → IPv4
        0x86DD (34525) → IPv6
        0x0806 → ARP
        Purpose: Tells the device what Layer 3 protocol is inside the frame.

    - Length (IEEE 802.3 Ethernet – Older standard)

        If the value is ≤ 1500, the field represents the length of the payload in bytes.
        Purpose: Tells the device how many bytes of data are in the frame.
    


Eth. Trailer
- FCS = Frame check sequence
    4 bytes (32 bits) in length
    Detects corrupted data by running a 'CRC' (Cyclic Redundancy Check)  algorithm over the received data

MAC Address AKA 'Burned in Address'
- 6 byte (48 bit) physical address assigned to the device when it is made
- globally unique
- first 3 bytes are the OUI (organizationaly Unique Identifier), which is assigned to the company making the device
- Last 3 bytes are unique to the device itself
- Written as 12 hexidecimal characters.
- Switches will keep a dynamic mac address of the source address when it receives a packet in its MAC Address table.

    
