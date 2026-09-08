Task 4 — Route Summarization (Supernetting)

Task Info 
This is the opposite of VLSM — instead of splitting one block into smaller subnets, I took four separate, contiguous /24 subnets and summarized them into a
single /22 announcement. The point was reducing how many routing entries the rest of the network has to store — instead of learning 4 routes, R0 only learns 1.

Topology
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/a670bf6ef57edbc045cf04ece83d2e9f6cb992aa/Screenshot%202026-09-08%20112902.png

R1 Config
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/a670bf6ef57edbc045cf04ece83d2e9f6cb992aa/Screenshot%202026-09-08%20112508.png

R2 Config
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/a670bf6ef57edbc045cf04ece83d2e9f6cb992aa/Screenshot%202026-09-08%20112518.png

Verification:
display ospf peer
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/a670bf6ef57edbc045cf04ece83d2e9f6cb992aa/Screenshot%202026-09-08%20112550.png

display ip routing-table
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/a670bf6ef57edbc045cf04ece83d2e9f6cb992aa/Screenshot%202026-09-08%20112638.png
