## Basic functions of a computer
| Input | Processing | Output |
|---|---|---|
| A user types the letter "A" on the keyboard, which results in sending a code representing the letter A to the computer | The computer's CPU determines what letter was typed by looking up the keyboard code in a table | The CPU sends instructions to the graphics card to display the letter "A", which is then sent to the computer monitor |

## Processing Components
CPU:<br>
It executes instructions from computer programs, such as word processors and from the computer's operating system.<br><br>

Current CPUs are composed of two or more processors called cores:<br>
1) a multicore CPU is like a person with 2 brains
2) multicore CPUs enable computers to carry out multiple instructions simultaneously
3) results in better overall performance

## Storage Components
1) The more storage a computer has, the better the performance.<br>
2) Most storage components are both input and output devices<br>
3) Most people think of storage as disk drives and more...<br><br>

There are 2 main categories of storage:
1) Short-term storage
2) Long-term storage

## Short Term vs Long Term Storage
| volatile Memory | Non-volatile Memory |
|---|---|
| requires constant power to maintian the stored info | can store info without constant power |
| requires a consistent flow of power to retain data | require a consistent flow of power |
| affects system performance | affects system storage |
| faster | slower |

## Key components of a motherboard
| Component | Description |
|---|---|
| CPU socket | The CPU is installed here|
| PCI bys expeanstion slots | Used to add functionality to a PC by adding expansion cards that have a Peripheral Component Interconnect (PCI) connect |
| PCI-E expansion slots | PCI-Express supersedes PCI and supports faster data transfer speeds. The larger slots are suitable for high-performance expansion cards, such as graphics cards and disk controllers. The smaller slots are best suited to sound cards and network interface cards. |
| RAM Slots | Slots for installing RAM on the motherboard |
| Chipset with heat sinks | The chipset consists of two chips referred to as the Northbridge and the Southbridge. These chips control data transfers between memory, expansion slots, I/O devices, and the CPU. THe heat sink sits on top of ther chipset to prevent it from overheating. |
| IDE connector | Used for connection Intergrated Drive Electronics (IDE) hard drives and DC/DVD-ROM devices. Most systems now use SATA |
| SATA connectors | Used for connecting drives that use the Serial Advanced Technology Attachment (SATA) |
| Main power connector | This connector is where the motherboard receives power from the system power supply. |

## Computer Bus Fundamentals
| Bus type | Bus responsibility |
|---|---|
| Data Bus | - used to carry data signals from main memory to CPU and vice versa<br>- used to carry data signals from main memory to I/O devices vice versa  |
| Address Bus | - used to carry address signals, example a memory location or interface, where an IO device is attached |
| Control Bus | - used to carry control signals, example read or write, from CPU to memory or interface |

## Interrupt and Polling
| CPU Scheduling Method | function |
|---|---|
| Polling | CPU keeps on checking I/O devices at regular intervals weather it needs CPU service |
| Interrupt | the I/O device interrupts the CPU and tells the CPU that it needs service |
| Busy-wait | It repeatedly waits and checks for a condition to be met before continuing.<br><br>For resource availability, consider a scenario where a process needs resources for a particular program. However, the resource is currently in use and unavailable at this time, so the process must wait for the resource to become available before it can continue. |
| Blocking-wait | A blocked process is a process that is waiting for an event, such as a resource becoming available or completing an I/O operation.<br><br>In a multitasking computer system, individual tasks or threads of execution must share system resources. Shared resources include CPU, network and network interfaces, memory, and disk. |

## HDD vs SSD
| Category | HDD | SSD |
|---|---|---|
| Speed | HDD has a higher latency, longer read/write times and supports fewer IOPs (IO operations per second) compared to SSD. | SSD has lower latency, faster read/writes, and supports more IOPs compared to HDD. |
| Components | Has moving parts, primarily a motor driven spindle that holds one or more platters coated with a thin layer of magnetic material. Read and write heads are positioned at the top of the disks. | SSD has no moving parts, it is a flash based drive. It is interconnected with integrated circuits with an interface connector. There are three basic components - controller, cache and capcitor. |
| Weight | HDDs are heavier | SSDs are lighter |
| Cost | Cheap | More expensive |
| Usage | Storage (In the syllabus, it expects us to think it boots from here and not the SSD instead, maybe because the thing is really dated.) | Storage, higher speed storage, Usually found in mobile phones and high-performance systems (not really anymore) |

## BIOS/CMOS
BIOS: Basic IO system
- Set of instructions located in a chip on the motherboard
- Tells the CPU to perform certain tasks when power is first applied to the computer
- One of those instructions is to perform a power-on self test (POST)
- When a computer boots, the BIOS program offers a chance to run the Setup utility in order to configure hardware components

CMOS:
- This configuration is stored in a type of memory called CMOS

## Computer Boot Procedure
1) Power is applied to the motherboard
2) The CPU starts
3) The CPU carries out BIOS routines, including POST (Power On Self Test)
4) Boot devices, as specified in the BIOS config, are searched through for an OS
5) THe OS is loaded to RAM
6) OS services are started

## NIC Basics and wireless NIC
Computer that is connected to a nerwork requires a Network Interface Card (NIC) to create and mediate network connection.:
- Contains MAC (Media Access Control) address. MAC Address is a Unique identifier which assigned to NIC.

Wireless NIC must be chosen according to type of wireless AP (Access Point) which is referred as Wi-Fi:
- Some standards are: Wireless-n, 802.11ac or 802.11 a/b/g/n
- Wireless NICs connect to networks using SSIDs (Service Set Identifier)
- Can be configured to use a security key or a username and password