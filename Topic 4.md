## Network Repeaters and Hubs
- A repeaster receives bit signals geerated by NICs and other devices. It strengthens them and then "repeats" them to other parts of the network.
- A repeater enables you to connect computers whose distance from one another would make communicaton impossible
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
3) The switch looks up the destinaton MAC address in the switching table
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
## NICs as Gatekeeper
## Wireless NICs
## How routers forward packet