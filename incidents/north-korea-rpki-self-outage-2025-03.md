---
title: "North Korea Self-Inflicted RPKI Outage"
date: 2025-03-15
incident_date: "2025-03-01"
type: "rpki"
affected: ["North Korea", "DPRK BGP prefixes", "RPKI-validating networks globally"]
impact: "A misconfigured RPKI ROA caused North Korean BGP routes to be dropped by RPKI-validating networks worldwide, effectively isolating DPRK prefixes from much of the internet."
description: "North Korea created an invalid RPKI Route Origin Authorization (ROA), causing its own BGP routes to be rejected as RPKI-invalid by networks performing Route Origin Validation globally — a self-inflicted internet isolation event."
tags: ["rpki", "roa", "north-korea", "dprk", "route-origin-validation", "bgp", "self-inflicted"]
---

In early 2025, North Korea (DPRK) misconfigured an RPKI Route Origin Authorization (ROA), causing the country's BGP route announcements to be marked as RPKI-invalid. Networks performing Route Origin Validation (ROV) dropped the affected prefixes, removing North Korean internet infrastructure from the routing tables of a large portion of the global internet.
