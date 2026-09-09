Task 10 — ISP–Enterprise Scenario

Task Info
This showed me how real networks handle the boundary between their own network and an ISP — never with OSPF running all the way out, just a static default route
on the edge router. R1 (the edge router) knows a static path to the ISP, and then uses default-route-advertise to inject that as a normal OSPF route so R2
(an internal router with zero static configuration) can still learn its way to the internet.

Topology:

![Topology diagram](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/becbe925ec2a2c166a25a02cffb8226a1b304197/Screenshot%202026-09-08%20074105.png)

ISP Config:

![ISP config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/becbe925ec2a2c166a25a02cffb8226a1b304197/Screenshot%202026-09-08%20074145.png)

R1 (Edge) Config:

![R1 config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/becbe925ec2a2c166a25a02cffb8226a1b304197/Screenshot%202026-09-08%20074225.png)

R2 (Internal) Config:

![R2 config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/becbe925ec2a2c166a25a02cffb8226a1b304197/Screenshot%202026-09-08%20074335.png)

Verification:

display ospf peer:

![OSPF peer table](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/becbe925ec2a2c166a25a02cffb8226a1b304197/Screenshot%202026-09-08%20074438.png)

display ip routing-table:

![Routing table](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/becbe925ec2a2c166a25a02cffb8226a1b304197/Screenshot%202026-09-08%20074449.png)

ping 8.8.8.8:

![Ping test](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/becbe925ec2a2c166a25a02cffb8226a1b304197/Screenshot%202026-09-08%20074458.png)
