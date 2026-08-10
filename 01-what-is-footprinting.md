# Chapter 1 — What is Footprinting?

## Definition
**Footprinting** is the process of gathering information about a target system, network, or organization to identify potential vulnerabilities *before* launching an attack (or before defending against one).

- It's the **first step in ethical hacking / pentesting** — hackers (and defenders) collect as much data as possible before touching the target directly.
- Also called **reconnaissance** or **information gathering** — Phase 1 of the standard pentest lifecycle:
  `Recon → Scanning → Gaining Access → Maintaining Access → Covering Tracks`

## Passive vs. Active Footprinting

| Type | Meaning | Contact with target? | Examples |
|------|---------|----------------------|----------|
| **Passive** | Information gathered **without** directly contacting the target (*"bina contact kiye"*) | ❌ No | Google search, LinkedIn, WHOIS, social media, job postings, cached pages |
| **Active** | Gathered via **direct interaction** with target systems | ✅ Yes | Ping, traceroute, port scanning, banner grabbing, DNS zone transfer attempts |

> 🧠 Rule of thumb: if the target's server/logs could notice you, it's **active**. If you're only reading public data through a third party (search engine, registrar, social platform), it's **passive**.

## Why it matters
- Passive recon is low-risk and often legal even without explicit authorization (public data), but active recon almost always requires written authorization.
- A good footprint gives an attacker/pentester: tech stack, employee names & roles, email formats, network ranges, exposed devices, and physical/organizational structure — often enough to plan a highly targeted attack (spear phishing, credential stuffing, exploiting a known CVE in a discovered software version).
