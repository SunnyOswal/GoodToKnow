| #        | LAYER        | PURPOSE           | PROTOCOL           | PORT  | CONCEPTS  |
| ------------- | ------------- |:-------------:|:-------------:| -----:| -----:|
| 1 | **P**hysical  |  |  |
| 2 | **D**ata Link    |       |    |
| 3 | **N**etwork  |       |     |  | **Network Address**: Identifier for **Group** of devices (All Binary 0's in Host portion)
|  |  |  |   |  | **Broadcast Address**: Identifier for **All** devices on network (All Binary 1's in Host portion)
|  |  |  |   |  | **Host Address**: Identifies **Unique** device on network (Anything except all Binary 0's/1's in Host portion)
| 4 | **T**ransport  |       |  TCP   | -  | **CONNECTION ORIENTED** , **3 Way Handshake** (SYN > SYN-ACK > ACK), **4 Way Disconnect** (FIN > FIN-ACK , FIN > FIN-ACK) ,**RESET**  (RST)
|  |  |  |  UDP | - | **CONNECTIONLESS**
| 5 | **S**ession  |       |     |
| 6 | **P**resentation  |       |     |
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
