Task 3 — Campus Network (Multi-Area OSPF)

Task Info
This task introduced multi-area OSPF: R1 sits in Area 1, R3 sits in Area 2, and R2 is the ABR connecting both. I learned that OSPF has a strict rule —
non-backbone areas can't talk to each other directly, everything has to pass through Area 0. So even though R2 only physically connects to R1 and R3,
it still needed a separate interface (I used a loopback) placed specifically in Area 0, just to satisfy that backbone requirement.

Topology:
![Topology diagram](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/edb7851f6c3edad524b886db89158716665746db/Screenshot%202026-09-07%20133534.png)

R1 Config:
![R1 config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/edb7851f6c3edad524b886db89158716665746db/Screenshot%202026-09-07%20133600.png)

R2 (ABR) Config:
![R2 config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/edb7851f6c3edad524b886db89158716665746db/Screenshot%202026-09-07%20133814.png)

R3 Config:
![R3 config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/edb7851f6c3edad524b886db89158716665746db/Screenshot%202026-09-07%20133932.png)

Verification:

display ospf peer:
![OSPF peer table](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/edb7851f6c3edad524b886db89158716665746db/Screenshot%202026-09-07%20134124.png)

display ip routing-table:
![Routing table](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/edb7851f6c3edad524b886db89158716665746db/Screenshot%202026-09-07%20134202.png)

ping 172.16.120.130:
![Ping test](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/edb7851f6c3edad524b886db89158716665746db/Screenshot%202026-09-07%20134226.png)
