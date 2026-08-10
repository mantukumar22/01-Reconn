# Chapter 12 — End-to-End Recon Workflow Checklist

A practical order of operations for an authorized recon engagement, tying together all prior chapters.

## Phase 0 — Scope & authorization
- [ ] Written authorization / signed scope document in hand
- [ ] Confirm in-scope domains, IP ranges, and explicitly out-of-scope assets
- [ ] Note legal framework (India: IT Act/DPDP; elsewhere: local law) and any data-handling restrictions

## Phase 1 — Passive domain & infrastructure recon
- [ ] WHOIS lookup on primary domain(s) — Ch.3
- [ ] DNS records: A, MX, TXT, NS, SOA — Ch.3
- [ ] Subdomain enumeration: Amass / Subfinder / crt.sh / DNSDumpster — Ch.3, Ch.10
- [ ] Wayback Machine snapshot review — Ch.10
- [ ] Tech stack fingerprint: BuiltWith / Wappalyzer — Ch.7, Ch.10

## Phase 2 — Organizational & people recon
- [ ] LinkedIn: employee roles, org structure — Ch.4
- [ ] Job postings for tech stack leaks — Ch.7
- [ ] Corporate registry lookup (MCA/Zauba for India, EDGAR/Companies House elsewhere) — Ch.7, Ch.11
- [ ] GitHub/GitLab dorks for leaked secrets/emails — Ch.4, Ch.5

## Phase 3 — Email & credential recon
- [ ] theHarvester run across multiple sources — Ch.5
- [ ] hunter.io for email pattern confirmation — Ch.5
- [ ] Have I Been Pwned domain check (if authorized) — Ch.5, Ch.10
- [ ] GitGuardian/TruffleHog scan on any discovered public repos — Ch.10

## Phase 4 — Document & metadata recon
- [ ] Metagoofil / FOCA sweep of public PDFs/DOCs on target domain — Ch.6
- [ ] exiftool spot-checks on any downloaded images — Ch.6

## Phase 5 — Internet-exposed asset discovery
- [ ] Shodan search on org name / known IP ranges — Ch.8
- [ ] Censys certificate search for subdomains/expired certs — Ch.8
- [ ] GreyNoise/BinaryEdge cross-check for exposed services — Ch.8, Ch.10

## Phase 6 — Consolidate & report
- [ ] Build the organization's digital footprint map (Maltego/Recon-ng graph) — Ch.9
- [ ] Prioritize findings by risk (exposed creds > exposed services > metadata leaks > org-chart info)
- [ ] Write findings with remediation guidance — not just a list of exposures

## Golden rule
Passive recon first, always. Only move to active techniques (scanning, direct interaction) once scope is confirmed and passive recon has told you *where* to look.
