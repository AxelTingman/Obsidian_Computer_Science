#Kurs/Datorsystem #Kurs/Datorsystem/Föreläsning/8 
### Properties of this simple multiprogramming technique  
• All virtual [[CPU|CPUs]] share same non-CPU resources  
– [[IO|I/O devices]] the same  
– Memory the same  
• Consequence of sharing:  
– Each [[Threads|thread]] can access the data of every other thread (good for  
sharing, bad for protection)  
– Threads can share instructions  
(good for sharing, bad for protection)  
– Can threads overwrite OS functions?  
• This (unprotected) model is common in:  
– Embedded applications  
– Windows 3.1/Early Macintosh (switch only with yield)  
– Windows 95—ME (switch with both yield and timer)