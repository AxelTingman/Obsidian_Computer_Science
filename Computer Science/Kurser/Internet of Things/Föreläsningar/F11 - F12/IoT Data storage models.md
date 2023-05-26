#Kurs/Internet_of_Things #Kurs/Internet_of_Things/Föreläsning/11-12

● New Architecture 
	– Data in C-store (column-store) is not physical stored using its related relational logical data model 
	– Most row stores implement physical tables directly and then add various indexes to speed access, Cstore implements only projections 
	– Projections are sorted subsets of the attributes of a table. 
● Large-scale storage in distributed environments [[Fog Computing]]
	– Users from different locations may have different data consumption needs 
	– Propose a selective replica strategy which supports replica of tables in the Web databases at record level to alleviate the overly replicated issue. 
	– Replica strategy, each replica location stores a full or partial copy of the replicated table depending on the data needs. Selective replica strategy: Consistency, Availability and Partition tolerance. 
● Storage on resource-constrained devices 
	– Storage issues also arise in resource-constrained scenarios in IoT. Sensor networks, communication activity normally plays a more important role than storage. Batch data collection, delay-tolerant mobile applications, and disconnected operations in static networks, the storage-centric paradigm becomes more critical. Decreasing costs and increasing capacity of storage hardware.