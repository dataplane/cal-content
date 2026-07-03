---
title: "RIPE NCC Hosted RPKI Publication Service Disruption"
date: 2024-07-07
incident_date: "2024-07-02"
type: "rpki"
affected: ["RIPE NCC", "paas.rpki.ripe.net", "LIRs using hosted RPKI"]
impact: "RIPE NCC's hosted RPKI publication service went offline, potentially preventing Local Internet Registries using the platform from publishing ROA updates."
source_url: "https://status.ripe.net/incidents/9jj0djz6qn68"
description: "The paas.rpki.ripe.net RPKI-as-a-service publication endpoint experienced a service disruption on July 2, 2024, temporarily halting RPKI object publication for RIPE NCC members using the hosted service."
tags: ["ripe-ncc", "rpki", "roa", "hosted-rpki", "publication-point", "lir"]
---

RIPE NCC's hosted RPKI publication service (paas.rpki.ripe.net) experienced a service disruption on July 2, 2024. LIRs (Local Internet Registries) using RIPE NCC's hosted RPKI service to publish their Route Origin Authorizations were unable to create, update, or delete ROAs during the disruption. RIPE NCC published an incident report on their status page.
