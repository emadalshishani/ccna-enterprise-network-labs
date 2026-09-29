# 08 — Floating Static Route and IPv6 Static Routing

## Objective

Add an IPv4 floating static route for backup reachability and introduce IPv6 addressing plus static IPv6 routing.

## IPv4 backup

R1 contains a primary static route toward `192.168.20.2/32` through `172.16.0.2` and a higher-distance backup through `172.16.0.6`.

## IPv6

R1/R2 use `2001::/64` on the inter-router link, with `2000::1/128` and `2002::2/128` loopback-style addresses. Static IPv6 routes are configured in both directions.
