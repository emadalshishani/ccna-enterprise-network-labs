# Topology Reference

## Final three-tier shape

```text
                   R1 -------- R2
                  /              \\
              ML-SW4 ======== ML-SW5
                / | \\          / | \\
              SW1 SW2 SW3    access segments
               |   |   |       |
             endpoints in VLAN 10 / 20 / 30
```

The two multilayer switches provide SVI gateway functions, Layer-2 resiliency, and routed uplinks. R1/R2 provide the routed upstream/transit portion of the later labs.

`====` represents the logical EtherChannel between ML-SW4 and ML-SW5.
