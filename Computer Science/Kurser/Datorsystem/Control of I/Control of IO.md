#Kurs/Datorsystem 
[[IO]]
# Control of IO

I/O can be controlled in five general ways.  
– Programmed I/O reserves a register for each I/O  
device. Each register is continually polled to detect  
data arrival.  
– Interrupt-Driven I/O allows the CPU to do other things  
until I/O is requested.  
– Memory-Mapped I/O shares memory address space  
between I/O devices and program memory.  
– Direct Memory Access (DMA) offloads I/O processing  
to a special-purpose chip that takes care of the  
details.  
– Channel I/O uses dedicated I/O processors.