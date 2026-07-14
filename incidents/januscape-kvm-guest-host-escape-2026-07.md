---
title: "Januscape — KVM Guest-to-Host Escape Vulnerability (CVE-2026-53359)"
date: 2026-07-14
incident_date: "2026-07-09"
type: "security"
affected: ["KVM", "Linux kernel", "Intel and AMD virtualization hosts", "Cloud providers"]
impact: "A guest VM with root access can exploit a use-after-free in KVM's shadow MMU emulation to crash or gain full code execution on the host hypervisor, breaking guest/host isolation in multi-tenant cloud environments."
source_url: "https://github.com/V4bel/Januscape"
description: "Researchers disclosed Januscape (CVE-2026-53359), a guest-to-host escape affecting in-kernel KVM's x86 shadow MMU emulation across roughly 16 years of kernel versions, triggerable on both Intel and AMD, and previously used as a 0-day in Google's kvmCTF competition."
tags: ["kvm", "virtualization", "vm-escape", "cve-2026-53359", "linux-kernel", "cloud-security"]
---

Security researchers published Januscape, tracked as CVE-2026-53359, a use-after-free vulnerability in KVM's x86 shadow MMU emulation. The affected code spans commits from August 2010 through June 2026 — roughly 16 years of kernel versions.

A guest VM with root-level access can exploit the flaw to corrupt the host kernel's shadow page table, resulting in either a kernel panic (denial of service) or full code execution with root privileges on the hypervisor. Unlike prior QEMU-level escapes, this vulnerability lives in in-kernel KVM itself, which the researchers describe as the first guest-to-host exploit triggerable on both Intel and AMD platforms — potentially affecting cloud providers running proprietary virtualization stacks on top of KVM.

The bug was previously exploited as a 0-day in Google's kvmCTF competition in June 2024, and was disclosed responsibly to linux-distros@vs.openwall.org ahead of public publication. Because it threatens isolation between co-tenant VMs on shared physical hosts, it carries particular weight for multi-tenant cloud infrastructure.
