# 04 — Rapid-PVST+ and EtherChannel

## Objective

Introduce Rapid-PVST+ for faster Layer-2 convergence and use STP priorities to control root placement. The multilayer switches are also connected through an LACP EtherChannel.

## Focus

- Rapid-PVST+
- STP root placement
- LACP EtherChannel
- Port-Channel verification

## Key configuration

ML-SW4 uses `channel-group 1 mode active`; ML-SW5 uses `channel-group 5 mode passive`.
