# Chapter 7 — Competitive Intelligence Techniques

> "Hackers don't just break things — they study their targets deeply."

## 1. Job Postings = Tech Stack Leak
Companies often unintentionally reveal their internal tools/tech stack in job descriptions.

- 📌 Companies mention specific tools by name in JDs.
- 🧠 **Hacker's trick:** read the JD to learn what tech the company runs.

**Example:**
> "Looking for a React.js developer with AWS, NGINX, and MongoDB experience"

➡️ Now you know their frontend framework, cloud provider, web/reverse-proxy server, and database — enough to start researching known vulnerabilities for that exact stack combination.

## Where to look
- Company career pages, **LinkedIn Jobs**, **Naukri.com** / **Indeed** / **Glassdoor**
- Look for: cloud provider, CI/CD tools, database, frameworks, security tools mentioned ("must know Splunk", "experience with Kubernetes"), even internal tool names.

## Other competitive-intel sources
- **BuiltWith.com / Wappalyzer** — detect the exact tech stack of a live website (CMS, analytics, CDN, frameworks) without needing a job posting.
- **Glassdoor / AmbitionBox (India)** — employee reviews sometimes leak internal tool names, org structure, or security practices.
- **SEC filings (EDGAR) / MCA filings (India)** — public company financial and structural disclosures.
- **Patents & research papers** — reveal R&D direction and sometimes technical architecture.
- **Conference talks / GitHub org repos / engineering blogs** — companies often publicly describe their own stack (great passive source, zero risk).
- **Crunchbase / Tracxn (India-focused)** — funding, leadership, and subsidiary/acquisition mapping — useful for understanding an org's attack surface across related entities.
