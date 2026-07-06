---
title: "Dataplane.org RPKI Publication Point Degradation"
date: 2022-09-15
incident_date: "2022-09-01"
type: "rpki"
affected: ["Dataplane.org RPKI publication point", "RPKI relying parties fetching from Dataplane.org"]
impact: "Severe RPKI publication point performance degradation; ROA management impossible due to CPU spikes during removal attempts."
description: "Dataplane.org's RPKI publication point and certificate authority experienced severe performance issues in September 2022 after an experimental ROA publication campaign pushed the system beyond its limits, requiring a full system rebuild."
tags: ["rpki", "roa", "publication-point", "dataplane-org", "certificate-authority"]
---

In September 2022, Dataplane.org's RPKI publication point and CA experienced severe degradation following an experimental campaign to publish a large number of Route Origin Authorizations (ROAs). The scale of the experiment exceeded the system's capacity; attempting to remove the extraneous ROAs caused CPU spikes and timeouts that made the system effectively unmanageable. The incident required a planned rebuild of the RPKI publication point infrastructure.

This was an internal operational incident at Dataplane.org, documented in their newsletter.
