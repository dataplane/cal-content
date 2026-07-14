---
title: "TCP Reachability Degradation at Several TLD Nameservers"
date: 2026-07-14
incident_date: "2026-07-05"
incident_end: "2026-07-11"
type: "dns"
affected: ["e164.arpa (ns3.lacnic.net)", ".ml TLD (a.nic.ml)", ".om TLD"]
impact: "RIPE DNSMON recorded elevated TCP query failure rates against individual authoritative nameservers for e164.arpa, .ml, and .om during the week."
source_url: "https://dnsmon.ripe.net/e164.arpa?start=2026-07-05T00:00:00.000Z&end=2026-07-11T23:59:00.000Z&zone=e164.arpa.&protocol=tcp&ipVersion=4"
description: "RIPE DNSMON flagged TCP reachability degradation over July 5-11, 2026 at three separate TLD nameservers: e164.arpa's ns3.lacnic.net (IPv4), the .ml zone's a.nic.ml (IPv4), and the .om zone (both IP versions), each independently monitored via RIPE Atlas probes."
tags: ["dns", "dnsmon", "ripe-ncc", "tld", "e164.arpa", "ml", "om", "monitoring"]
---

RIPE NCC's DNSMON, which tracks authoritative nameserver reachability from RIPE Atlas probes worldwide, recorded elevated TCP query failure rates at three unrelated TLD nameservers during the week of July 5-11, 2026:

- **e164.arpa** — degraded TCP/IPv4 reachability at ns3.lacnic.net
- **.ml** — a TCP/IPv4 outage at a.nic.ml
- **.om** — TCP degradation across both IPv4 and IPv6

Each of these reflects a single nameserver's reachability within its zone's broader anycast or unicast nameserver set, rather than a full zone-wide resolution failure. No public incident reports from the respective operators (LACNIC, Mali's ANTIM, and Oman's TRA) accompanied these monitoring signals as of publication.
