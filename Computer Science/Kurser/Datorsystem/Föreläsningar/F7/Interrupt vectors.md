#Kurs/Datorsystem #Kurs/Datorsystem/Föreläsning/7 
# Interrupt vectors
***

• The status of the interrupt signal is checked at the  
top of the fetch-decode-execute cycle.  
• The particular code that is executed whenever an  
interrupt occurs is determined by a set of  
addresses called interrupt vectors that are  
stored in low memory.  
• The system state is saved before the Interrupt  
Service Routine (ISR) is executed and is restored  
afterward.