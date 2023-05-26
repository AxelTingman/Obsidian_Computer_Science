#Kurs/Datorsystem #Kurs/Datorsystem/Föreläsning/8 

- Hardware provides at least two modes:  
	- “Kernel” mode (or “supervisor” or “protected”)  
	- “User” mode: Normal programs executed 
	
- Some instructions/ops prohibited in user mode:  
	- Example: cannot modify page tables in user mode  
- Attempt to modify Þ Exception generated  
- Transitions from user mode to kernel mode:  
	- System Calls, Interrupts, Other exceptions