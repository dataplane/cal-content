---
title: "XZ Utils Supply Chain Backdoor (CVE-2024-3094)"
date: 2024-03-31
incident_date: "2024-03-29"
type: "security"
affected: ["XZ Utils", "Linux distributions", "OpenSSH"]
impact: "Deliberately inserted backdoor in xz/liblzma versions 5.6.0–5.6.1 giving unauthorized remote access to affected SSH servers; caught before widespread deployment in stable Linux releases."
source_url: "https://www.openwall.com/lists/oss-security/2024/03/29/4"
description: "A sophisticated supply chain attack embedded a backdoor in the xz compression utility (versions 5.6.0 and 5.6.1), targeting systemd-linked OpenSSH servers on Linux. Discovered by Andres Freund at Microsoft before the compromised versions reached most stable Linux distributions."
tags: ["supply-chain", "backdoor", "xz", "liblzma", "openssh", "linux", "cve-2024-3094", "security"]
---

On March 29, 2024, Microsoft engineer Andres Freund disclosed that xz/liblzma versions 5.6.0 and 5.6.1 contained a deliberately inserted backdoor (CVE-2024-3094). The backdoor was introduced by a long-term contributor known as "Jia Tan" (JiaT75) who had spent roughly two years building trust in the xz project before executing the attack.

The backdoor modified the RSA key decryption process in liblzma, which OpenSSH links through systemd on affected systems. When exploited with a specific hidden key, it would allow unauthenticated remote code execution. Freund noticed the backdoor while investigating unexpected CPU usage and SSH authentication slowness on a Debian testing system.

The compromised versions had reached several rolling-release and testing distributions (Fedora 40/41 beta, Debian testing, Arch, openSUSE Tumbleweed) but did not reach any stable/LTS distributions before discovery. The attacker's toolkit and patient multi-year social engineering campaign was considered a landmark supply chain attack against open source infrastructure.
