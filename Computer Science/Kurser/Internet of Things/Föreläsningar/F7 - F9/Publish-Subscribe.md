#Kurs/Internet_of_Things #Kurs/Internet_of_Things/Föreläsning/7-9 

- A model for messaging between two applications 
● Senders, publishers, do not send message directly to the receivers, subscribers 
● Publisher publishes messages to the event dispatcher/Message broker/Queue manager 
● Subscriber(s) registers with the event dispatcher and gets notified when message is available

![[publish_subscribe.png]]


## Types 
● Mainly two types – topic-based – content-based 
● Topic-based – all topics connected to a subject are notified to a subscriber 
● Content-based – subscribers have the freedom to choose the events of interest – thus enjoying more flexibility and usefulness than the topic-based model can offer. 
● Mix of both is common nowadays

## Examples
- [[MQTT]]
- [[DCXP]]
- [[CoAP]]