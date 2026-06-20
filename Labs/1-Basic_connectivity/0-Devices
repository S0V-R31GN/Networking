Network Devices — Switches, Routers, Hubs

Switches (Layer 2)

Switches bundle local PCs together into a LAN.

PCs inside the same LAN (e.g. Lab 1) can talk to each other instantly through their switch using hardware MAC addresses. They don't need the router for local communication — the switch handles it entirely on its own.

Routers (Layer 3)

Routers sit at the network border and connect separate LANs together.

How traffic actually decides to leave the LAN:
It's the sending PC, not the switch, that decides whether a destination is local or remote — by comparing the destination IP against its own subnet mask.


If the destination is local → PC addresses the frame directly to the destination PC's MAC.
If the destination is remote (e.g. a PC in Lab B) → PC addresses the frame to the router's MAC address (its default gateway) from the very start, even though that frame still physically flows across Switch 1 to get there.


So the actual path is:


PC in Lab 1 checks the destination IP → sees it's a different subnet → sends the frame addressed to the router's MAC.
Switch 1 forwards that frame out whichever port the router's MAC lives on (it's just matching MAC → port, same as any other frame).
Router receives it, makes a Layer 3 routing decision, forwards it toward Lab B.
Switch 2 forwards it to the destination PC's port.


The switch never "realizes" the destination is in a different room — it has no concept of IP, subnets, or rooms. That logic lives entirely in the PC (deciding where to address the frame) and the router (deciding how to route between subnets).

Hubs

As of 2026, hubs are essentially never implemented in real networks — obsolete and insecure. A hub has no memory or addressing intelligence: it broadcasts every incoming frame to all ports, meaning any connected device can see all traffic on the hub (no isolation, easy to sniff).
