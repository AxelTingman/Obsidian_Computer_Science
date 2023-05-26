#Kurs/Datorsystem 
***
• Faster memory is more expensive than slower  
memory.  
• To provide the best performance at the lowest  
cost, memory is organized in a hierarchical  
fashion.  
• Small, fast storage elements are kept in the CPU,  
larger, slower main memory is accessed through  
the data bus.  
• Larger, (almost) permanent storage in the form of  
disk and tape drives is still further from the CPU.

• This storage organization can be thought of as a pyramid:

![[f6_memory_hierarchy.PNG]]

![[f6_memory_hierachy_2.PNG]]

![[f6_memory_hierarchy_3.PNG]]

13  
• Virtual memory -> implemented using a hard drive  
– it extends the address space from RAM to the  
hard drive.  
• Virtual memory provides more space:  
• Cache memory provides speed.


• CPU ->  
– sends a request to nearest memory->usually  
cache.  
– If data not in cache-> main memory  
– If data not in main memory-> disk  
• Once the data is located, -> the data, and a number  
of its nearby data elements are fetched into cache  
memory.  
– Hit -> data is found  
– Miss -> not found