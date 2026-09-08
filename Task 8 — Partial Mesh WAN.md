Task 8 — Partial Mesh WAN

Task Info
Three routers, but only two of the three possible links actually exist — R1 and R3 aren't cabled directly. This showed me that OSPF doesn't need a direct 
connection to work out a route; as long as some path exists through the network, OSPF finds it and routes through the middle router.

Topology
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/5671414536c26ca49014ef93e884e98fc46c6c29/Screenshot%202026-09-08%20044132.png

R1 Config
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/5671414536c26ca49014ef93e884e98fc46c6c29/Screenshot%202026-09-08%20044211.png

R2 Config
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/5671414536c26ca49014ef93e884e98fc46c6c29/Screenshot%202026-09-08%20044248.png

R3 Config
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/5671414536c26ca49014ef93e884e98fc46c6c29/Screenshot%202026-09-08%20044324.png

Verification
display ospf peer
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/5671414536c26ca49014ef93e884e98fc46c6c29/Screenshot%202026-09-08%20044412.png

display ip routing-table
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/5671414536c26ca49014ef93e884e98fc46c6c29/Screenshot%202026-09-08%20044421.png

ping 10.120.100.6
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/5671414536c26ca49014ef93e884e98fc46c6c29/Screenshot%202026-09-08%20044429.png
