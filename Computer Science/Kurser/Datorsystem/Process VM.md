#Kurs/Datorsystem 

[[Virtual Machine]]
# Process VM
***

Programming simplicity  
- Each process thinks it has all memory/CPU time  
- Each process thinks it owns all devices  
- Different devices appear to have same high level interface  
- Device interfaces more powerful than raw hardware  
	- Bitmapped display -> windowing system  
	- Ethernet card -> reliable, ordered, networking (TCP/IP)  

Fault Isolation  
- Processes unable to directly impact other processes  
- Bugs cannot crash whole machine  

Protection and Portability  
- Java interface safe and stable across many platforms