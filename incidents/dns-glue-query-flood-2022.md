---
title: "DNS Query Flood from Lingering Hosting-Provider Glue Record"
date: 2022-09-15
incident_date: "2022-09-01"
type: "dns"
affected: ["Dataplane.org DNS sensor", "COM zone resolvers"]
impact: "Sensor received 300,000–700,000 additional unsolicited DNS queries per day, polluting signal data until resolved."
description: "A Dataplane.org sensor was assigned an IP previously used as a default nameserver glue record by a hosting provider for unconfigured COM domains, causing the sensor to receive up to 700,000 extra DNS queries per day until the provider updated the glue record."
tags: ["dns", "glue-record", "dns-sensor", "dataplane-org", "com-zone", "noise"]
---

A Dataplane.org network sensor was assigned an IP address that had previously been used as a default nameserver glue record by a hosting provider for customer domains under .COM. Because the provider had not updated the glue record after reassigning the IP, all DNS queries for unconfigured customer domains continued to flow to the Dataplane.org sensor — up to 700,000 unsolicited queries per day.

The anomaly polluted the sensor's DNS traffic data until the hosting provider was identified and persuaded to update the stale glue record. The incident is documented in the Dataplane.org newsletter.
