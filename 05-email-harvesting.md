# Chapter 5 — Email Harvesting

## What is it
Gathering email addresses from public sources to build a target list — used (legitimately) to test phishing awareness, or (maliciously) for spam/phishing. In authorized engagements, this maps out the org's **email naming convention** (e.g. `first.last@company.com`) which is critical for phishing simulations and password-spray planning.

## Live tool: theHarvester
```
theHarvester -d example.com -b google
```
Options:
- `-d` → target domain
- `-b` → data source (google, bing, baidu, duckduckgo, yahoo, linkedin, etc. — or `all`)
- `-l` → limit number of results
- `-f` → save output to file (html/xml/json)

## Other sources for email hunting

| Source | How |
|--------|-----|
| **hunter.io** | Shows a company's email pattern + known addresses from its domain |
| **Google Dorks** | `site:example.com "@example.com"` , `filetype:xls intext:@example.com` |
| **GitHub leaks** | `site:github.com "@example.com"` — commit emails, config files |

### 💡 Pro tip
Cross-reference emails found in multiple places (WHOIS registrant, GitHub commits, LinkedIn "contact info", leaked spreadsheets) to confirm the company's actual email format before larger enumeration.

## Additional email-recon tools
- **Snov.io / Voila Norbert / Clearbit Connect** — email finder/verifier services (commercial, similar to hunter.io).
- **EmailRep.io** — reputation lookup for an email address (flags if it's associated with spam/breaches).
- **Have I Been Pwned (haveibeenpwned.com)** — checks if an email/domain has appeared in known data breaches (great for defensive awareness — also has a domain-wide breach search for verified domain owners).
- **DeHashed / Intelligence X** — breach-data search engines (paid/limited free tier) — used in authorized investigations only.
- **Mailboxlayer / Verifalia** — bulk email verification (checks if harvested addresses are still active/deliverable).
