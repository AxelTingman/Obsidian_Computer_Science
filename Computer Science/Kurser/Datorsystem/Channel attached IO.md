#Kurs/Datorsystem 
[[IO]]
# Channel attached IO
***

• In very large systems employ Channel-attached I/O  
• One or more I/O processors (IOPs) that control various  
channel paths.  
• Slower devices such as terminals and printers are  
combined (multiplexed) into a single faster channel.  
• Distinguished from DMA by the intelligence of the IOPs.  
• The IOP negotiates protocols, issues device  
commands, translates storage coding to memory coding,  
and can transfer entire files or groups of files  
independent of the host CPU.

![[f7_cannel_attached_io.png]]