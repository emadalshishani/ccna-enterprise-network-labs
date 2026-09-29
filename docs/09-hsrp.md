# 09 — HSRP First-Hop Redundancy

## Objective

Add first-hop redundancy for selected VLANs while retaining the routed three-tier and OSPF foundation.

## HSRP design

- VLAN 10 VIP: `192.168.10.124`; ML-SW4 priority `120`; ML-SW5 default priority.
- VLAN 20 VIP: `192.168.20.60`; ML-SW5 priority `120`; ML-SW4 priority `80`.
- Both sides use `preempt`.
- VLAN 30 continues without an HSRP VIP in this final file.

This creates VLAN-specific gateway preference rather than making one switch active for every VLAN.
