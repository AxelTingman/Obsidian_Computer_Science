#Kurs/Internet_of_Things #Kurs/Internet_of_Things/Föreläsning/7-9 

– More flexibility and power to subscribers, by allowing more expression in arbitrary/customized query over the contents of the event. 
– Event [[Publish-Subscribe|publication]] by a key/value attribute pair, and subscriptions specify filters using a explicit subscription language. 
– E.g. Notify me of all stock quotes of IBM from New York stock exchange if the price is greater than 150

– Added complexity in matching an event to subscriptions. (Implementation: Subscription arranged in a matching tree, where each node is a partial condition. 
– However, more precision is provided and event routing is easier