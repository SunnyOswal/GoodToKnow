| #        | LAYER        | PURPOSE           | PROTOCOL           | PORT  | Notes  |
| ------------- | ------------- |:-------------:|:-------------:| -----:| -----:|
| 1 | **P**hysical  |  |  |
| 2 | **D**ata Link    |       |    |
| 3 | **N**etwork  |       |     |
| 4 | **T**ransport  |       |     |
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
|  |  |  Auio/Visual |  H.323  | 1720 | Video Conferencing
|  |  |  |  SIP | 5060/5061 | VOIP
