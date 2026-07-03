---
title: "BGP Unknown Attribute 28 Routing Disruption"
date: 2023-06-11
incident_date: "2023-06-06"
type: "outage"
affected: ["Global BGP routing", "Multiple ISPs and networks"]
impact: "Widespread BGP session resets and routing instability across the Internet; multiple ISPs reported peering session failures due to malformed attribute handling."
source_url: "https://labs.ripe.net/author/emileaben/unknown-attribute-28-a-source-of-entropy-in-interdomain-routing/"
description: "A BGP UPDATE message containing an unrecognized optional transitive attribute (type code 28) propagated through the global routing system, causing routers that did not handle it correctly to reset BGP sessions, resulting in widespread routing instability."
tags: ["bgp", "routing", "attribute", "optional-transitive", "internet-routing", "stability", "protocol"]
---

In early June 2023, an unusual BGP UPDATE message containing an unknown optional transitive attribute (type code 28) began propagating through the global Internet routing system. Per BGP protocol rules (RFC 4271), optional transitive attributes that a router does not recognize should be passed on to BGP neighbors with the partial bit set. However, some router implementations did not handle this correctly, instead resetting BGP peering sessions upon encountering the attribute.

The cascading effect caused widespread BGP session flapping and routing instability as the malformed or unexpected attribute propagated. Multiple ISPs and network operators reported losing peering sessions and experiencing routing disruptions.

RIPE NCC's analysis documented the event as an example of how seemingly minor protocol edge cases can propagate through the tightly coupled global routing system. The incident highlighted implementation differences in how BGP speakers handle unknown attributes and the importance of graceful handling of optional transitive attributes under RFC specifications.
