---
title: "Orange Spain BGP Hijack via RIPE NCC Account Breach"
date: 2024-01-07
incident_date: "2024-01-03"
type: "security"
affected: ["Orange Spain", "AS12479", "RIPE NCC", "Spain"]
impact: "Orange Spain's routing was disrupted for approximately 2.5 hours as malicious ROAs redirected traffic away from the operator's prefixes; significant Internet disruption for Spanish customers."
source_url: "https://www.ripe.net/publications/news/ripe-ncc-access-security-breach-investigation"
description: "An attacker gained access to Orange Spain's RIPE NCC account and created fraudulent RPKI Route Origin Authorizations (ROAs), causing route origin validation to reject legitimate Orange Spain prefixes and disrupting routing for the operator's customers."
tags: ["bgp", "rpki", "roa", "ripe-ncc", "orange-spain", "hijack", "routing-security", "spain", "as12479"]
---

On January 3, 2024, an attacker who had obtained credentials for Orange Spain's RIPE NCC portal account created malicious RPKI Route Origin Authorizations (ROAs) for Orange Spain's prefixes (AS12479). By associating the prefixes with a different, invalid origin AS, the attacker caused RPKI-validating routers around the world to mark Orange Spain's legitimate route announcements as "Invalid" and drop them.

The resulting routing disruption lasted approximately 2.5 hours and caused widespread Internet connectivity problems for Orange Spain's customers. The attacker reportedly used the handle "Ms_Snow_OwO" and taunted the operator on social media.

RIR account access translates directly into the ability to modify routing security configurations affecting global reachability. RIPE NCC subsequently accelerated work on mandatory MFA for all accounts with routing-related access.
