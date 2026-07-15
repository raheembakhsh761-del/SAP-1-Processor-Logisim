\# SAP-1 Computer



A hardware implementation of the \*\*SAP-1 (Simple-As-Possible 1)\*\* processor architecture, built and simulated in \[Logisim Evolution](https://github.com/logisim-evolution/logisim-evolution). This project demonstrates the fundamental building blocks of a CPU, from registers and the ALU to the control unit that ties everything together.



\## Overview



SAP-1 is a classic educational CPU architecture used to teach the basics of digital computer design. It uses an 8-bit data bus, a simple instruction set, and a sequential control unit to fetch, decode, and execute instructions.



\## Complete Processor



The figure below shows the complete SAP-1 processor implemented in Logisim Evolution.



<p align="center">

&#x20; <img src="images/overall%20sap-1-computer%20diagram.png" width="800">

</p>



The processor includes the Program Counter, Memory Address Register, RAM, Instruction Register, Control Unit, ALU, Accumulator, B Register, and Output Register, all connected via a shared 8-bit bus.



\## Modules



\### Program Counter

A 4-bit counter that keeps track of the address of the next instruction to be fetched.



<p align="center">

&#x20; <img src="images/program\_counter.png" width="600">

</p>



\### Memory Address Register (MAR)

Holds the address of the memory location currently being accessed by the RAM.



<p align="center">

&#x20; <img src="images/Memory%20Adder%20Register%20.png" width="600">

</p>



\### Instruction Register

Stores the current instruction fetched from memory, splitting it into an opcode and operand.



<p align="center">

&#x20; <img src="images/Instruction%20Register%20.png" width="600">

</p>



\### Control Unit

Generates the timing and control signals that sequence each instruction through fetch, decode, and execute cycles.



<p align="center">

&#x20; <img src="images/control%20unit%20.png" width="700">

</p>



\### Instruction Decoder

Decodes the opcode from the Instruction Register and activates the corresponding control lines.



<p align="center">

&#x20; <img src="images/instruction%20decoder.png" width="600">

</p>



\### Ring Counter

Generates the sequential timing states (T1–T6) used by the Control Unit to step through each instruction cycle.



<p align="center">

&#x20; <img src="images/Ring%20counter%20.png" width="600">

</p>



\### ALU (Adder/Subtractor)

Performs addition and subtraction on the Accumulator and B Register values, with subtraction implemented using 2's complement.



<p align="center">

&#x20; <img src="images/ALU\_Adder\_and-substructor%20.png" width="700">

</p>



<p align="center">

&#x20; <img src="images/Half\_Adder.png" width="400">

</p>



<p align="center">

&#x20; <img src="images/sub%20module.png" width="500">

</p>



\### Accumulator

An 8-bit register that stores intermediate results of arithmetic operations.



<p align="center">

&#x20; <img src="images/accmulator%20.png" width="600">

</p>



\### B Register

Holds the second operand used by the ALU during arithmetic operations.



<p align="center">

&#x20; <img src="images/Register%20B.png" width="600">

</p>



\### Output Register

Latches the final result from the bus and displays it on the output.



<p align="center">

&#x20; <img src="images/output%20register%20.png" width="600">

</p>



\### Tri-State Register

A reusable general-purpose register with tri-state output buffers, used as the building block for several components above.



<p align="center">

&#x20; <img src="images/Tri\_stage%20Register.png" width="600">

</p>



\## Getting Started



1\. Install \[Logisim Evolution](https://github.com/logisim-evolution/logisim-evolution).

2\. Open `sap-1-computer.circ` in Logisim Evolution.

3\. Load a program into RAM and run the simulation to see the processor fetch, decode, and execute instructions.



\## Repository Structure



```

├── sap-1-computer.circ   # Main Logisim Evolution project file

├── images/                # Circuit diagrams used in this README

└── README.md

```

