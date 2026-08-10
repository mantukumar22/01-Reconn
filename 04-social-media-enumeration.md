# Chapter 4 — Social Media Enumeration

## What is it
Extracting valuable intel from social media platforms to build a digital profile of a target (person or organization).

> 👀 Looks normal to a casual viewer... but a hacker sees gold 💰

## What you can find

| Platform | What it reveals |
|----------|------------------|
| **LinkedIn** | Employee roles & org structure, tech stack from bios/skills |
| **Facebook / Instagram** | Birthdays, locations, events, family/relationship info |
| **GitHub / GitLab** | Code leaks, hardcoded secrets, usernames, commit emails |
| **Twitter/X, Reddit, forums** | Email IDs, reused usernames across platforms, opinions/affiliations |

## Live tools/demos from the course
- **linkedin.com** — search: `"Company X employees in Delhi"`
- **hunter.io** — extract email addresses tied to a domain
- **namechk.com** — check if a username is registered across many platforms
- **GitHub dork:** `site:github.com "@company.com"` — finds company email addresses leaked in commits, config files, or README's

## Additional social/username OSINT tools
- **Sherlock** (CLI, open-source) — checks a username across 400+ social platforms simultaneously.
- **Maigret** — like Sherlock but with richer profile parsing and report generation.
- **WhatsMyName.app** — web-based username search across many sites.
- **Social-Searcher.com** — real-time social media mention search.
- **Pipl / Spokeo / TruePeopleSearch** — people-search aggregators (mostly US data).
- **IntelTechniques Search Tools** (osintframework author Michael Bazzell) — curated manual search tools for almost every platform.
- **OSINT Framework** ([osintframework.com](https://osintframework.com)) — a giant categorized tree of free OSINT tools/sources for every recon need (usernames, emails, phone numbers, images, etc.)

## Ethical note
Enumerating **public** profile data is generally acceptable for authorized assessments; scraping at scale may violate platform Terms of Service, and using this data to harass, impersonate, or socially engineer someone without authorization is illegal.
