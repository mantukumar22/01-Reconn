# Chapter 9 — Core Recon Tools Cheat-Sheet

Quick reference for the four "flagship" tools highlighted in the course.

| Tool | What it does | Type |
|------|---------------|------|
| **theHarvester** | Emails, subdomains, hosts, employee names from search engines/PGP servers | CLI, free, open-source |
| **Maltego** | Visual link-analysis — maps relationships between domains, people, emails, infrastructure | GUI, free (Community Edition) + paid tiers |
| **Recon-ng** | Modular, automated recon framework (like Metasploit but for OSINT) | CLI, free, open-source |
| **FOCA** | Extracts metadata from public documents (PDF, DOC, XLS) found on a domain | GUI, Windows, free |

## theHarvester quick reference
```
theHarvester -d target.com -b all -l 200 -f report
```

## Recon-ng quick reference
```
recon-ng
workspaces create target_co
modules load recon/domains-hosts/hackertarget
options set SOURCE target.com
run
```

## Maltego quick reference
- Start a new graph → add a "Domain" entity → right-click → run transforms (e.g., "To DNS Name", "To Email addresses", "To Person").
- Free Community Edition has limited transform runs/day; paid version unlocks full transform hub + commercial data sources (e.g., Shodan, HaveIBeenPwned integrations).

## FOCA quick reference
1. New project → enter target domain.
2. Search engines (Google/Bing) auto-discover public docs.
3. Download → extract metadata → FOCA auto-builds a network map (usernames, software, folder paths, internal hostnames).
