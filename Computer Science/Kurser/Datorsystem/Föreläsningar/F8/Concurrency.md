#Kurs/Datorsystem #Kurs/Datorsystem/Föreläsning/8 
***

## The Basic Problem of Concurrency  
The basic problem of concurrency involves resources:  
– Hardware: single [[CPU]], single [[DRAM]], [[IO|single I/O devices]]  
– [[Multiprogramming]] API: processes think they have exclusive access to  
shared resources  

[[Operating System|OS]] has to coordinate all activity  
– Multiple [[Kurser/Datorsystem/Föreläsningar/F8/Process|processes]], [[IO|I/O interrupts]], ...  
– How can it keep all these things straight?  

Basic Idea: Use [[Virtual Machine]] abstraction  
– Simple machine abstraction for processes  
– [[Multiplex in time|Multiplex]] these abstract machines  
• Dijkstra did this for the “THE system”  
– Few thousand lines vs 1 million lines in OS 360 (1K bugs)