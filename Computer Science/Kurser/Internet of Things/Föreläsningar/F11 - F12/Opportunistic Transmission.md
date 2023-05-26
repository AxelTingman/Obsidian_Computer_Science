#Kurs/Internet_of_Things #Kurs/Internet_of_Things/Föreläsning/11-12 
• It works well without requiring any centralized server or infrastructure for communication and management. 
• It reduce the workload of cellular networks in dense areas. 
• Energy-efficient: less expensive, which is very important because most users hope to save battery energy and data usage on their mobile devices. 
• Characteristics of human mobility from the perspectives of both sensing and transmission.

## Human mobility
● Unique characteristics such as: Spatiotemporal correlation, hotspots’ effects, and sociality. (uncontrolled mobility) 
● Identifying these characteristics is beneficial to estimate: sensing quality, perform network planning, design efficient sensing and transmission protocols, and develop accurate mobility models. 
● OPPORTUNITIES IN OPPORTUNISTIC SENSING 
	– How can the sensing opportunities and sensing quality be measured? 
		• inter-cover time to characterize the opportunity with which a sub-region is covered ( in time domain). 
	– How many mobile users can provide enough sensing opportunities to achieve the required sensing quality? 
		• The opportunistic coverage ratio to characterize the relationship between the sensing quality and the number of users. 
● OPPORTUNITIES IN OPPORTUNISTIC TRANSMISSION 
	– The transmission opportunities of human mobility and their impacts on the data delivery performance have been intensively studied and relatively well understood in opportunistic networks or delaytolerant networks (DTNs). 
	– The inter-contact time is one key metric to characterize the transmission opportunities of the same couple of mobile users. 
	– Human sociality has a key impact on human mobility, since it decides the spatial properties of human mobility (i.e., where people move). human sociality has been considered an important factor affecting the performance of opportunistic forwarding protocols

## Inter-cover time
• The coverage in MCS is time-variant due to human mobility. 
• T into multiple sampling periods of Ts. 
• In the space domain, we divide the monitoring region into a set of grid cells (b). 
• A grid cell is said to be covered by a mobile user only when a new sampling period arrives and the location of the mobile user is just within the area of the grid cell. 
• The inter-cover time is defined as the time elapsed between two consecutive periods of coverage of the same grid cell. 
• Shorter inter-cover time results in better sensing quality for a grid cell.


![[social-based_opportunistic_protocols.png]]


● Many opportunistic forwarding protocols have been proposed in opportunistic networks ● Epidemic Routing 
	– Without knowing anything about the mobility of users. 
	– Grasp each forwarding opportunity, thus resulting in the minimum delivery delay under ideal conditions (unlimited resources such as bandwidth and buffer space) at high cost. 
	– In order to reduce the cost, many variants of epidemic routing have been proposed (k- hop schemes, probabilistic forwarding, spray- and-wait, etc) 
	– Some protocols : identify the best relay node to achieve better trade-off between delivery delay and transmission overhead by exploiting the context information (e.g., the mobility of a node and its current energy level). Several works have exploited human sociality for improving opportunistic transmission performance. Most existing social-based opportunistic forwarding protocols use traditional approaches in social networks or ego networks to evaluate social metrics. These approaches have high spatiotemporal complexity due to transient user contacts and intermittently connected environment, and hence cannot be applied in large-scale opportunistic scenarios. 
	– It is necessary to develop a lightweight approach to exploiting human sociality for improving opportunistic transmission performance.