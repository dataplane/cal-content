---
title: "ARIN RPKI RRDP Service Disruption"
date: 2024-07-14
incident_date: "2024-07-08"
type: "rpki"
affected: ["ARIN", "RPKI RRDP", "ARIN-region RPKI relying parties"]
impact: "ARIN's RPKI Repository Delta Protocol (RRDP) service experienced an outage, disrupting relying party cache updates for the ARIN region."
source_url: "https://arin.statuspage.io/incidents/5nl6xjzdf1zc"
description: "ARIN's RPKI RRDP publication endpoint suffered a service disruption on July 8, 2024, preventing RPKI relying party software from fetching delta updates to ARIN-region ROA and RPKI object data."
tags: ["arin", "rpki", "rrdp", "route-origin-authorization", "relying-party"]
---

ARIN's RPKI Repository Delta Protocol (RRDP) endpoint experienced a service disruption on July 8, 2024. RRDP is the primary mechanism by which RPKI relying party software (validators) fetches updated RPKI objects from registries. During the disruption, relying parties were unable to receive fresh ARIN-region ROA data via RRDP, potentially falling back to rsync or serving stale cached data. ARIN published an incident report on their status page.
