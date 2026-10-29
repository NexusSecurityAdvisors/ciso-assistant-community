# CISO Assistant Client Onboarding Runbook

Procedure for standing up CISO Assistant for a Nexus vCISO or readiness client. Always check the [upstream documentation](https://github.com/intuitem/ciso-assistant-community) for current deployment steps.

## 0. Decide the deployment model

| Option | When to use |
|---|---|
| **Client-hosted instance** (preferred) | Client owns the data and infrastructure; Nexus has a named user account |
| **Nexus-hosted, one instance per client** | Client has no hosting capability; never mix multiple clients in one instance |

- [ ] Data location, backup, and retention agreed in the SOW
- [ ] Hosting meets the client's obligations (e.g., CUI for CMMC, PHI for HIPAA)

## 1. Deploy

- Use the upstream Docker Compose quick start, pinned to a released version.
- Put it behind TLS and restrict access (VPN / IP allowlist / SSO).
- Change all default credentials; enforce MFA for every user.
- Configure automated, encrypted backups and test one restore.

## 2. Structure the program

1. Create a **domain / folder** for the client and **perimeters** for in-scope business units or systems.
2. Load frameworks from the library using [`framework-mapping.md`](framework-mapping.md).
3. Configure the risk matrix to match the **Nexus 5×5 likelihood × impact scale**.
4. Create users with least-privilege roles: client executive (read), client IT owner (edit assigned controls), Nexus (program admin).

## 3. Populate

- Import assets and key systems.
- Run the initial **compliance assessment** for each in-scope framework.
- Attach scanner evidence (Prowler, ScubaGear, ScubaGoggles reports) to the relevant requirements.
- Build the **risk register** from validated findings; link each risk to applied controls.
- Create the **remediation plan** with owners and target dates.

## 4. Operate (vCISO cadence)

| Cadence | Activity |
|---|---|
| Monthly | Update remediation status; review new risks |
| Quarterly | Re-run scanners, refresh evidence, update compliance assessments, board-ready posture report |
| Annually | Full risk assessment and policy review |

## 5. Offboarding

- Export the client's data in an agreed format and hand it over.
- For Nexus-hosted instances: securely destroy the instance and backups after the agreed retention period, and confirm in writing.
