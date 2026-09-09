Task 1 — Basic Enterprise LAN–WAN (Single Area OSPF)

What this task is about:
This is the simplest possible OSPF setup — two routers, each with a LAN and a WAN link, both in Area 0. The point was to see OSPF actually work: once
I put the right interfaces into the right network statements, the two routers found each other and started exchanging routes automatically, without me
manually typing any route entries. That's the core idea of a dynamic routing protocol — I tell it which interfaces to run OSPF on, and it figures out the rest.

Topology:

![Topology diagram](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/ad3c27623c79328ea96244509cf1921f50b5175b/Screenshot%202026-09-07%20130054.png)

R1 Config:

![R1 config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/ad3c27623c79328ea96244509cf1921f50b5175b/Screenshot%202026-09-07%20130236.png)

R2 Config:

![R2 config log](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/ad3c27623c79328ea96244509cf1921f50b5175b/Screenshot%202026-09-07%20130333.png)

Verification:

display ospf peer:

![OSPF peer table](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/ad3c27623c79328ea96244509cf1921f50b5175b/Screenshot%202026-09-07%20130417.png)

display ip routing-table:

![Routing table](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/ad3c27623c79328ea96244509cf1921f50b5175b/Screenshot%202026-09-07%20130443.png)

ping 192.168.120.65:

![Ping test](https://raw.githubusercontent.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/ad3c27623c79328ea96244509cf1921f50b5175b/Screenshot%202026-09-07%20130614.png)
