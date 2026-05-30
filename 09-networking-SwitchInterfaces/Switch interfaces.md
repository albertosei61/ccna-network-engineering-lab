Switch interfaces

Switch Commands

show interfaces status -> brings up port | Name(Description) | Status | Vlan | Duplex | Speed | Type

Duplex is auto on cisco devices

Interface range to set more than one interface at once
interface range f0/5 -12 

or more options
int range f0/5 - 6, f0/9 - 12

CSMA/CD -  Carrier sense multiple access with collision detection
- Devices listen to the collision domain until they detect that other devices are not sending
- If a collision does occur, the device sends a jamming signal to inform the other devices that a collision happened.
- Each device will wait a random period of time before sending frames again.

Speed/Duplex Auto negotiation is set up on all devices to avoid collisions.


Interface errors:
show interfaces f0/2 for example
- runts: Frames that are smaller than minimum frame size (64 bytes)
- Giants: Frames that are larger than the maximum frame size (1518 bytes)
- CRC: Frames that failed the CRC check (in the Ethernet FCS trailer)
- Frame: Frames that have an incorrect format (due to an error)
- Input errors: Total of various counters, such as the above four
- Output errors: Frames the switch tried to send, but failed due to an error.












