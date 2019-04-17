The OSI model presents a **standard data flow architecture**, with **protocols** specified in such a way that the receiving layer at the **destination computer receives exactly the same object as sent by the matching layer at the source computer**.

**DATA FLOW:**  
+ The *sending process* passes data to the application layer. The *application layer* **attaches an application header(AH) and then passes the frame** to the presentation layer.
+ The *presentation layer* **can transform data in various ways, if necessary, such as by translating it and adding a header(PH).** It gives the result to the session layer. The presentation layer is not aware of which portion (if any) of the data received from the application layer is the application header and which portion is actually user data, because that information is irrelevant to the presentation layer's role.
+ The **process of adding headers(SH) is repeated from layer to layer until the frame reaches the data link layer**. There, in addition to a **data-link header(DH)**, **a data-link trailer(DT) is added**. The data-link trailer contains a checksum and padding if needed. This aids in frame synchronization. The frame is passed down to the *physical layer*, where it is transmitted to the receiving computer.
+ On the *receiving computer*, the **various headers and the data trailer are stripped off**  
`( DH + NH + TH + SH + PH + AH + DATA + DT)` one by one as the frame ascends the layers and finally reaches the receiving process.


| #        | LAYER        | PURPOSE           | PROTOCOL           | PORT  | CONCEPTS  |
| ------------- | ------------- |:-------------:|:-------------:| -----:| -----:|
| 1 | **P**hysical  | Media,signal and binary transmission . Manages the **reception and transmission** of the unstructured raw bit stream over a physical medium | - | - | This puts data onto the wire at the source computer and then it is sent to the destination computer
| 2 | **D**ata Link | Physical Addressing | ARP | - | Provides error-free transfer of **data frames** from one computer to another **over the physical layer**
| 3 | **N**etwork  | Path determination and logical addressing . Controls the **operation of the subnet** | IP(v4/v6) | - | **Network Address**: Identifier for **Group** of devices (All Binary 0's in Host portion)
|  |  |  | - | - | **Broadcast Address**: Identifier for **All** devices on network (All Binary 1's in Host portion)
|  |  |  | - | - | **Host Address**: Identifies **Unique** device on network (Anything except all Binary 0's/1's in Host portion)
|  |  |  | - | - | **CIDR Notation** , **IPv4** , **IPv6**
| 4 | **T**ransport  | E2E connection and reliability . Ensures that messages are **delivered error-free, in sequence, and with no loss or duplication.** |  TCP   | -  | **CONNECTION ORIENTED** , **3 Way Handshake** (SYN > SYN-ACK > ACK), **4 Way Disconnect** (FIN > FIN-ACK , FIN > FIN-ACK) ,**RESET**  (RST)
|  |  |  |  UDP | - | **CONNECTIONLESS**
| 5 | **S**ession  | InterHost communication |     |
| 6 | **P**resentation  | Data representation and encryption |     |
| 7 | **A**pplication  |  Transferring **Data**     | HTTP | 80 |Every Layer 7 Protocol has a Layer 4 component called a PORT Number which                                                                 identifies the Application Layer Protocol being used at Layer 4.
|  |  |  |  HTTPs | 443
|  |  |  Transferring **File** |  FTP  | 20 21 | Requires AUTH
|  |  |  |  sFTP | 22 | Requires AUTH
|  |  |  |  TFTP | 69 | NO AUTH
|  |  |  |  SMB | 445 | Requires AUTH
|  |  |  Transferring **Email** |  POP3  | 110/995 | **INCOMING**: Client fetches from server
|  |  |  |  IMAP | 143/993 | **INCOMING**: Client fetches from server
|  |  |  |  SMTP | 25/465 | **OUTGOING**: Client sends to server
|  |  |  Network Services |  DHCP  | - |
|  |  |  |  DNS | - | 
|  |  |  |  NTP | - | 
|  |  |  Authentication |  LDAP  | 389 | 
|  |  |  |  LDAPs | 636 | 
|  |  |  Network Management |  Telnet  | 23 | Requires AUTH
|  |  |  |  SSH | 22 | Requires AUTH
|  |  |  |  SNMP | - | 
|  |  |  |  RDP | 3389 |
|  |  |  Audio/Visual |  H.323  | 1720 | Video Conferencing
|  |  |  |  SIP | 5060/5061 | VOIP
