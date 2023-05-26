#Kurs/Datorsystem #Kurs/Datorsystem/Föreläsning/5

Instruction Set Architectures are measured  
according to:  
• Main memory space occupied by a program.  
• Instruction complexity.  
• Instruction length (in bits).  
• Total number of instructions in the  
instruction set.

In designing an instruction set, consideration is  
given to:  
• Instruction length.  
– Whether short, long, or variable.  
• Number of operands.  
• Number of addressable registers.  
• Memory organization.  
– Whether byte- or word addressable.  
• Addressing modes.  
– Choose any or all: direct, indirect or indexed.

• Byte ordering, or endianness, is another major  
architectural consideration.  
• If we have a two-byte integer, the integer may be  
stored so that the least significant byte is followed  
by the most significant byte or vice versa.  
– In little endian machines, the least significant byte  
is followed by the most significant byte.  
– Big endian machines store the most significant byte  
first (at the lower address).

[[Big endian]]
[[Little endian]]


• The next consideration for architecture design  
concerns how the CPU will store data.  
• We have three choices:  
1. A [[Stack architecture|stack architecture]]  
2. An [[Accumulator|accumulator]] architecture  
3. A [[General Purpose Register (GPR)]] architecture.  
• In choosing one over the other, the tradeoffs are  
simplicity (and cost) of hardware design with  
execution speed and ease of use.