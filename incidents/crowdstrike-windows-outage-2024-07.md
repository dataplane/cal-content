---
title: "CrowdStrike Falcon Sensor Update Causes Global Windows Outage"
date: 2024-07-20
incident_date: "2024-07-19"
type: "outage"
affected: ["CrowdStrike", "Microsoft Windows", "Airlines", "Banks", "Hospitals", "Emergency Services", "Global"]
impact: "Estimated 8.5 million Windows systems rendered unbootable globally; one of the largest IT outages in history."
source_url: "https://www.crowdstrike.com/falcon-content-update-remediation-and-guidance-hub/"
description: "A faulty content update to CrowdStrike's Falcon sensor caused Windows systems worldwide to enter a boot loop (BSOD), taking down critical infrastructure across aviation, banking, healthcare, and emergency services in what became one of the largest IT outages in history."
tags: ["crowdstrike", "falcon", "windows", "bsod", "aviation", "global-outage", "endpoint-security", "supply-chain"]
---

On July 19, 2024, CrowdStrike deployed a defective channel file update (C-00000291-*.sys) to its Falcon endpoint security sensor. Windows systems running the affected version entered an unrecoverable boot loop displaying the Blue Screen of Death (BSOD), requiring manual intervention to recover each affected machine.

The outage affected an estimated 8.5 million Windows systems across virtually every industry: airlines grounded flights and reverted to paper ticketing; banks and financial services went offline; hospitals cancelled non-urgent procedures; and 911 call centers in several US states were impacted. Delta Air Lines alone cancelled over 7,000 flights.
