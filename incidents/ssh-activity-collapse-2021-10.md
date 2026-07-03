---
title: "Global SSH Client Activity Sudden Collapse"
date: 2021-10-10
incident_date: "2021-10-06"
type: "anomaly"
affected: ["SSH client activity globally", "libssh library users", "Multiple unrelated networks"]
impact: "Dramatic unexplained drop in global SSH probe and client connection attempts; cause never publicly identified."
description: "Around October 6, 2021, a sudden collapse in SSH client connection attempts was observed globally across multiple unrelated networks — most significantly among libssh library users. The anomaly was independently verified by SANS and NETSCOUT ASERT, but the root cause was never publicly identified."
tags: ["ssh", "libssh", "anomaly", "internet-scanning", "measurement", "netscout", "sans"]
---

Around October 6, 2021, observers across multiple unrelated networks noticed a dramatic and unexplained collapse in SSH client connection attempts globally. The drop was particularly pronounced among traffic attributable to the libssh library. The anomaly was independently observed by SANS Internet Storm Center port-22 monitors and NETSCOUT ASERT analysts, confirming it was a real global phenomenon rather than a local measurement artifact.

Despite the unusual nature and scale of the event, no public explanation was ever provided for the sudden and sustained drop in SSH scanning/probing activity. The event remains an unexplained data point in internet measurement history.
