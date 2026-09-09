Task 9 — Multi-Area OSPF + Summarization

Task Info
This builds on Task 3, but adds summarization at the area boundary. R3 has four contiguous LANs in Area 2, and R2 (the ABR) summarizes them into one /22 
before they cross into Area 0. Without this, every individual subnet inside Area 2 would flood into Area 0 and Area 1, which doesn't scale well in a real network.

Topology
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/4d76119cc08ac0dee2e30988d7df4ebdd86e0785/Screenshot%202026-09-08%20054112.png

R1 Config
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/4d76119cc08ac0dee2e30988d7df4ebdd86e0785/Screenshot%202026-09-08%20071210.png

R2 (ABR) Config
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/4d76119cc08ac0dee2e30988d7df4ebdd86e0785/Screenshot%202026-09-08%20071241.png

R3 Config
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/4d76119cc08ac0dee2e30988d7df4ebdd86e0785/Screenshot%202026-09-08%20071546.png

Verification
display ip routing-table
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/4d76119cc08ac0dee2e30988d7df4ebdd86e0785/Screenshot%202026-09-08%20071626.png

display ospf peer
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/4d76119cc08ac0dee2e30988d7df4ebdd86e0785/Screenshot%202026-09-08%20072026.png
