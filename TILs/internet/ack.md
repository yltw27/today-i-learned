# ACK (Acknowkedge)

## How do browsers know a packet is lost

ACK is part of TCP (Transmission Control Protocol). ACK is a receipt of a packet, before a packet is going to be sent from device A to device B, ACK will be sent from A to B, which allows B to know which packet has arrived. When B has received the packet, it will also send an ACK back to A to inform A. There is also a timeout mechanism, if an ACK/packet didn’t arrive with the expected time (i.e. timeout), A will send the ACK/packet again.
