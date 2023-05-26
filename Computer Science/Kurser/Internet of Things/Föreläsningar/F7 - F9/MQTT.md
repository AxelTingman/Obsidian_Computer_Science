#Kurs/Internet_of_Things #Kurs/Internet_of_Things/Föreläsning/7-9 

● Stands for **M**essage **Q**ueuing **T**elemetry **T**ransport 
● Is a lightweight messaging transport 
	– CONNECT, PUBLISH, SUBSCRIBE, UNSUBSCRIBE, DISCONNECT ([[Publish-Subscribe]])
● IoT enabler protocol 
● Useful for connections with remote locations where a small code footprint is required and/or network bandwidth

## Architecture
![[mqtt_architecture.png]]

## How does it work? 
● Central concept in MQTT to dispatch messages are topics 
● A topic is a simple string – Can have hierarchy – Ex: house/living-room/temperature. 
● Sensors send data to the broker, which resides in the cloud, and broker subsequently notifies the subscribers

## Replacing [[HTTP]]
 MQTT provides support fro transactions and an event-orinted paradigm, engineered around wireless transmision.
 - Reliably and securely completing mobile business transactions over unreliable networks.
 - Pushing information over unreliable networks
 - Transmitting information one-to-many
 - Listening for events whenever they happen
 - Distributing minimal packets of data in huge volumes.

## Keep Alive
- Protocol includes support for client and server to detect failed connections
	-  At connection time, a keep alive can be specified.
- If client does not not recieve PINGRESP after the keep alive time has passed after sending the request, the connection is failed.
- Maximum keep alive interval of 18 hours.
	- Can specify a value of 0 to disable keep alive.

## Last Will & Testament
- During connection, a *Will* message and topic can be specified.
	- Abnormal disconnections will cause WMQ to publish the message.
	- Clean disconnects will not cause the message to publish.
- Can set the message as retained.
	- Message is published to a subscriber when registering
- Useful to report the connection status of a client.
	- Will message is a retained *down*
	- Upon connection, client publishes a retained *up* message.

![[mqtt_life 1.png]]
![[mqtt_life2.png]]

## MQTT Clients and API
- The published wire format is useful when implementing very lightweight sensors.
- However, a prebuilt client library simplifies MQTT programming.
	- No need to know the bits and butes flowing over the wire.
	- No need to code thread management for background processing.
	- Makes code more maintainable.
- Open source clients availablein Eclipse Paho project
	- Java, C and JavaScript
- Clients for Other languages are available (see `mqtt.org/software`)
	- C++, Delphi, Erlang, Lua, -Net, Objective-C, PERL, PHP, Python, Ruby.