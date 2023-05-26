#Kurs/Datorsystem #Kurs/Datorsystem/Föreläsning/8 
• The operating system schedules process execution.  
• First, the operating system determines which process  
shall be granted access to the CPU.  
– This is long-term scheduling.  
• After a number of processes have been admitted, the  
operating system determines which one will have  
access to the CPU at any particular moment.  
– This is short-term scheduling.  
• Context switches occur when a process is taken from  
the CPU and replaced by another process.  
– Information relating to the state of the process is  
preserved during a context switch.


[[Short-term scheduling]]

• In non-preemptive scheduling, a process has use of  
the CPU until either it terminates, or must wait for  
resources that are temporarily unavailable. 

[[Preemtive scheduling]]



## Four approaches to CPU scheduling are:  
– **First-come, first-served** where jobs are serviced in arrival  
sequence and run to completion if they have all of the  
resources they need.  
– **Shortest job first** where the smallest jobs get scheduled  
first. (The trouble is in knowing which jobs are shortest!)  
– **Round robin scheduling** where each job is allocated a  
certain amount of CPU time. A context switch occurs when  
the time expires.  
– **Priority scheduling** preempts a job with a lower priority  
when a higher-priority job needs the CPU.