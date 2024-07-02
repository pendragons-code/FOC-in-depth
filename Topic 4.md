## Network Repeaters and Hubs
- A repeaster receives bit signals geerated by NICs and other devices. It strengthens them and then "repeats" them to other parts of the network.
- A repeater enables you to connect computers whose distance from one another would make communication impossible
- A traditional repeater has 2 ports or connections that you can use to extend your network

## Multiport Repeaters and Hubs
- Hubs cleans the signals by filtering out electrical noise
- They transmit the regenerated signal to all other ports where a computer (or other network device) is connected to
- Receives bit signals generated from a connected computer's NIC on one of its ports
- Regereates the signal to full strength

## Duplex:
Half-duplex is when data can only go in one direction at a time.<br>
Full-duplex is when data can flow in both directions at the same time.

## Steps of switch operation
1) The switch receives a frame.
2) The switch reads the source and destination MAC addresses
3) The switch looks up the destination MAC address in the switching table
4) The siwtch forwards the frame to the port where the computer owning the MAC address is found
5) Tne switching table is updated with the source MAC address and the port information

## What is a hub-switch-router
| Characteristic | Hubs | Switches | Routers |
|---|---|---|---|
| intelligence | false | true | true |
| duplex | half | full | full |
| bandwidth | divided by all | dedicated | dedicated |
| data destination | all | only to the specified MAC address in frame | only to specified IP address in packet |
| table type | none | switching | routing |
| info type | none | frame | packet |
| address type | none | mac | ip |
| internet | Cannot provide internect connection (only interconnect computers) | Cannot provide internect connection (only interconnect computers) | can provide a connection |
| broadcast | yes | forwards broadcasts | no |
| usage | to create Networks (LANs) | to create Networks (LANs) | to connect networks (LANs) |
| Additional Remarkds | As the hub duplicates data frames across all ports, it wastes bandwidth and creates security risks. | Has a set of operations to determine destination, this is done so by the switch learning the mac addresses of all connected device and storing them in a table (switching table). | Get packet, inspects it, checks if the ip address matches to the packet to see if the packet was intended for the router's network or another. If it ain't for the router's network, the packets are sent away. |

## Switch Operations:
- Data is sent onto the medium one frame at a time
- Each frame has the destination and source MAC address
- Switch reads the address
	- Uses the source MAC address of frame to keep a record of which computer is which port (switching table)
	- Forwards the frame to the port where the destination MAC can be found

## Switch Ops step-by-step
1) receives frame
2) reads sources and destination MAC address
3) looks up the destination MAC address in its switching table
4) forwards the frame to the port where the computer owning the MAC address is found
5) the switching table is updated with the source MAC address and port information

## What is a Wireless Access Point
- The heart of a wireless network is the wireless access point (AP)
- APs operate similarly to a hub without wires
- All communication passes through the AP
- Most small businesses and home networks typically called wireless router that combines an AP, switch and a router
- Wireless LANs are usually attached to wired networks

## What is a NIC
- A NIC provides a connection from computer to the medium
- Incoming messages: receives bit signals and assembles them into frames
	- verifies the destination address
	- removes the frame header and sends the resulting packets to the network protocol
- Outgoing messages: recives packet from network protocol
	- creates frame by adding MAC address/error checking
	- converts frame to bit signals suitable for the medium and transmits them

## multicast-broadcast-unicast
| broadcast | unicast | multicast |
|---|---|---|
| to all parties | to only one party | multiple (does not to be all) parties |

## NICs and MAC addresses
NIC manufacturers ensure that every NIC produced has a unique address
- Networks won't function correctly if duplicate MAC addresses exists.
MAC address is stored in ROM on the NIC<br>
The address consists of 2 24-bit hexadecimal numbers:
- 24-bit manufacturer ID called OUI
- 24-bit serial number assigned by the manufacturer

- 48-bit address expressed in 12 hexadecimal digits
    - 04-40-31-5B-1A-C4

## NICs as Gatekeeper
When a frame arrives at a NIC, the NIC checks the frame's destination MAC address to see weather it matches it's built in MAC address<br><br>
NIC only permits inbound communications if the destination MAC:
- Matches the NICs burned in address
- Is a broadcast address
- NIC is in a special mode called promiscuous

When the destination MAC address mastches the MAC burned-in address (BIA), or the physical address of a NIC, it's a unicast frame
- intended for a single computer

## How routers forward packet
When routers forward packets, the MAC address header is stripped and regenerated to get it to the next hop. The IP header generated by the first computer is only stripped off by the final computer, hence the IP header handled the "end to end" delivery, and each of the four different MAC header.
