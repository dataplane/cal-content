---
title: "DigiCert Mass TLS Certificate Revocations (Domain Validation Bug)"
date: 2024-08-04
incident_date: "2024-07-01"
type: "other"
affected: ["DigiCert", "Google Cloud", "DigiCert certificate holders globally"]
impact: "DigiCert was required to revoke and reissue a large batch of TLS certificates due to a domain validation bug, affecting Google Cloud and numerous other services under emergency timelines."
description: "DigiCert discovered a bug in its domain validation process that required mass revocation of affected TLS certificates in July 2024, forcing emergency reissuance affecting Google Cloud and many websites under tight regulatory deadlines."
tags: ["digicert", "tls", "certificate", "revocation", "google-cloud", "pki", "domain-validation"]
---

In July 2024, DigiCert discovered that a subset of TLS certificates had been issued using a defective domain validation method. CA/Browser Forum baseline requirements mandate rapid revocation of mis-issued certificates, requiring DigiCert to revoke a large batch of certificates within hours.

Google Cloud was among the affected customers, requiring emergency certificate reissuance across its services. Website operators across the internet were forced to replace certificates under tight deadlines to avoid service disruptions from browser rejection of revoked certificates.
