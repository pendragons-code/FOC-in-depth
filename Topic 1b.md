## Data and Bits
Data on a computer is stored as binary digits ("bits")
- A bit holds a value of 1 or 0 (usually it has a 5 volts of electricity to represent 1 bit and a pulse of 0 volts to represent a 0 bit)
- This can also be used in fibre optics, where the presence and absense of voltage is represented with light instead.
- 8 bits make a byte

## Functional units
This section is outdated due to 32 bit pretty much not being as relevant anymore, but this is out syllabus so...<br><br>
Primary memory:
- Organized into words (binary) of 32 bits
- A 32 bit word contains 4 8 bit bytes

A personal computer memory might have 4 Gigabyte or more (damn our textbook is really old).

Programs and their data must be in this memory to be executed

| Type | Purpose |
|---|---|
| Cache memory | - An adjuct to the main memory fabricated on the processor chip<br>- Much smaller and faster than the main memory<br>- Holds sections of the program and data currently/frequently being executed |
| Processor | - Logic Circuits: for performing arithmetic and logical operations on word-size data operands<br>- Timing and control circuits: for fetching program instructions and data from memory, one after another |
| Registers (typically 16 or 32) | each of which hold one word of operand data |

## Processor
| Arithmetic and Logic Unit | Control Unit |
|---|---|
| - Most computer operations are executed in the ALU of the processor<br>- Performs arithmetic or logic operation | - Memory, ALU and I/O units store and process I/O operations.<br>- The operation of these units must be coordinated (this is the responsibility of the control unit) |

## Operation of a computer
1) Computer accepts information in the form of programs and data through an input unit and stores it in the memory
2) Information stored in the memory is fetched under program control into an ALY, where it is processed
3) Processed information leaves the computer trhough an output unit
4) All activities in the computer are directed by the Control Unit

## Instruction Cycle Operations
| Step | Actions |
|---|---|
| 1 | Fetch an instruction and increment the program counter. |
| 2 | Decode the instruction and read registers from the register file. |
| 3 | Perfom an ALU operation. |
| 4 | Store instruction to memory. |
| 5 | Write the result into the destination register if needed. |

## Instruction and Programs
1) An instruction specifies an operation and the location of its data operands.
2) A 32 bit word typically holds one encoded instruction.
3) A sequence of instructions, executed one after another, forms a program.
4) Both a program and its data are stored in the main memory.

## Instruction Types
| Type | Details |
|---|---|
| Load | Read a data operand from memory or an input device into the processor. |
| Store | Write a data operand from a processor register to memory or an output device. |
| Operate | Perform an arithmetic or logic operation on data operands in processor registers. |

## Functional Units
| Unit | Responsibility |
|---|---|
| Program counter | Holds the memory address of the next instruction. |
| Instruction Register | Holds the current instruction. |
| General Pupose registers | Holds data and addresses. |
| COntrol circuits and the ALU | Fetches and executes instructions. |

## Program Counter
A program counter is a register in a computer processor that contains the address of the instruction being executed at the current time.<br><br>
As each instruction gets fetched, the program counter increases its stored value by 1. Afer each instruction is fetched, the program counter points to the next instruction in the sequence.<br><br>
When the computer restarts or is reset, the program counter normally reverts to 0.

## Handling I/O devices
| category | details |
|---|---|
| read | Read data (such as a keyboard characted from an input device) |
| write | Write data (such as letter character) to an output display screen |
| sense | Sense the readiness of an input or output device to perform a transfer |

## Performance
| category | details |
|---|---|
| Speed | Speed of electronic circuits in the processor |
| Access | Access times to the cache and main memory |
| Design | Design of the instruction set |
| Number | Number of operations that can be done at the same time (parallel tasks) |

## Parallelism
Multicore processors (across multiple cores):
- Multiple processing units can be fabricated on a single chip
- core is used to refer to these individual processors