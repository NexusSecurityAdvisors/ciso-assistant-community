# Framework Selection and Evidence Mapping

Which CISO Assistant library frameworks to load for each Nexus client type, and how scanner evidence feeds into them. Library contents change over time, so confirm the current framework list in your deployed version.

## Frameworks by client type

| Client type | Load first | Add as needed |
|---|---|---|
| **Any SMB (default)** | NIST CSF 2.0 | CIS Controls v8 (if available) for prioritized safeguards |
| **Defense supplier / DIB** | NIST SP 800-171 Rev 2 (current CMMC L2 basis), CMMC 2.0 | NIST SP 800-171 Rev 3 to plan ahead |
| **Healthcare / HIPAA covered entity or BA** | HIPAA Security Rule (if available in library), NIST CSF 2.0 | HHS 405(d) HICP practices as a guide |
| **SaaS / tech vendor** | SOC 2 (TSC 2017), NIST CSF 2.0 | ISO/IEC 27001:2022 |
| **Financial services** | NIST CSF 2.0 | FFIEC / state requirements (e.g., NYDFS Part 500) where applicable |
| **AI-heavy organization** | NIST AI RMF, ISO/IEC 42001 (if available) | EU AI Act for EU exposure |

Use CISO Assistant's **mapping** features to reuse evidence across frameworks instead of assessing the same control twice.

## Where scanner evidence goes

| Evidence source | NIST CSF 2.0 categories it supports |
|---|---|
| Prowler (cloud) | ID.AM, ID.RA, PR.AA, PR.DS, PR.PS, PR.IR, DE.CM |
| ScubaGear (M365) | PR.AA, PR.DS, PR.PS, DE.CM, DE.AE |
| ScubaGoggles (Google Workspace) | PR.AA, PR.DS, PR.PS, DE.CM, DE.AE |
| Policy and interview evidence (Nexus posture review) | GV (all), ID.IM, PR.AT, RS, RC |

Automated scanners cover technical controls well and governance controls poorly. **GV, RS, and RC** always need interviews, documents, and tabletop evidence.
