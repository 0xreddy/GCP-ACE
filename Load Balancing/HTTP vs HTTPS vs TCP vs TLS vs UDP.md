HTTP vs HTTPS vs TCP vs TLS vs UDP
• Network Layer:
• IP (Internet Protocol): Transfer bytes. unreliable.
• Transport Layer:
• TCP (Transmission Control): Reliability > Performance
• TLS (Transport Layer Security): Secure TCP
• UDP (User Datagram Protocol): Performance > Reliability
• Application Layer:
HTTP(Hypertext Transfer Protocol): Stateless Request

Response Cycle
• HTTPS: Secure HTTP
SMTP: Email Transfer Protocol
![[Pasted image 20231018214448.png]]

• Most applications typically communicate at
application layer
• web apps/REST API(HTTP/HTTPS), Email Servers(SMTP), File
Transfers(FTP)
• All these applications use TCP/TLS at network layer(for
reliability)
• HOWEVER applications needing high performance
directly communicate at transport layer:
• Gaming applications ang live video streaming use UDP
(sacrifice reliability for performance)
• Objective: Understand Big Picture. Its 0K if you do
not understand all details.