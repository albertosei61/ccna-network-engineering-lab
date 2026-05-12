Network Overview

Built a small enterprise-style topology with two buildings connected over a 3 km WAN link using routers.

LAN Setup

Configured two separate LANs (one per building), each containing:

PCs
Switches
Router interfaces acting as default gateways
WAN Connection

Connected both LANs using a router-to-router WAN link to enable inter-building communication.

Physical Media

Used a multi-node fiber optic cable for the WAN link. Single-mode fiber was not used due to cost considerations and because the 3 km distance was acceptable for the chosen lab setup. Interfaces and Cables

- Understanding ethernet protocols that allow transfer of data
- Speed is measured in bits per second and 8 bits == 1 byte
- Bits and Bytes
1 kilobit (Kb) == 1,000 bits
1 megabit (Mb) == 1,000,000 bits
1 gigabit (Gb) == 1,000,000,000 bits
1 terabit (Tb) == 1,000,000,000,000 bits

- UTP Cables
Unshielded twisted pair which has no metallic shield subsceptible to  rf interference.
Twisted cable = Protects against EMI(Electromagnetic Interference)

Full-Duplex transmission configuration on 10BASE-T, 100BASE-T (can send and receive data at the same time without collision) using straight through cable.
- Routers and PC Transmit data on pins 1&2 and receive on 3&6. 
- Switches transmit on 3&6 and receive on 1&2.

Cross over cable
- Cable pairs are reversed allowing pin switch Receive(Rx) 1 to connect to Switch Transmit(tx) 3 etc. 
- This allows devices that use the same pins for transmitting and receiving to avoid collision or packet loss. Avoids a transmit pin going to another device's transmit pin instead of its receiving pin.

Auto MDI-X
- Allows devices to automatically detect which pins another device is transmitting data on and adjusts configuration to allow communication.

UTP Cables (1000BASE-T, 10GBASE-T)
- 4 Pair utilization: All eight wires (four pairs) are active, providing increased bandwidth (1Gbps/10Gbps).

Fiber-Optic Connections
- SFT Transceiver is used (Small Form-Factor Pluggable) used with fiber optic cable. 
- Two connectors used == one for transmitting and receiving on both ends. 

Difference between single and multimode fiber
- Core diameter is wider than single mode fiber.
- Allows multiple angles (modes) of light waves to enter the fiberglass core.
- Multi-mode allows longer than UTP, but shorter cables than single-mode fiber
- Cheaper than single-mode fiber (due to cheaper LED based SFP transmitters) - Single mode uses laser based SFP transmitters.


Ethernet Standards
- Defined in the IEEE 802.3 standared in 1983
- IEEE == Institute of Electrical and Electronics Engineers

 

