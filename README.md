# CCNA Enterprise Network Labs

A progressive Cisco Packet Tracer lab series documenting the evolution from basic campus switching to a routed three-tier enterprise design.

The labs are intentionally **sequential**. Each stage builds on the previous one and documents the evolution of the same environment.

## Lab progression

| # | Lab | Main topics | Documentation | Packet Tracer |
|---|---|---|---|---|
| 01 | Basic Campus Topology | Basic switching, connectivity | [Lab 01](docs/01-basic-campus.md) | [Open file](packet-tracer/CCNA%20First%20Topology%20Lab.pkt) |
| 02 | Two-Tier Campus Topology | Access/distribution design | [Lab 02](docs/02-two-tier.md) | [Open file](packet-tracer/CCNA%20First%20Topology%20Lab%20two%20Tier.pkt) |
| 03 | VLAN Segmentation | VLANs, 802.1Q trunking | [Lab 03](docs/03-vlans.md) | [Open file](packet-tracer/CCNA%20First%20Topology%20Lab2-%20two%20Tier%20Vlans.pkt) |
| 04 | Rapid-PVST+ and EtherChannel | STP, RPVST+, LACP | [Lab 04](docs/04-rpvst-etherchannel.md) | [Open file](packet-tracer/CCNA%20First%20Topology%20Lab3-%20two%20Tier%20-SPT-RPVST.pkt) |
| 05 | CIDR and Gateway Model | Subnetting, CIDR, inter-VLAN routing | [Lab 05](docs/05-cidr-gateway-model.md) | [Open file](packet-tracer/CCNA%20First%20Topology%20Lab4-%20two%20Tier%20-Vlan%20and%20Router-On-Stick%20CIDR%20first%20step.pkt) |
| 06 | Three-Tier and Static Routing | Core/distribution/access, static routing | [Lab 06](docs/06-three-tier-static-routing.md) | [Open file](packet-tracer/CCNA%20First%20Topology%20Lab5-%20Three%20Tiers%20Static%20Route.pkt) |
| 07 | OSPF Area 0 | Neighbors, LSDB, routes, cost | [Lab 07](docs/07-ospf.md) | [Open file](packet-tracer/CCNA%20First%20Topology%20Lab6-%20Three%20Tier%20OSPF.pkt) |
| 08 | Floating Static and IPv6 | Administrative distance, backup routes, IPv6 | [Lab 08](docs/08-floating-static-ipv6.md) | [Open file](packet-tracer/CCNA%20First%20Topology%20Lab7-%20Three%20Tier%20-%20FloatingStaticRoute_IPv6StaticRoute.pkt) |
| 09 | HSRP First-Hop Redundancy | FHRP, priority, preemption | [Lab 09](docs/09-hsrp.md) | [Open file](packet-tracer/CCNA%20First%20Topology%20Lab8-%20Three%20Tier%20-%20HSRP.pkt) |

## Skills demonstrated

### Switching
- VLAN segmentation
- 802.1Q trunking
- Rapid-PVST+
- STP root placement
- EtherChannel using LACP
- Access/distribution switching concepts

### Routing
- Inter-VLAN routing
- Multilayer switching
- CIDR and subnetting
- IPv4 static routing
- Floating static routes
- OSPF Area 0
- IPv6 addressing and static routing

### High availability
- HSRP
- Active/standby gateway roles
- HSRP priority and preemption
- Redundant Layer 3 paths
- Route failover concepts

### Verification and troubleshooting

The labs include practical verification with commands such as:

<code>show interfaces status</code>  
<code>show interfaces trunk</code>  
<code>show spanning-tree</code>  
<code>show etherchannel summary</code>  
<code>show ip interface brief</code>  
<code>show ip route</code>  
<code>show ip route ospf</code>  
<code>show ip ospf neighbor</code>  
<code>show ip ospf database</code>  
<code>show standby</code>  
<code>show ipv6 route</code>  
<code>ping</code>  
<code>traceroute</code>

## Addressing overview

| Segment | Network | Purpose |
|---|---|---|
| VLAN 10 | 192.168.10.0/25 | User VLAN |
| VLAN 20 | 192.168.20.0/26 | User VLAN |
| VLAN 30 | 192.168.30.0/27 | User VLAN |
| R1 ↔ ML-SW4 | 172.16.0.0/30 | Routed transit |
| R1 ↔ R2 | 172.16.0.4/30 | Routed transit |
| R2 ↔ ML-SW5 | 172.16.0.8/30 | Routed transit |
| Loopbacks | 10.255.0.0/32 | Router/switch loopbacks |
| IPv6 R1 ↔ R2 | 2001::/64 | IPv6 transit |

See the complete [addressing plan](docs/addressing.md).

## Repository structure

<pre>
ccna-enterprise-network-labs/
├── README.md
├── docs/
│   ├── README.md
│   ├── 01-basic-campus.md
│   ├── 02-two-tier.md
│   ├── 03-vlans.md
│   ├── 04-rpvst-etherchannel.md
│   ├── 05-cidr-gateway-model.md
│   ├── 06-three-tier-static-routing.md
│   ├── 07-ospf.md
│   ├── 08-floating-static-ipv6.md
│   ├── 09-hsrp.md
│   ├── addressing.md
│   └── topology.md
└── packet-tracer/
    ├── README.md
    └── *.pkt
</pre>

## How to use

1. Install a compatible version of Cisco Packet Tracer.
2. Start with Lab 01.
3. Open each Packet Tracer file in sequence.
4. Read the matching documentation.
5. Run the verification commands documented for each stage.
6. Compare later stages with earlier stages to understand the design evolution.

## Design progression

<pre>
Basic Switching
      ↓
Two-Tier Campus
      ↓
VLAN Segmentation
      ↓
RPVST+ + EtherChannel
      ↓
CIDR + Inter-VLAN Routing
      ↓
Three-Tier Architecture
      ↓
Static Routing
      ↓
OSPF Area 0
      ↓
Floating Static + IPv6
      ↓
HSRP First-Hop Redundancy
</pre>

## Documentation

- [Documentation index](docs/README.md)
- [Topology overview](docs/topology.md)
- [Addressing plan](docs/addressing.md)

> The Packet Tracer files are working lab artifacts. Later files intentionally retain earlier configuration and experiments because the series documents the evolution of the same environment.
