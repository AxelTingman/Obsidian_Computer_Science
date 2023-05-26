#Kurs/Datorsystem #Kurs/Datorsystem/Föreläsning/8 

Software emulation of an abstract machine:
- Give programs illusion they own the machine  
- Make it look like hardware has features you want  

Two types of “Virtual Machine”s:
- [[Process VM]]: supports the execution of a single program; this  
functionality typically provided by OS  
- System VM: supports the execution of an entire OS and its  
applications (e.g., VMWare Fusion, Virtual box, Parallels Desktop,  
Xen)

Useful for OS development  :
- When OS crashes, restricted to one VM  
- Can aid testing programs on other OSs

![[f8_vm_layers.png]]

## Approaches to VM

• Allows one or more cores to be  
dedicated to a particular process and  
then leave the processor alone to  
devote its efforts to that process  
• Multicore OS could then act as a  
hypervisor that makes a high-level  
decision to allocate cores to applications  
but does little in the way of resource  
allocation beyond that

***
## Globala Informationssystem

Många användare, med var sin virtuella dator använder samma hårdvara samtidigt, fast varje användare upplever sig ensam på den fysiska datorn. Datorn körs i [[Molntjänster (Cloud)|molnet]].

Användare och applikationer på olika datorer når inte varandra och konkurrerar ej om samma  hårdvaruresurser.

Virtualiseringsmiljön tilldelar hårdvaruresurser
- [[Belastningsutjämning (load balancing)]]
- [[Skalbar hårdvara]]

***
# Exempel
- [[VirtualBox]]