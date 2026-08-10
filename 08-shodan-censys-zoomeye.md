# Chapter 8 — Shodan, Censys & Device Search Engines

> "Google is for websites. Shodan is for devices on the internet."

These tools index the real face of the internet — routers, webcams, servers, industrial control systems (ICS/SCADA) — live and sometimes vulnerable.

## 1. Shodan.io
- **Use:** search for IoT devices, exposed services, open ports across the entire internet.
- **Real use cases:** finding unsecured webcams, exposed databases, default-credential devices.
- **Example searches:**
  ```
  webcamxp
  port:22 country:"IN"
  default password
  ```
- Other useful filters: `product:`, `org:`, `net:` (CIDR range), `has_vuln:true`, `city:`

## 2. Censys.io
- **Use:** search certificates, hosts, IPs, open services.
- More focused on **TLS/HTTPS and large-scale internet scanning** than Shodan.
- **Example searches:**
  ```
  services.service_name: "http"
  443.https.tls.certificate.parsed.subject.common_name: "example.com"
  ```
- **Good for identifying:** expired certificates, misconfigured HTTPS, leaked subdomains (via cert SANs).

## Additional device/internet search engines
- **ZoomEye** (China, knownsec.com) — Shodan-equivalent with strong coverage of Asian infrastructure; useful for a different vantage point than Western-hosted scanners.
- **FOFA** (China, fofa.info) — another large-scale internet asset search engine, popular for Chinese and APAC infrastructure.
- **BinaryEdge.io** — internet-wide scanning with a strong API, good for automated monitoring of your own exposed assets.
- **GreyNoise.io** — tells you whether an IP scanning your network is "internet background noise" (mass scanners/bots) vs. a targeted attacker.
- **Netlas.io** — Shodan-alternative with generous free tier for domain/IP/cert search.
- **LeakIX** — indexes exposed/misconfigured services (open databases, unauthenticated admin panels) — heavily used for breach research.

## Defensive use
Security teams should run their **own** org name/IP ranges through Shodan/Censys periodically to catch accidental exposures (e.g., a dev database left open) before attackers find them — this is one of the most valuable *defensive* uses of these tools.
