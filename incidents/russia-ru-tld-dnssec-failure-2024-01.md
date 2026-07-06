---
title: "Russia .RU TLD DNSSEC Failure"
date: 2024-02-04
incident_date: "2024-01-30"
type: "outage"
affected: ["Russia", ".RU TLD", "DNSSEC", "Coordination Center for TLD RU"]
impact: "Widespread resolution failures for .ru domains lasting several hours; websites and services under .ru inaccessible for users relying on validating resolvers."
source_url: "https://circleid.com/posts/20240130-dnssec-failure-causes-massive-website-outages-on-russian-internet"
description: "A DNSSEC signing failure in the Russian .ru TLD zone caused DNSSEC-validating resolvers worldwide to return SERVFAIL for .ru domains, making a large portion of the Russian Internet inaccessible for users behind validating resolvers."
tags: ["dnssec", "russia", "ru-tld", "dns", "outage", "tld", "zone-signing"]
---

On January 30, 2024, the Russian .ru top-level domain zone experienced a DNSSEC signing failure that caused widespread resolution outages. The Coordination Center for TLD RU failed to correctly sign the zone, resulting in an invalid or expired DNSSEC signature chain. DNSSEC-validating resolvers worldwide began returning SERVFAIL responses for any .ru query, making domains under .ru unreachable for users whose DNS resolvers performed DNSSEC validation.

The failure affected a broad swath of Russian Internet services and websites. While users behind non-validating resolvers could still resolve .ru names, many public resolvers (including those from major cloud and ISP providers) perform validation, leaving millions of users unable to access .ru sites.

Russia had experienced a similar DNSSEC failure previously. The NANOG and DNS-OARC mailing lists discussed the failure mode and resolution timeline. Full recovery required the zone to be re-signed with a valid key and for resolvers to flush their negative caches.
