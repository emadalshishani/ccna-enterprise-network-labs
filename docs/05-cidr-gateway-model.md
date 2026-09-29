# 05 — CIDR Addressing and Gateway Model

## Objective

Move the VLANs to separate CIDR-sized networks and establish the addressing model used by the later routed design.

## VLAN subnets

- VLAN 10: `192.168.10.0/25`
- VLAN 20: `192.168.20.0/26`
- VLAN 30: `192.168.30.0/27`

The addressing separates broadcast domains and prepares the topology for Layer-3 gateway functions.
