---
title: "Optus Australia National Network Outage"
date: 2023-11-13
incident_date: "2023-11-08"
type: "outage"
affected: ["Optus", "Australia", "Mobile", "Fixed broadband"]
impact: "Approximately 10 million customers lost mobile and home Internet service for up to 12 hours; triple-zero (000) emergency calls failed for VoIP users; trains, hospitals, and businesses disrupted."
source_url: "https://www.theregister.com/2023/11/08/internet_phone_train_and_payments/"
description: "Optus, Australia's second-largest telecommunications provider, suffered a nationwide network outage affecting roughly 10 million mobile and fixed broadband customers. A BGP routing table update that exceeded equipment limits triggered cascading failures across the network."
tags: ["optus", "australia", "outage", "mobile", "broadband", "bgp", "triple-zero", "emergency-services"]
---

On November 8, 2023, Optus's Australian network failed completely in the early morning hours, leaving approximately 10 million customers without mobile or home Internet service. The outage began around 4 AM AEDT and lasted up to 12 hours for many users before restoration was complete.

The root cause was a software upgrade that introduced a large volume of new BGP routes, exceeding the capacity of Optus routing equipment. When the equipment received routing table updates containing more routes than it could handle, it disconnected from the network—and safety mechanisms designed to reconnect the devices instead triggered a cascading failure that spread across the network.

The outage had significant real-world impact: the New South Wales train network experienced disruption; hospital appointment systems and clinical tools were affected; payment terminals at businesses went offline; and VoIP-dependent users found they could not reach emergency services via triple-zero (000). Optus subsequently faced government scrutiny over its failure to adequately communicate during the incident and questions about redundancy in its network architecture.
