# Security Policy

## Reporting a Vulnerability

This project is part of the OS2 – Offentligt Digitaliseringsfællesskab (OS2(ai)) community. Security vulnerabilities and incidents concerning OS2 products are handled through the OS2 community security process.

Please read the OS2 security policy before reporting:

<https://www.os2.eu/web/content/18350?unique=1dd0b16d88dcd2d111a890e397f91d0bc1b19b43>

More information is available at [os2.eu/sikkerhed](https://www.os2.eu/sikkerhed). Machine-readable contact details are published per RFC 9116 at [os2.eu/.well-known/security.txt](https://www.os2.eu/.well-known/security.txt).

**Do not report suspected vulnerabilities in public GitHub issues or other open channels** if they could be used to compromise systems or data. Send reports to <security@os2.eu>, and CC the product-specific contact (e.g. `os2ai@os2.eu`) when one exists.

A report should include, where possible:

- The system or OS2 product the report concerns (e.g. this repository).
- A description of the vulnerability or security incident.
- How it can be reproduced or verified.
- An assessment of the potential impact.
- Contact details, if you want feedback.

Do not send passwords, personal data, or other sensitive information via ordinary e-mail. Contact <security@os2.eu> first to agree a secure way to exchange information.

## Scope

This repository contains Helm charts and GitOps configuration deployed by adopting organizations. Vulnerabilities in third-party dependencies (upstream charts and container images) are shared upstream where possible. Remediation of running deployments is the responsibility of the organization operating them.

Automated or AI-generated reports without a verified, reproducible finding may be closed without further response.

## Bug Bounty

OS2 has no bug bounty program and offers no monetary reward for reported vulnerabilities. We appreciate responsible disclosure and coordination with the responsible parties before any information is published.
