The TCP/IP model, contains **4 layers** and protocols at each layer.  
**N**etworkAccess **I**nternet **T**ransport **A**pplication
+ Different encapsulation types exist at the different layers, such as **packets at the Network layer**.
+ TCP operates at the Transport layer and IP operates at the Network layer.
+ All computers and devices participating in a TCP/IP network require an IP address, subnet mask, and default gateway.
+ There are a few ports that should be remembered including: 53 (DNS), 80 (HTTP), 25 (SMTP), 110 (POP3).

**DATA ENCAPSULATION**:  
`Packet (L3) > Frame (L2)`


Transport Control Protocol (TCP)
+ When the *application layer* needs to send large amount of data, it sends the data down to the *transport layer* for TCP or UDP to transport it across the network. 
+ TCP first **sets up a virtual-circuit** between the source and the destination in a process called **three-way handshake**.  
`SYN >`  
`< SYN-ACK`  
`ACK >`
+ Then it **breaks down the data into chunks called segments (MTU = Max Transmission Unit)**, adds a header to each segment and sends them to the *Internet layer*.
+ After all data has been transferred, the source initiates a **four-way handshake** to close the session.  
`FIN >`  
`< ACK`  
`< FIN`  
`ACK >`
