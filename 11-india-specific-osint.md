# Chapter 11 — India-Specific OSINT Sources & Registries

Public, legitimate Indian government/regulatory and business registries useful during authorized recon on India-based organizations. All of these are **official public-record lookups** — no scraping or unauthorized access involved.

## Company & corporate records
- **MCA (Ministry of Corporate Affairs) — mca.gov.in** — search any registered Indian company/LLP: CIN, directors, registered address, incorporation date, filing status.
- **Zauba Corp (zaubacorp.com)** — friendlier interface over MCA data — company financials, director network graphs (who else a director is linked to).
- **GST Search (services.gst.gov.in)** — verify a business's GSTIN, registration status, and state jurisdiction.
- **Tofler.in** — Indian company intelligence, financials, and director relationship mapping (freemium).
- **Trademark & Patent search — ipindia.gov.in** — IP filings can reveal product roadmaps/brand names before public launch.

## Domain & telecom
- **.in domain WHOIS — registry.in** — India's ccTLD registry (NIXI); note most `.in` WHOIS is also proxy-masked now.
- **Truecaller** — reverse phone number lookup (crowd-sourced caller ID) — widely used in India for identifying unknown numbers (use ethically; it's a privacy-sensitive tool).
- **TRAI (trai.gov.in)** — telecom regulator, useful for verifying ISPs/telecom operators tied to an IP block.

## Government & legal
- **India Code (indiacode.nic.in)** — full text of Indian laws/acts — useful to check legal boundaries before any assessment (IT Act 2000, DPDP Act 2023).
- **Indian Kanoon (indiankanoon.org)** — searchable case law database — useful in due-diligence/investigation contexts.
- **RTI Online (rtionline.gov.in)** — Right to Information portal; RTI replies are sometimes published and contain org-structure/procurement data for government bodies.
- **CERT-In (cert-in.org.in)** — India's national CERT; publishes advisories on active threats/vulnerabilities relevant to Indian infrastructure — check before/after any engagement involving Indian entities.
- **eProcure / GeM (Government e-Marketplace)** — government tenders often disclose exact software/hardware being procured (a govt-sector equivalent of the "job posting tech stack leak" trick).

## Startup & funding intelligence
- **Tracxn** — India-focused startup funding, cap table, and org-network intelligence (paid, freemium tiers).
- **YourStory / Inc42** — Indian startup news — good for org history, leadership changes, past incidents.

## Data-breach & privacy law context
- India's **Digital Personal Data Protection Act, 2023 (DPDP Act)** and **IT Act, 2000 (Sections 43, 66, 66C, 66D, 72)** govern unauthorized access, data theft, and identity-theft-related offences. Always confirm written scope/authorization before any recon involving Indian citizens' personal data — this is a hard legal line, not just best practice.

## Practical tip
For India-based targets, combine **MCA/Zauba (corporate structure)** + **LinkedIn (employees)** + **job postings (tech stack)** + **GitHub dorks (`site:github.com "@company.in"` or `"@company.com"`)** — this combination alone typically maps org structure, tech stack, and staff contact patterns without a single active scan.
