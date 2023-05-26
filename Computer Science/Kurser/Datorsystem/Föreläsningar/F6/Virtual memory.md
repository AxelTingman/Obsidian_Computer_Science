#Kurs/Datorsystem #Kurs/Datorsystem/Föreläsning/6 
***

• [[Cache]] memory enhances performance by providing  
faster memory access speed.  
• Virtual memory enhances performance by providing  
greater memory capacity, without the expense of  
adding main memory.  
• Instead, a portion of a disk drive serves as an  
extension of main memory.  
• If a system uses paging, virtual memory partitions  
main memory into individually managed page  
frames, that are written (or paged) to disk when they  
are not immediately needed.

• A physical address is the actual memory address  
of physical memory.  
• Programs create virtual addresses -> mapped to  
physical addresses by the memory manager.  
• Page faults occur when a logical address requires  
that a page be brought in from disk.  
• Memory fragmentation occurs when the paging  
process results in the creation of small, unusable  
clusters of memory addresses.

• Main memory and virtual memory are divided into  
equal sized pages.  
• The entire address space required by a process  
need not be in memory at once. Some parts can  
be on disk, while others are in main memory.  
• the pages allocated to a process do not need to be  
stored contiguously-- either on disk or in memory.  
• Then only the needed pages are in memory at any  
time, the unnecessary pages are in slower disk  
storage.

52  
• Information concerning the location of each page,  
whether on disk or in memory, is maintained in a data  
structure called a page table (shown below).  
• There is one page table for each active process.

## [[Segmentation]]

## [[Paging]]

## [[Translation look-aside buffer (TLB)]]