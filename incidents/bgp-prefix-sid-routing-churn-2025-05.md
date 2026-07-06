---
title: "BGP Malformed Prefix-SID Attribute Causes Global Routing Churn"
date: 2025-05-15
incident_date: "2025-05-01"
type: "anomaly"
affected: ["Juniper Junos routers", "Arista routers", "Global BGP routing table", "Internet globally"]
impact: "BGP message rates spiked from ~30,000 to over 150,000 per second; widespread session resets caused significant routing instability worldwide."
description: "A corrupt BGP UPDATE containing a malformed prefix-SID attribute triggered automatic session resets in Juniper Junos and Arista implementations, cascading into global routing churn with BGP message rates increasing more than fivefold at peak."
tags: ["bgp", "prefix-sid", "juniper", "junos", "arista", "routing-churn", "bgp-session-reset", "segment-routing"]
---

In May 2025, a BGP UPDATE message containing a malformed prefix-SID attribute propagated across the internet, triggering a wave of automatic BGP session resets in routers running Juniper Junos and Arista EOS. The implementations' handling of the corrupt attribute caused them to tear down and re-establish BGP sessions, creating a cascade of BGP OPEN/NOTIFICATION messages across the global routing table.

At peak, BGP UPDATE message rates increased from roughly 30,000 to over 150,000 per second (more than a fivefold increase) as affected routers repeatedly re-established sessions and exchanged full table dumps. The incident caused significant routing instability and packet loss for traffic transiting affected networks, and prompted vendor patches to handle malformed attribute data more gracefully.
