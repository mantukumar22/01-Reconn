# Chapter 3 — WHOIS Lookup, DNS Records, Reverse DNS

## WHOIS Lookup
**"Jise website dikhti hai, uske peeche ka malik bhi dikhta hai"** — whoever's website you see, you can also see who's behind it.

- Finds: domain owner, registrar, contact email, address, registration/expiry dates.
- Tool: `whois example.com`
- Note: many domains now use **WHOIS privacy/proxy protection**, which masks the real registrant — you'll only see the privacy service's details.

## DNS (Domain Name System)
Converts domain names → IP addresses. Different record types leak different info:

| Record | Purpose |
|--------|---------|
| `A` / `AAAA` | Domain → IPv4 / IPv6 address |
| `MX` | Mail server(s) handling the domain's email |
| `NS` | Authoritative name servers |
| `TXT` | Arbitrary text — often SPF/DKIM/DMARC, domain verification strings |
| `CNAME` | Alias to another domain |
| `SOA` | Zone authority info, serial numbers |
| `PTR` | Used for reverse DNS |

Tools: `nslookup example.com` or `dig example.com`

## Reverse DNS
Converts an **IP back into a domain name** (PTR record lookup).
```
nslookup <IP>
dig -x <IP>
```

## Bonus tip (from course)
Use **[hackertarget.com](https://hackertarget.com)** for free web-based DNS tools (WHOIS, DNS lookup, reverse DNS, zone transfer test, etc.) without installing anything.

> *Example: "Kabhi socha email kis server se jata hai? MX record bata dega."* — Ever wondered which server an email goes through? The MX record tells you.

## Extra tools for this stage
- **crt.sh** — search Certificate Transparency logs to find subdomains from SSL certs issued for a domain.
- **DNSDumpster.com** — free DNS recon + visual domain map, shows subdomains, MX, TXT records.
- **SecurityTrails.com** — historical DNS/WHOIS data (see past IPs, old registrant info even after privacy was enabled).
- **ViewDNS.info** — reverse WHOIS, reverse IP, DNS propagation checker.
- **Sublist3r / Subfinder / Amass** — CLI subdomain enumeration tools that combine multiple passive sources (certificate transparency, search engines, DNS brute force).
- **dnstwist** — finds typosquatted/lookalike domains registered against your brand (useful defensively).
