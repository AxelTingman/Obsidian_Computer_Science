#Kurs/Databasmetodik 
Egenskaper:  
● Lagrar till synes data i rader, men...  
● Lagrar data i serialiserade kolumner (en kolumn blir en rad i DB)  
● Den lagrade datan agerar nyckel (snarare än värde)  
● Värdet är istället index till förekomster i olika rader i datan  
● Snabbt att läsa, långsamt att lägga till och uppdatera  
Användningsområden: analytiska databaser / data warehousing  
Exempel: Cassandra (Apache), BigTable (Google), Druid, MariaDB ColumnStore