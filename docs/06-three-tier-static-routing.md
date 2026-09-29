# 06 — Three-Tier Architecture and Static Routing

## Objective

Add R1 and R2 and evolve the campus into a routed three-tier architecture.

## Routed transit networks

- ML-SW4 ↔ R1: `172.16.0.0/30`
- R1 ↔ R2: `172.16.0.4/30`
- R2 ↔ ML-SW5: `172.16.0.8/30`

## Routing

Static routes are used to provide deterministic reachability before introducing dynamic routing.
