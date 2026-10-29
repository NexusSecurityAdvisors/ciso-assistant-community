# CISO Assistant at Nexus Security Advisors

This is the Nexus Security Advisors fork of [intuitem/ciso-assistant-community](https://github.com/intuitem/ciso-assistant-community). CISO Assistant is an open-source GRC platform for risk management, compliance, audits, and control mapping across many frameworks.

**The upstream code is unchanged.** This `nexus/` folder adds how we use CISO Assistant in client engagements.

## How Nexus uses it

CISO Assistant is the **system of record** for a Nexus vCISO program. The scanners in our other forks (Prowler, ScubaGear, ScubaGoggles) produce evidence, and CISO Assistant is where that evidence becomes a managed risk register, compliance assessments, and a remediation plan.

| Engagement | Use |
|---|---|
| **Fractional vCISO** | Ongoing risk register, policy and control tracking, board-ready posture reporting |
| **Compliance readiness** | Gap assessments against NIST CSF 2.0, NIST SP 800-171 / CMMC, HIPAA, SOC 2, ISO 27001, and others in the framework library |
| **AI governance** | Tracking AI-related risks and controls alongside the security program (e.g., NIST AI RMF, ISO/IEC 42001 where available in the library) |

## Contents

| File | Purpose |
|---|---|
| [`assessment-runbook.md`](assessment-runbook.md) | Client onboarding and program setup procedure |
| [`framework-mapping.md`](framework-mapping.md) | Which frameworks to load per client type, and how scanner evidence feeds in |
| [`client-report-checklist.md`](client-report-checklist.md) | Quality gate before a report goes to a client |

## License note (AGPL-3.0)

The community edition is licensed under **AGPL-3.0** (see upstream `LICENSE` for details and any enterprise-edition exceptions). If Nexus **modifies** the code and makes it available to clients over a network, the modified source must be offered to those users. This fork keeps upstream code unmodified. Get legal review before shipping code changes to a client-facing deployment.

## Keeping this fork current

Sync with upstream before every new deployment (**Sync fork**). Record the version deployed for each client.

## Disclaimer

Compliance assessments in CISO Assistant support readiness work and do not constitute an audit opinion, certification, or legal advice.

---

**Nexus Security Advisors** · Fractional CISO and AI governance for SMBs · SDVOSB
[nexussecurityadvisors.com](https://nexussecurityadvisors.com) · [info@nexussecurityadvisors.com](mailto:info@nexussecurityadvisors.com)
