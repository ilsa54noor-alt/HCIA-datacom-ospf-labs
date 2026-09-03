HCIA Datacom — Task 2: Branch Network Using VLSM (OSPF)

Objective:
Configure a 3-router star topology (BR1 — HQ — BR2) using VLSM-sized
subnets, with loopback interfaces simulating each site's LAN.

Topology:
![Topology diagram](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/e0e32462786b17223f1dc8cfb38843a8d93ae0ab/Screenshot%202026-09-03%20020613.png)

BR1 config log:
![BR1 config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/c634e2db0cc1ceeb968f8d030cea81c53dd8a87f/Screenshot%202026-09-03%20054936.png)

BR2 config log:
![BR2 config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/c634e2db0cc1ceeb968f8d030cea81c53dd8a87f/Screenshot%202026-09-03%20055254.png)

HQ config log:
![HQ config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/c634e2db0cc1ceeb968f8d030cea81c53dd8a87f/Screenshot%202026-09-03%20055711.png)

display ospf peer:
![OSPF peer table](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/c634e2db0cc1ceeb968f8d030cea81c53dd8a87f/Screenshot%202026-09-03%20060000.png)

display ip routing-table:
![Routing table](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/c634e2db0cc1ceeb968f8d030cea81c53dd8a87f/Screenshot%202026-09-03%20055808.png)

ping 10.120.0.1:
![Ping test](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/c634e2db0cc1ceeb968f8d030cea81c53dd8a87f/Screenshot%202026-09-03%20055922.png)

## Problem 1: Mismatched WAN subnets
Initially assigned WAN IPs from different /30 blocks on the two ends
of the same cable (e.g. BR1 = 10.120.10.5/30, HQ = 10.120.10.2/30).
Result: the link never came up — two ends of one cable must fall in
the same /30 block to be recognized as directly connected.
**Fix:** recalculated both WAN links so each pair shares one /30
block (10.120.10.0/30 for BR1–HQ, 10.120.10.4/30 for HQ–BR2).

## Problem 2: Loopback interfaces always advertised as /32
Loopback interfaces representing each site's LAN (/26, /24, /27)
showed up in OSPF as /32 host routes on other routers, hiding the
actual VLSM sizing.
**First attempt:** `ospf network-type p2p` — did not work; routing
table still showed /32 after applying it.
**Root cause:** p2p fixes this on Cisco IOS, but Huawei VRP requires
`ospf network-type broadcast` (or nbma) to advertise a loopback's
real configured mask.
**Fix:** applied `ospf network-type broadcast` on all three loopbacks.
Confirmed via `display ip routing-table` — masks now show correctly.

## Final Verification
- `display ospf peer` on HQ — 2 neighbors, both Full state
- `display ip routing-table` on HQ and BR1 — correct /26, /24, /27
  masks visible (not /32)
- `ping 10.120.0.1` from BR1 — success, proves the path BR1→HQ works
