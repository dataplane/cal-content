---
title: "UltraDNS DNSSEC Validation Errors"
date: 2024-04-07
incident_date: "2024-04-02"
type: "dns"
affected: ["UltraDNS", "UltraDNS customers", "DNSSEC-validating resolvers"]
impact: "DNSSEC validation errors disrupted DNS resolution for UltraDNS customers."
description: "UltraDNS experienced DNSSEC validation errors in early April 2024, causing DNS resolution failures for customers relying on DNSSEC-signed zones hosted on UltraDNS."
tags: ["ultradns", "dnssec", "dns", "validation-error"]
---

UltraDNS, a major managed DNS provider, experienced DNSSEC validation errors around April 2, 2024. The errors caused DNS resolution failures for customers whose zones were hosted on UltraDNS and relied on DNSSEC, particularly affecting resolvers that enforce DNSSEC validation (SERVFAIL responses instead of valid answers).
