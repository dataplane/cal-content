---
title: "TCPShield Tokyo Datacenter Hardware Failure"
date: 2026-07-14
incident_date: "2026-07-06"
incident_end: "2026-07-07"
type: "outage"
affected: ["TCPShield", "Tokyo", "Asia Network"]
impact: "Suspected motherboard failure took a Tokyo node offline; traffic was automatically rerouted to Seoul with no service interruption to tunnel and proxy services."
source_url: "https://status.tcpshield.com/incidents/c662h70v873r"
description: "A suspected motherboard failure at TCPShield's Tokyo datacenter left a node unresponsive from July 6-7, 2026; traffic failed over to Seoul until hardware was replaced."
tags: ["tcpshield", "tokyo", "hardware-failure", "outage", "asia"]
---

TCPShield's Tokyo datacenter node became unresponsive to power attempts starting July 6, 2026 at 16:42 UTC, due to a suspected motherboard failure. Traffic was automatically redirected to Seoul, with TCPShield reporting no service interruption to tunnel and proxy services during the failover.

The datacenter completed a hardware replacement and fully restored the Tokyo node by July 7 at 14:00 UTC, rerouting player traffic back to Tokyo.
