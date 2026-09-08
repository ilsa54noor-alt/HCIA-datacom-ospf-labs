Task 5 — OSPF Cost Manipulation

Task Info
This showed me that OSPF doesn't pick paths by hop count — it uses cost, which by default is based on bandwidth. I set up two physical links between the same
two routers and manually assigned different costs to each, to see OSPF prefer the lower-cost path even though both paths physically existed.

Topology
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/012058756fbaa548ded3e85e3b32f5aec3c44766/Screenshot%202026-09-07%20140350.png

R1 Config
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/012058756fbaa548ded3e85e3b32f5aec3c44766/Screenshot%202026-09-07%20142523.png

R2 Config
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/012058756fbaa548ded3e85e3b32f5aec3c44766/Screenshot%202026-09-07%20142653.png

Verification
display ip routing-table
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/012058756fbaa548ded3e85e3b32f5aec3c44766/Screenshot%202026-09-07%20142740.png

display ospf peer
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/012058756fbaa548ded3e85e3b32f5aec3c44766/Screenshot%202026-09-07%20142818.png

ping 192.168.120.2
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/012058756fbaa548ded3e85e3b32f5aec3c44766/Screenshot%202026-09-07%20143030.png
