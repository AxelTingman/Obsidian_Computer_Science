#Kurs/Internet_of_Things #Kurs/Internet_of_Things/Föreläsning/4-6 

No general definition.

Applicaiton specific.
- If not, overlay is a more appropriate definition

At least two [[Peer|peers]].

Evry peer is is a client and a server.
- For same application
- Possibility of hierarchy.

Peers form an [[Overlay Communication|overlay network]].

## The new P2P paradigm
- P2P solutions has become pupular cecause of high speed internet connections. There has also been a power shoft from servers to en-users.
- P2P applications are a true revolution, aside from TCP/IP and the web.

## New P2P applications
- P2P applications capitalize on any resource from anybody. They can share CPU, bandwidth and storage with eachother.
	- BitTorrent, Emule, Gnutella
	- Skype, Google Talk, WhatsApp, Telegram, etc.
	- Pubilus

## P2P file sharing taxonomy
- Current taxonomy for P2P file sharing
	- Unstructured P2P: BitTorrent, Gnutella, KaZaA, etc.
	- Structured P2P: DHT (e.g. Chord, CAN, Pastry, Kedemilla, etc)
	- What is wrong?
		- Assume that P2P applications must be classified according to their content localization architecture.
- Propsed taxonomy for P2P:
	- Content localization
		- Unstructured
		- Structured
	- Content replication
		- Parallell download
		- File splitting
		- Piece selection
			- Rarest first, random, sequential, etc.
		- Peer selection
			- Choke algorithm, tit-for-tat, priority queue, etc.

## Measurement of P2P traffic
- Hard to perform P2P traffic measurements
- Known techniques
	- Port detection
		- Can be easily circumvented
	- Layer 7 inspection
		- Does not work with encrypted payload
		- Database of signatures. Hard to maintain.
	- Heuristics
		- Hard to identify, similar to other applications

## Why P2P is so efficient
- The service capacity grows exponentially with time
- With a flash crowd of *n* peers, the mean download time is in *log(n)* 
- The mean download time decreases in *1/(# of pieces)* when the *#* of pieces increases

## Model discussion
- Each peer has the same upload capacity
- No network bottleneck.
- Idealized peer selection strategy
	- Each peer always knows to which peer to send the content at a given time
	- Conflict resolution solved with global knowledge
	- No peer dynamics, i.e., *arrival*  and *departure* 
- Idealized piece selection.
	- Global knowledge
	- A peer is never blocked because it does nothave the right piece to upload.
- No advanced hypothesis: reciprocation, parallell download, etc.