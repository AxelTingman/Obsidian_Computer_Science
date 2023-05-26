#Kurs/Datorsystem 
Certain registers hold the context of thread  
– Stack pointer holds the address of the top of stack  
• Other conventions: Frame Pointer, Heap Pointer, Data  
– May be defined by the instruction set architecture or by compiler  
conventions  
• Thread: Single unique execution context  
– Program Counter (PC), Registers, Execution Flags, Stack  
• A thread is executing on a processor when it is resident in  
the processor registers.  
• PC register holds the address of executing instruction in  
the thread.  
• Registers hold the root state of the thread.  
– The rest is “in memory”