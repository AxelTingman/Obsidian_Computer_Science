#Kurs/Datorsystem 
***

• Process: execution environment with Restricted Rights  
– Address Space with One or More Threads  
– Owns memory (address space)  
– Owns file descriptors, file system context, ...  
– Encapsulate one or more threads sharing process resources  
• Why processes?  
– Protected from each other!  
– OS Protected from them  
– Processes provides memory protection  
– Threads more efficient than processes (later)  
• Fundamental tradeoff between protection and efficiency  
• Communication easier within a process  
• Communication harder between processes  
• Application instance consists of one or more processes

– A running program is a process.  
– It is allocated a number of resources:  
• Registers in the CPU  
• Some part of the CPU’s RAM  
• I/O devices (the monitor, files in the file system)  
• Several copies of the same program can be running as  
different processes.  
– But data values, current Program Counter location, etc., will  
differ among the different processes