#Kurs/Datorsystem #Kurs/Datorsystem/Föreläsning/8 
• Assume a single [[CPU|processor]]. How do we provide the illusion of  
multiple processors?  
– Multiplex in time!  
• Each virtual “CPU” needs a structure to hold:  
– Program Counter (PC), Stack Pointer (SP)  
– Registers (Integer, Floating point, others...?)  
• How switch from one virtual CPU to the next?  
– Save PC, SP, and registers in current state block  
– Load PC, SP, and registers from new state block  
• What triggers switch?  
– Timer, voluntary yield, I/O, other things