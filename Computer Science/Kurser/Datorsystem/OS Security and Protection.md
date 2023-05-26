#Kurs/Datorsystem 
***

- Operating systems must protect itself from user programs.
	- Reliability: Compromising the operationg system usually causes i to crash
	- Security: limit the scope of what processes can do
	- Privacy: limit each process to the data it is permitted to access
	- Fairness: Each should be limited to it's appropriate chare of system recources.

## Protecting applications from eachother
- The OS must protect the user programs from eachother
- Primary Mechanism: limit the translation from program  
address space to physical memory space

#### Problem:
- Run multiple applications in such a way that  
they are protected from one another  

#### Goal:  
- Keep User Programs from Crashing OS  
- Keep User Programs from Crashing each other  
- Keep Parts of OS from crashing other parts? 

#### (Some of the required) Mechanisms:  
- Address Translation  
- Dual Mode Operation  

#### Simple Policy:  
- Programs are not allowed to read/write memory of other  
Programs or of Operating System


## Memory Restricions
- Can only touch what is mapped into process address space
- Additional Mechanisms:  
	- Privileged instructions, in/out instructions, special registers  
	- syscall processing, subsystem implementation  
		(e.g., file access rights, etc)
		
