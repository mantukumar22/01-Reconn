# Chapter 2 — Google Hacking / Google Dorks

## What it is
Using advanced Google search operators to surface pages, files, and data that were never meant to be publicly indexed — misconfigurations, exposed backups, leaked credentials in text, etc.

## Core operators

| Operator | Purpose | Example |
|----------|---------|---------|
| `site:` | Restrict results to a domain/TLD | `site:gov.in` |
| `intext:` | Word must appear in page body | `intext:"password"` |
| `filetype:` | Restrict to a file extension | `filetype:xls` |
| `inurl:` | Word must appear in the URL | `inurl:"email"` |
| `intitle:` | Word must appear in page title | `intitle:"index of"` |

## Live examples from the course
```
site:gov.in intext:"password"
filetype:xls inurl:"email"
intitle:"index of" "backup"
intitle:"index of" aadhar card
```
These surface open directory listings, leaked spreadsheets with emails, and government-domain pages that mention credentials — classic signs of misconfigured web servers.

> ⚠️ Never attempt to access, download, or use data found this way if it involves personal/sensitive records (e.g., ID documents) you're not authorized to view — doing so can itself be a criminal offence (e.g., unauthorized access to personal data under India's DPDP Act / IT Act, or GDPR elsewhere). Report such exposures responsibly instead.

## Combine operators
```
site:example.com filetype:pdf intext:"confidential"
site:linkedin.com intitle:"[Company] employees"
```

## Reference database
- **Google Hacking Database (GHDB)** — [exploit-db.com/google-hacking-database](https://www.exploit-db.com/google-hacking-database) — a categorized library of thousands of dorks (maintained by Offensive Security), covering files containing usernames/passwords, vulnerable servers, sensitive directories, error messages, and more.

## Other search-engine dorking (not Google-only)
- **Bing dorks** — similar syntax (`site:`, `filetype:`, `ip:`), sometimes surfaces different indexed content than Google.
- **DuckDuckGo** — useful for non-personalized, non-filtered results.
- **Yandex** — often indexes Russian/CIS content Google misses.
