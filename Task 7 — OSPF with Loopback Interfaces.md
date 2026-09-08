Task 7 — OSPF with Loopback Interfaces

Task Info
This one was about observing OSPF's default behavior, not fixing it. Loopback interfaces are virtual and never physically go down, so they're commonly 
used for stable router IDs — but by default, OSPF always advertises a loopback as a /32 host route, no matter what mask I actually configured. I left that 
default behavior alone here, since that's literally the point being demonstrated.

Topology
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/5f16507908e6f60b8e861e1eb45503197d4d84c0/Screenshot%202026-09-08%20042812.png

R1 Config
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/5f16507908e6f60b8e861e1eb45503197d4d84c0/Screenshot%202026-09-08%20042854.png

R2 Config
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/5f16507908e6f60b8e861e1eb45503197d4d84c0/Screenshot%202026-09-08%20042946.png

Verification
display ospf peer
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/5f16507908e6f60b8e861e1eb45503197d4d84c0/Screenshot%202026-09-08%20043032.png

display ip routing-table
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/5f16507908e6f60b8e861e1eb45503197d4d84c0/Screenshot%202026-09-08%20043037.png

ping 1.1.1.1
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/5f16507908e6f60b8e861e1eb45503197d4d84c0/Screenshot%202026-09-08%20043042.png
