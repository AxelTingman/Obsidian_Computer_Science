#Kurs/Datorsystem 
[[Virtual memory]]
# Segmentation 
• Another approach to virtual memory is the use of  
segmentation.  
• Instead of dividing memory into equal-sized pages,  
virtual address space is divided into variable-length  
segments, often under the control of the programmer.  
• A segment is located through its entry in a segment  
table, which contains the segment’s memory location  
and a bounds limit that indicates its size.  
• After a page fault, the operating system searches for a  
location in memory large enough to hold the segment  
that is retrieved from disk.

Causes [[External fragmentation|external fragmentation]].