# Chapter 10 — Additional Global Recon Tools & Techniques

Tools not covered in the original course but essential in a modern (2026) OSINT/recon toolkit worldwide.

## Automated recon frameworks
- **SpiderFoot** — free/open-source, automates 200+ OSINT modules (DNS, breach data, dark web, social, threat intel) into one correlated scan; has a web UI. One of the best "run once, get everything" tools.
- **Amass** (OWASP) — industry-standard subdomain enumeration + attack-surface mapping, combines passive sources with active DNS resolution and graph visualization.
- **SpyOnWeb / DNSlytics** — find websites sharing the same Analytics ID, AdSense ID, or IP — great for uncovering related/shadow domains owned by the same org.

## Network & infrastructure
- **Nmap** — the standard active scanning tool (port/service/OS detection); `nmap -sV -sC target` is the classic first active scan (⚠️ authorization required).
- **Masscan** — extremely fast internet-wide port scanner, often paired with Nmap for deep-dive follow-up.
- **traceroute / mtr / tracert** — map network path/hops to a target.
- **BGP.he.net (Hurricane Electric)** — look up ASN, IP ranges, and peering info for an organization.

## Web & wayback
- **Wayback Machine (web.archive.org)** — see historical snapshots of a site; often reveals deleted pages, old employee lists, or removed sensitive files.
- **Google Cache / Bing Cache** — view a recently indexed but now-changed/removed page.
- **Wappalyzer / BuiltWith** — browser extensions/sites that fingerprint a website's tech stack instantly.

## Breach & credential intelligence
- **Have I Been Pwned** — breach exposure lookup (email/domain).
- **DeHashed / LeakCheck / IntelligenceX** — searchable breach databases (use only for authorized investigations).
- **GitGuardian / TruffleHog** — scan GitHub/GitLab repos for leaked API keys, secrets, and credentials in commit history.

## People & image OSINT
- **PimEyes / FaceCheck.id** — reverse face-search engines (ethically sensitive — use with caution and only where legally permitted).
- **TinEye / Google Lens / Yandex Images** — reverse image search to trace an image's origin.
- **Pipl, Spokeo, Whitepages** — people-search aggregators (mostly US/EU data coverage).

## Threat intelligence & correlation
- **VirusTotal** — check domains/IPs/files against 70+ antivirus/threat-intel engines; also shows passive DNS and related samples.
- **AlienVault OTX (Open Threat Exchange)** — free threat intelligence feeds and IOC search.
- **MISP** — open-source threat intelligence sharing platform, commonly used by CERTs and SOCs.

## All-in-one directories
- **OSINT Framework** (osintframework.com) — categorized tree linking to nearly every free OSINT tool by category.
- **IntelTechniques.com** — Michael Bazzell's curated OSINT tools + free "OSINT Tools" companion PDF, updated regularly.
