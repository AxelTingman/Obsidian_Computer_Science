#Kurs/Databasmetodik 

Ett ramverk för [[Kurser/Databasmetodik/Alternativ till relationsmodellen/Big data|Big data]]


![[hadoop_ekosystem.png]]
## Hadoops ekosystem
- En skiktad, staplad arkitektur (se illustrerat exempel)  
- Lägre nivåer: lagring och schemaläggning  
- Högre nivåer: interaktivitet  
- Modulärt

● HDFS: Hadoop Distributed File System  
○ Fundament för Hadoops ekosystem  
○ Erbjuder skalbarhet och pålitlighet (genom att hantera till exempel hårdvarufel)  
○ Lagring av massiva datamängder: upp till 200 PB, 4500 servrar och 1 miljard filer och block  
○ Delar upp filer mellan noder för parallell åtkomst

● YARN: Yet Another Resource Negotiator  
○ Hadoops resurshanterare  
○ Interagerar med applikationer och schemalägger resurser  
○ Nytt för Hadoop 2.0  
■ Tillåter mer än bara MapReduce  
■ Förbättrar användning av resurser

● MapReduce: programmeringsmodell för Hadoops ekosystem  
○ Förenklar parallellprogrammering  
○ Utnyttjar YARN för schemaläggning+exekvering av parallell bearbetning över filblock i HDFS  
● Map = utför operation på alla element  
● Reduce = sammanfatta operation på element

● Hive: data warehousing-infrastruktur för dataanalys och rapportering  
○ Utvecklat av Facebook, senare open source  
● Använder MapReduce  
● Har ett SQL-likt gränssnitt som tillåter relationell datamodellering  
○ Används framför allt av analytiker

● Pig: data warehousing-infrastruktur för applikationsutveckling  
○ Utvecklat av Yahoo!, senare open source  
● Använder också MapReduce  
● Har också ett SQL-likt gränssnitt  
○ Används av forskare och programmerare (t.ex. för LinkedIns People You May Know)

● HBase: en icke-relationell, distribuerad databas  
○ Modellerad efter Googles BigTable  
● Använder HDFS

● Cassandra: en NoSQL-databas  
○ Column Store (använder inte HDFS)  
● Har sitt eget filsystem  
● Hög prestanda och skalbarhet  
○ Används t.ex. av NetFlix