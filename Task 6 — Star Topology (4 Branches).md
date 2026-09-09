Task 6 — Star Topology (4 Branches)

Task Info
CORE connects to four branches, but the branches don't connect to each other. This showed me that OSPF neighbor relationships follow the actual cabling
— each branch only ever becomes a neighbor with CORE — but branches can still reach each other because OSPF calculates a path that passes through CORE.

Topology:

![Topology diagram](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/d7a786e66e395a5f59a43a56a738cbf4b789d5f6/Screenshot%202026-09-08%20010626.png)

CORE Config:

![CORE config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/d7a786e66e395a5f59a43a56a738cbf4b789d5f6/Screenshot%202026-09-08%20013311.png)

BR1 Config:

![BR1 config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/d7a786e66e395a5f59a43a56a738cbf4b789d5f6/Screenshot%202026-09-08%20013352.png)

BR2 Config:

![BR2 config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/d7a786e66e395a5f59a43a56a738cbf4b789d5f6/Screenshot%202026-09-08%20013433.png)

BR3 Config:

![BR3 config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/d7a786e66e395a5f59a43a56a738cbf4b789d5f6/Screenshot%202026-09-08%20013507.png)

BR4 Config:

![BR4 config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/d7a786e66e395a5f59a43a56a738cbf4b789d5f6/Screenshot%202026-09-08%20013536.png)

Verification:

display ospf peer:

![OSPF peer table](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/d7a786e66e395a5f59a43a56a738cbf4b789d5f6/Screenshot%202026-09-08%20022729.png)

display ip routing-table:

![Routing table](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/d7a786e66e395a5f59a43a56a738cbf4b789d5f6/Screenshot%202026-09-08%20022812.png)

ping 192.168.11.1:

![Ping test](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/d7a786e66e395a5f59a43a56a738cbf4b789d5f6/Screenshot%202026-09-08%20022844.png)
