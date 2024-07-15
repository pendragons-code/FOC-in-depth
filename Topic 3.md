## Network Components
| Name | Purpose |
|---|---|
| Network Interface Card | - An add-on card plugged into a motherboard expansion slot that provides a connection between the computer and the network. |
| Network Medium | - A cable that plugs into the NIC and makes the connection between a computer and the rest of the network.<br>- Network media can also be the air waves, as in wireless networks. |
| Interconnecting Device | Allows two or more computers to communicate on the network without having to be connected directly to one another. |

## Network Components
Network clients and servers:
- Network client software requests information stored on another network computer or device (e.g. chrome web browser)<br>
- Network server software allows a computer to share its resources (e.g. Apache web server)

Protocols
- Defines the rules and formats a computer must use when sending information across the network (e.g. TCP/IP protocol stack)

NIC driver:
- Receives data from protocols and forwards this data to the physical NIC

## Layers of the Network Communication Process
| Step | Description | Layer |
|---|---|---|
| 1 | An application tries to access a network resource. | User Application |
| 2 | Client software detects the attempts to access the network and passes the message on the network protocol. | Network Software |
| 3 | The protocol packages the message in a format suitable for the network and sends it to the NIC driver | Network Protocol |
| 4 | The NIC driver sends the data in the request to the NIC card, which converts it into the necessary signals to be transmitted across the network medium. | Network Interface |

![layers](https://github.com/pendragons-code/FOC-in-depth/blob/master/assets/Network-layers.png)

## How two computers communicate on a LAN
TCP/IP is the most common protocol (language) used on networks
TCP/IP uses 2 addresses to identify devices:
- Logical address(IP address) - e.g. 192.168.1.41
- Physical address (MAC address) - e.g. 24-77-03-FA-24-D0

Just as a mail person needs an address to deliever mail, TCP/IP needs an address in order to deliver data to the correct device on a network:
- Think of the Logical address as your name and the physical address as your postal address

## How two Computers Communicate on a LAN
| step | details |
|---|---|
| 1 | A user at Computer A types ping 10.1.1.2 at a command prompt |
| 2 | Network software creates a ping message |
| 3 | The network protocol packages the message by adding IP address of sending and destination computers and acquires the destination computer's MAC address |
| 4 | The network interfact software adds MAC address of sending and destination computers |
| 5 | Computer B receive message, verifies that the addresses are correct and then sends a reply to computer A using steps 2-4 |

## CIDR IP Address
| RESERVED IP ADDRESS |
|---|
| 192.168.1.0 subnet |
| 192.168.1.255 broadcast |
| 256 - 2 = 254 |

![CIDR Notation](https://github.com/pendragons-code/FOC-in-depth/blob/master/assets/CIDR.png)

## Broadcast IP address:
Example: 192.168.1.255/24<br>
Broadcast addressing was designed to facilitate message broadcasting for all network devices.

## LANs, Internetworks, WANs and MANs
| Network | Description |
|---|---|
| Local Area Network | Small network, limited to a single collection of machines and connected by one or more interconnecting devices in a smaller geographic area. |
| Internetwork | A networked collection of LANs tied together by devices such as routers<br>Reason for creation:<br>- Two or more groups of users and their computers need to be logically separated but still needs to communicate.<br>-Number of computers in a single LAN has grown and is no longer efficient<br>THe distance between 2 groups of computers exceeds the capabilities of most LAN devices. |
| Wide Area Networks | Uses the services of third-party communcation providers to carry network traffic from one location to another (covers world-wide) |
| Metropolitan Area Networks | Uses WAN technologies to interconnect LANs in a specific geographic region, such as a county of city (or a campus) |

## Broadcast IP address
| internetwork | details |
|---|---|
| Internet | A worldwide public internetwork. Uses protocols such as TCP/IP and HTTP to transfer and view information |
| Intranet | A private internetwork in which devices and servers are only available to those users connected to the internal network (like an internal internet) |
| Extranet | Allows limited and controlled access to internal resources by outside users |

## LAN: Privated IP address
Reserved for private networks. The organisations that distribute IP addresses to the world reserves a range of IP addresses for private networks:
- 192.168.0.0 to 192.168.255.255 (65,536 IP addresses)
- 172.16.0.0 to 172.31.255.255 (1,048,576 IP addresses)
- 10.0.0.0 to 10.255.255.255 (16,777,216 IP addresses)

## Packet Traveling
When data leaves your computer, it is grouped into small chunks called packets. These packets are essentially little envelopes that carry data across the internet (Network of networks connected through routes)<br><br>
Computers transfer information across networks in short bursts of about 1500bytes of data.

## Packet and Frames
- Pause between bursts allows other computers to transfer data during pauses.
- It allows the receiving computer to process received data.
- Allows the receiving computer data from other computers at the same time.
- Gives the sending computer an opportunity to receive data from other computers and perform other processing tasks
- If an error occues during transmission of a larfe file, only the chunks of the data involved in the error has to be sent again.

## Packets
Packet: a chunk of data with a source and destination IP address added to it (routers route packet between networks)<br>
| Destination IP | Src IP | Protocol | Destination Port | Source Port | Http Request |
|--|--|--|--|--|--|

## Frames
Frame: a packet with the source and destination MAC addresses added to it
- The packet is "framed" by the MAC addresses on one end and an error-checking code on the other (NIC sends and receives frames)

The proess of adding IP addresses and MAC addresses to chunks of data is called encapsulation.
- Information added to the front of the data is called a header and information added to the end is called a trailer.

| Destination MAC | Source MAC |  Destination IP | Source IP | Destination Port | Source Port | Http Request | Frame trailer |
|--|--|--|--|--|--|--|--|

## Clients
A clinet can be a workstation running a client OS or it can refer to the network software on a computer that requests network resources from a server.<br>
The word "client" is usually used in these three contexts:
- Client operating system - the OS installed on a computer
- Client computer - primary role is to run user applications and access network resources
- Client software - software that requests network resources from server software on another computer

## Servers
A computer becomes a server when software is installed on it that provieds a network service to client computers.


The term "servers" is also used in three contexts:
- Server operating system - OS installed on a computer designed to share network resources and provide other network services
- Server computer - a computer's primary role in the network is to give client computers access to network resources and services
- Server software - responds to requests for network resources from client software
