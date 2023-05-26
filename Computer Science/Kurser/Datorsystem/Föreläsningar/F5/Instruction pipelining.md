#Kurs/Datorsystem #Kurs/Datorsystem/Föreläsning/5  
***
• Some [[CPU|CPUs]] divide the fetch-decode-execute cycle into  
smaller steps.  
• These smaller steps can often be executed in parallel to  
increase throughput.  
• Such parallel execution is called instruction pipelining.  
• Instruction pipelining provides for instruction level  
parallelism (ILP)

#### Vilka konflikter kan uppstå i en pipline?  
• Strukturella konflikter: Uppstår när 2 pipelinade  
instruktioner försöker använda en  
hårdvarukomponent(t.ex. primärminnet)) samtidigt.  
• Data konflikter: Uppstår när en instruktion påverkas av  
resultat från en annan instruktion som ännu inte är  
färdig.  
• Kontrollkonflikter: Uppstår när en conditional branch  
instruktion felaktigt hoppas över. Det Kan ske när  
branch–condition:et -> beror på resultatet från en  
pipline:ad instruktion som inte är färdig.