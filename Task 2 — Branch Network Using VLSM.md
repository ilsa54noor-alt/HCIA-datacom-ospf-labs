Task 2 — Branch Network Using VLSM

Task Info: This one was about VLSM — instead of using the same subnet size everywhere, I sized each subnet to how many hosts it actually needed (a /24 for HQ, /26 for BR1, /27 for BR2). Since I couldn't use extra switches or PCs, I simulated each branch's LAN using a loopback interface instead of a physical Ethernet port.

Topology:
![Topology diagram](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/d7833f7237e81e42965666770056980c2c0e433c/Screenshot%202026-09-03%20020613.png)

BR1 Config:
![BR1 config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/d7833f7237e81e42965666770056980c2c0e433c/Screenshot%202026-09-03%20054936.png)

HQ Config:
![HQ config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/d7833f7237e81e42965666770056980c2c0e433c/Screenshot%202026-09-03%20055254.png)

BR2 Config:
![BR2 config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/d7833f7237e81e42965666770056980c2c0e433c/Screenshot%202026-09-03%20055711.png)

Verification:

display ospf peer:
![OSPF peer table](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/d7833f7237e81e42965666770056980c2c0e433c/Screenshot%202026-09-03%20060000.png)

display ip routing-table:
![Routing table](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/d7833f7237e81e42965666770056980c2c0e433c/Screenshot%202026-09-03%20055808.png)

ping 10.120.0.1:
![Ping test](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/d7833f7237e81e42965666770056980c2c0e433c/Screenshot%202026-09-03%20055922.png)
