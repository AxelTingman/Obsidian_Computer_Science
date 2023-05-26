#Kurs/Internet_of_Things #Kurs/Internet_of_Things/Föreläsning/11-12 

Data streaming techniques process incoming data through a sequence of transformation based on Common SQL operators. 

● The Complex Event processing model views the information in the streams as events in the physical world. 
● Systems for event processing and in particular event recognition (event pattern matching) accept a stream of time-stamped, simple or low-level events as input. 
● A low-level event is the result of applying a computational derivation process to some other event, such as an event coming from a sensor. 
● Using low-level events as input, (complex) event processing systems identify composite or high- level events of interest. 
● They are also collections of events that satisfy certain patterns. 
● SASE (a complex event processing system) and other new query evaluation model is designed for processing pattern matching over RFID streams, employing a new type of automaton that comprises a nondeterministic finite automaton (NFA) and a match buffer, named NFA. 
● Nested CEP language called NEEL is proposed to support the flexible nesting of AND, OR, Negation and SEQ operators at any level

![[complex_event_processing.png]]

## Semantic CEP
● Semantic Complex Event Processing 
	– Semantic models of events can improve event processing quality by using event meta- data in combination with ontologies and rules (i.e., knowledge bases). 
	– The [[Data fusion|fusion]] of background knowledge with data from an event stream can help the event processing engine to know more about incoming events and their relationships to other related concepts. 
● Semantic event enrichment 
	– The usage of background knowledge about events and their relations to other concepts in the application domain can improve the expressiveness and flexibility of CEP systems. – The process of reducing information incompleteness is called event enrichment. 
	– Several challenges are identified for event enrichment, including determination of the enrichment source, retrieval of information items from the enrichment source, finding complementary information for an event in the enrichment source and fusion of complementary information with the event. 
● Approximate semantic matching 
	– To achieve approximate matching, semantic selection and inexact selection are used. 
	– The semantic selection evaluates pattern constraints based on the semantic equivalence of attribute meanings captured by the event ontology instead of syntactic identical attribute values. 
	– The inexact selection selects events and allows a limited number of mismatches to detect relevant patterns.
	
![[knowledge-based_event_processing.png]]