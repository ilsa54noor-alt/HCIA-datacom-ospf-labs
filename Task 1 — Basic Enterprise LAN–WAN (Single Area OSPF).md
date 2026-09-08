Task 1 — Basic Enterprise LAN–WAN (Single Area OSPF)

What this task is about:
This is the simplest possible OSPF setup — two routers, each with a LAN and a WAN link, both in Area 0. The point was to see OSPF actually work: once 
I put the right interfaces into the right network statements, the two routers found each other and started exchanging routes automatically, without me
manually typing any route entries. That's the core idea of a dynamic routing protocol — I tell it which interfaces to run OSPF on, and it figures out the rest.

Topology
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/ad3c27623c79328ea96244509cf1921f50b5175b/Screenshot%202026-09-07%20130054.png

R1 Config
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/ad3c27623c79328ea96244509cf1921f50b5175b/Screenshot%202026-09-07%20130236.png

R2 Config
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/ad3c27623c79328ea96244509cf1921f50b5175b/Screenshot%202026-09-07%20130333.png

Verification:
display ospf peer
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/ad3c27623c79328ea96244509cf1921f50b5175b/Screenshot%202026-09-07%20130417.png

display ip routing-table
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/ad3c27623c79328ea96244509cf1921f50b5175b/Screenshot%202026-09-07%20130443.png

ping 192.168.120.65
https://github.com/ilsa54noor-alt/HCIA-datacom-ospf-labs/blob/ad3c27623c79328ea96244509cf1921f50b5175b/Screenshot%202026-09-07%20130614.png
