● The way Sensor data collection 
● A [[Publish-Subscribe|Pub/Sub]] approach will be adopted 
● Information to be intelligently performed in order to satisfy consumers requirements. 
● The [[IoT Data storage models|storage]] and organization of information 
● Similar to that adopted by Twitter: Each single sensor can be virtualized in the infrastructure of the service provider. 
● Each sensor individually identified and will generate a timeline of messages ( very similar to tweets) that will be passed to the consumer and store in the provider infrastructure. 
● Virtual Sensors can be grouped to set of sensors. 
● Much like Twitter allows for sending and receiving of private messages between users.
● Some of virtual sensor can be anonymized , the par of their timeline can be made available to [[Data fusion|aggregators]] who can use this information for running data mining algorithms to organize data or to extract information from different timelines 
● The aggregator has the need to access data in different “pages” ( e.g. to check data in different sensors timelines) in order to dynamically extract the relevant information. 
● Quit similar to Twitter possibly using Hadoop or similar solutions. 
● The coupling of Publish/Subscribe and Hadoop extended with cognitive platform capabilities seems to be a strong indication for a workable IoT architecture.

![[iot_architecture.png]]