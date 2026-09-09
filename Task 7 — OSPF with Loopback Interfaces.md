Task 7 — OSPF with Loopback Interfaces

Task Info
This one was about observing OSPF's default behavior, not fixing it. Loopback interfaces are virtual and never physically go down, so they're commonly
used for stable router IDs — but by default, OSPF always advertises a loopback as a /32 host route, no matter what mask I actually configured. I left that
default behavior alone here, since that's literally the point being demonstrated.

Topology:

![Topology diagram](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/5f16507908e6f60b8e861e1eb45503197d4d84c0/Screenshot%202026-09-08%20042812.png)

R1 Config:

![R1 config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/5f16507908e6f60b8e861e1eb45503197d4d84c0/Screenshot%202026-09-08%20042854.png)

R2 Config:

![R2 config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/5f16507908e6f60b8e861e1eb45503197d4d84c0/Screenshot%202026-09-08%20042946.png)

Verification:

display ospf peer:

![OSPF peer table](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/5f16507908e6f60b8e861e1eb45503197d4d84c0/Screenshot%202026-09-08%20043032.png)

display ip routing-table:

![Routing table](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/5f16507908e6f60b8e861e1eb45503197d4d84c0/Screenshot%202026-09-08%20043037.png)

ping 1.1.1.1:

![Ping test](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/5f16507908e6f60b8e861e1eb45503197d4d84c0/Screenshot%202026-09-08%20043042.png)
