# Awesome-Attack-Surface-Management-ASM

# Awesome-Attack-Surface-Management-ASM
**Top Attack Surface Management ASM (Opensource) 🌟 Star if you like it! 🌟**

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on External Asset Discovery, Shadow IT Detection, Exposure Prioritization & Continuous Monitoring*
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Attack Surface Management (ASM)**. These tools enable security teams to discover unknown internet-facing assets, identify exposures before attackers exploit them, and continuously monitor for drift—from fully managed enterprise platforms with global internet scanning and adversary intelligence to self-hosted recon frameworks and open ASM platforms that give teams complete control over their discovery pipelines and data.

**Examples** include CrowdStrike Falcon Surface, Palo Alto Cortex Xpanse, Censys, Shodan, Recorded Future, NetSPI, Rapid7, Bishop Fox Cosmos, ProjectDiscovery Cloud, and Hadrian (the category leaders in commercial space).

**Open-source emphasis**: This section is expanded with every relevant project for self-hosted attack surface discovery, reconnaissance, and open ASM infrastructure. **Critical note**: The open-source ASM space is active but fragmented—**OWASP Amass** dominates subdomain enumeration, **reNgine** and **reNgine-ng** provide full recon suites, and **OASM** offers a modern distributed ASM platform. However, no open-source project matches Censys's internet-wide scanning map or CrowdStrike's adversary intelligence-driven prioritization.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[CrowdStrike Falcon Surface](https://www.crowdstrike.com/en-au/resources/data-sheets/falcon-surface/)**
  **Adversary-driven External Attack Surface Management (EASM)** within the Falcon platform. Maps and indexes over **7 billion exposed assets globally each year** (160 million weekly) without requiring an asset inventory—only a domain address is needed to map the entire ecosystem, including subsidiaries and third-party vendors . Prioritizes risks using CrowdStrike's adversary intelligence, CVE scores, geolocation, attack history, and asset type. **Pricing**: Quote-only; enterprise contracts. **Free tier**: None. **Best for**: CrowdStrike customers wanting EASM tightly integrated with threat intelligence and vulnerability management—**trade-off**: ecosystem lock-in and enterprise pricing.

- **[Palo Alto Cortex Xpanse](https://www.paloaltonetworks.com/)**
  **Active External Attack Surface Management** with continuous monitoring and exposure management. Named a Leader in Forrester's ASM evaluation . Discovers unmanaged AI infrastructure ("Shadow AI") and OT devices exposed to the internet. Integrates with Cortex XSIAM for unified SecOps . **Pricing**: Quote-only; subscription based on monitored assets and features . **Free tier**: None. **Best for**: Palo Alto customers wanting ASM integrated with a broader Cortex security platform.

- **[Censys](https://censys.com/)**
  **Internet-wide attack surface management** powered by the Censys Internet Map. Discovers assets across **all 65,535 ports**—including non-standard and high ports routinely missed by competitors. Claims **6x faster** asset discovery and up to **65% more attack surface visibility** . Uses first-party scanning, not just third-party data. **Pricing**: Quote-only; tiered by asset count. **Free tier**: None. **Best for**: teams wanting the most complete internet-wide visibility—**note**: Censys's scanning map is a genuine differentiator that open-source tools cannot replicate.

- **[Shodan](https://www.shodan.io/)**
  **Search engine for internet-connected devices** with a continuously updated index of exposed services, banners, and vulnerabilities. Shodan Enterprise provides monitoring and alerting for organizational assets . **Pricing**: Freemium for basic search; Enterprise quote-only. **Free tier**: Limited search results. **Best for**: security researchers and teams wanting a broad view of internet exposure—**note**: Shodan is a data source, not a full ASM workflow platform.

- **[Recorded Future Attack Surface Intelligence](https://www.recordedfuture.com/products/attack-surface-intelligence)**
  **Intelligence-driven EASM** with 10+ years of historical DNS, WHOIS, and SSL/TLS data. Customers report **29% increase in visibility** and **51% reduction in vulnerable attack surface** within six months . Integrates with Recorded Future's Intelligence Graph for threat context on exposures adversaries are actively targeting. **Pricing**: Quote-only. **Free tier**: None. **Best for**: organizations wanting ASM enriched with threat intelligence—**note**: strongest for teams already using Recorded Future.

- **[NetSPI Attack Surface Visibility](https://www.netspi.com/attack-surface-visibility/)**
  **Managed ASM service** with weekly external discovery scans, cloud configuration reviews (AWS, Azure), dark web monitoring, and look-alike domain detection . Delivered by offensive security experts who validate findings. **Pricing**: Quote-only; managed service. **Free tier**: None. **Best for**: organizations wanting human-validated ASM with penetration testing expertise—**note**: service-oriented rather than self-service tooling.

- **[Bishop Fox Cosmos](https://bishopfox.com/)**
  **Fully managed ASM service** with tech-enabled experts who validate asset ownership and exploitability. A Fortune 500 utility relies on Cosmos for continuous perimeter tracking across subsidiaries and compliance with NERC CIP/TSA directives . **Pricing**: Quote-only; managed service. **Free tier**: None. **Best for**: critical infrastructure and regulated industries wanting validated findings with expert guidance.

- **[Rapid7](https://www.rapid7.com/)**
  **Security analytics and ASM** through Insight platform. **Pricing**: Quote-only. **Free tier**: Limited. **Best for**: Rapid7 customers wanting ASM alongside vulnerability management and SIEM.

- **[ProjectDiscovery Cloud](https://cloud.projectdiscovery.io/)**
  **Managed platform for ProjectDiscovery's open-source tools** (Nuclei, Subfinder, httpx, etc.) with cloud orchestration and collaboration . **Pricing**: Free tier; paid plans for teams. **Free tier**: Yes. **Best for**: teams already using ProjectDiscovery tools wanting managed execution and collaboration.

- **[Hadrian](https://www.hadrian.io/)**
  **Agentic AI offensive security platform** combining continuous exposure management (Atlas) with agentic penetration testing (Nova). Claims **10x greater visibility** into critical exposures and **80% reduction** in time to resolution . Raised $40M in 2026; customers include McKesson, NBC Universal, TotalEnergies. **Pricing**: Quote-only. **Free tier**: None. **Best for**: organizations wanting AI-driven exploitability validation at scale.

## Open-Source GitHub Projects

- **[OWASP Amass](https://github.com/owasp-amass/amass)**
  **In-depth attack surface mapping and asset discovery** (Apache 2.0) — **the most widely adopted open-source recon tool** with ~15,000 GitHub stars . **Features**: **Subdomain enumeration** via 50+ data sources including APIs (Shodan, VirusTotal, SecurityTrails, Censys, FOFA, ZoomEye), certificate transparency, DNS brute forcing, web archives, and WHOIS . **Network mapping** of attack surfaces using open-source intelligence and active reconnaissance. Used by Accenture's adversary simulation team and Visma's red team . **Tech stack**: Go. **Deploy**: CLI (`go install`, Homebrew, Docker). **Trade-off**: **Subdomain enumeration and asset discovery only**—no vulnerability scanning, exposure prioritization, or continuous monitoring dashboard. It is a recon foundation, not a complete ASM platform. **Best for**: security teams and bug bounty hunters wanting the most comprehensive open-source subdomain and asset discovery engine—as the first stage of a custom ASM pipeline.

- **[reNgine](https://github.com/yogeshojha/rengine)**
  **Automated reconnaissance framework for web applications** (GPL-3.0 per Docker Hub) — **the most complete open-source recon suite with a web UI** . **Features**: **Subdomain discovery** (Subfinder, Amass), **port discovery** (Naabu), **endpoint discovery**, **directory bruteforce**, **screenshot gathering** with gallery and filters, **vulnerability scan using Nuclei**, OSINT capabilities (employee/email gathering, leaked database checks), **customizable scan engines** via YAML, **periodic scans** with change detection, **notifications** to Slack/Discord/Telegram, **automatic HackerOne reporting** . **Tech stack**: Python (Django), PostgreSQL, Redis. **Deploy**: Self-hosted (Ubuntu/VPS with installation script). **Trade-off**: **Recon and vulnerability scanning, not full ASM lifecycle**—no asset ownership attribution, no exposure scoring based on adversary intelligence. **Best for**: penetration testers and bug bounty hunters wanting a comprehensive recon suite with a UI and automation.

- **[reNgine-ng](https://github.com/Security-Tools-Alliance/rengine-ng)**
  **Next-generation fork of reNgine** (license per repo) — **a modernized, refactored alternative to the original reNgine** . **Features**: Same core capabilities as reNgine (subdomain discovery, port scanning, screenshots, Nuclei vulnerability scanning, notifications) with **significant refactoring by the community** and a 2.0 release. Designed to address limitations of the original and surpass commercial offerings for web application reconnaissance . **Tech stack**: Python (Django), PostgreSQL, Redis. **Deploy**: Self-hosted (Ubuntu/VPS). **Trade-off**: **Fork fragmentation**—the original reNgine and reNgine-ng have diverged; choose based on community activity and feature requirements. Still recon-focused, not full ASM. **Best for**: teams wanting a modernized reNgine with active community development.

- **[OASM (Open Attack Surface Management)](https://github.com/oasm-platform/open-asm)**
  **Open-source ASM platform** (GPL-3.0) — **the most complete open-source ASM platform architecture** found in this research . **Features**: **Asset discovery and management** (domains, IPs, services) with grouping and multi-workspace support; **vulnerability assessment** with issue tracking, risk analysis, and remediation guidance; **technology detection**; **distributed scanning engine** with horizontally scalable workers; **tool integration framework**; **MCP server integration** for AI assistants to query asset data via natural language; **workflow automation** with scheduled scans and alerts; **real-time monitoring** with statistics dashboard . **Architecture**: Web console, core API, Redis queue, PostgreSQL, distributed workers, MCP server . **Tech stack**: Per repository. **Deploy**: Docker Compose (one command) . **Trade-off**: **Younger project with limited community validation** compared to Amass or reNgine. Does not have Censys-scale internet scanning or adversary intelligence. **Best for**: security teams wanting a self-hosted ASM platform with a modern architecture, distributed scanning, and AI assistant integration—willing to evaluate and contribute to an early-stage project.

- **[IVRE](https://github.com/ivre/ivre)**
  **Network recon framework** (GPL-3.0) — **the most mature open-source alternative to Shodan/Censys for building your own internet-wide scanning infrastructure**, with ~4,100 GitHub stars . **Features**: Build **self-hosted and fully-controlled** alternatives to Shodan, ZoomEye, Censys, and GreyNoise; run your own **Passive DNS service**; collect and analyze network intelligence from your sensors; uses **Nmap, Masscan, Zeek, p0f, and ProjectDiscovery tools** . **Tech stack**: Python. **Deploy**: Self-hosted. **Trade-off**: **Infrastructure for building ASM, not a turnkey ASM platform**—requires significant operational investment to run scanning sensors and manage data. **Best for**: organizations wanting to operate their own internet-wide scanning capability—essentially building a private Shodan/Censys.

- **[vamp-easm](https://pypi.org/project/vamp-easm/)**
  **Lightweight continuous EASM engine with delta detection** (PyPI) — **the most focused open-source tool for continuous external monitoring with change detection** . **Features**: **Daily diff tracking**—each run compared against previous snapshot in SQLite, surfacing only what changed; **subdomain enumeration** via crt.sh and HackerTarget; **port scanning** (async TCP, optional nmap); **TLS certificate inspection** (issuer, expiration, SANs, self-signed detection); **webhook alerts** for CRITICAL/HIGH diffs (Slack/Discord compatible); **Shodan and Censys enrichment**; CI/CD-ready exit codes (0 clean, 1 HIGH, 2 CRITICAL) . **Tech stack**: Python (pip install). **Deploy**: CLI (`pip install vamp-easm`). **Trade-off**: **Delta detection engine, not a full ASM platform**—no web UI, no vulnerability scanning beyond enrichment, no asset attribution. **Best for**: teams wanting a lightweight, scriptable continuous monitoring tool that alerts only on changes—ideal for CI/CD or cron-based monitoring.

- **[ProjectDiscovery Nuclei](https://github.com/projectdiscovery/nuclei)**
  **Fast, customizable vulnerability scanner** (MIT) — **the most widely used open-source vulnerability scanner for ASM pipelines**, with ~14,000 GitHub stars (as part of the ProjectDiscovery ecosystem) . **Features**: Template-based vulnerability scanning with a community-curated template repository; used by reNgine, OASM, and countless custom ASM pipelines as the vulnerability detection engine. **Tech stack**: Go. **Deploy**: CLI, Docker, or managed via ProjectDiscovery Cloud . **Trade-off**: **Scanner only**—no asset discovery, ASM workflow, or exposure prioritization. It is a component in a larger pipeline. **Best for**: teams building ASM pipelines needing a proven, fast vulnerability scanner with an active template community.

### Additional Strong Open-Source Options

- **Red Kite** — Extensible Attack Surface Management tool (per GitHub topic listing). **Note**: Listed among ASM repositories but with limited documentation available in search results. **Best for**: exploration, not production adoption .
- **Mantis** — Security framework automating discovery, reconnaissance, and vulnerability scanning workflows. **Note**: Workflow automation, not a full ASM platform . **Best for**: teams wanting to automate recon-to-vuln-scan pipelines.
- **ElectricEye** — Multi-cloud, multi-SaaS security posture and attack surface monitoring (Python CLI). **Note**: Cloud/SaaS posture focus, not internet-wide asset discovery . **Best for**: cloud security teams wanting posture checks across AWS, Azure, GCP, and SaaS.

**Frameworks for building custom systems**: Combine **OWASP Amass** for comprehensive subdomain and asset discovery with **Nuclei** for vulnerability scanning, **vamp-easm** for continuous delta monitoring, and **OASM** as the ASM platform layer—creating a self-hosted ASM stack. **None of these match Censys's internet-wide scanning map or CrowdStrike's adversary intelligence-driven prioritization**; those require commercial platforms or building your own scanning infrastructure with **IVRE**.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- ASM platforms scanning external infrastructure must respect legal boundaries—only scan assets you own or have explicit authorization to test. Unauthorized scanning may violate computer fraud laws (CFAA, etc.).
- **The "internet-wide scanning platform" vs. "recon framework" vs. "ASM platform" vs. "continuous monitoring engine" distinction is critical.** **Censys and Shodan** operate **internet-wide scanning infrastructure**—their visibility comes from scanning the entire internet continuously . **CrowdStrike and Cortex Xpanse** are **adversary-intelligence-driven ASM platforms**—they prioritize exposures based on threat context . **OWASP Amass** and **reNgine** are **recon frameworks**—they discover assets but do not provide exposure prioritization or full ASM workflow . **OASM** is an **ASM platform**—it orchestrates discovery, vulnerability assessment, and issue tracking . **vamp-easm** is a **continuous monitoring engine**—it detects changes, not a full platform . **Choose based on whether you need visibility, workflow, or change detection.**
- **OWASP Amass is the foundation of most open-source ASM pipelines.** It is the most comprehensive subdomain enumeration tool, used by Accenture and Visma red teams . **The trade-off**: it discovers assets but does not assess or prioritize them—you need Nuclei and a platform layer on top.
- **reNgine and reNgine-ng are the most complete open-source recon suites with UI**, combining Amass, Subfinder, Naabu, and Nuclei into a single workflow with screenshots and notifications . **The trade-off**: they are recon-focused, not full ASM lifecycle management.
- **OASM is the most ambitious open-source ASM platform**, with distributed workers, MCP integration, and a modern architecture . **The trade-off**: it is early-stage with limited community validation—evaluate maturity before production use.
- **IVRE is the only open-source path to Censys-like visibility**—it lets you build your own internet-wide scanning infrastructure with Nmap, Masscan, Zeek, and ProjectDiscovery tools . **The trade-off**: significant operational investment to run scanning sensors and manage data.
- **Pricing opacity is universal across commercial ASM vendors.** CrowdStrike, Cortex Xpanse, Censys, Shodan Enterprise, Recorded Future, NetSPI, Bishop Fox, Rapid7, and Hadrian all require sales contact. ProjectDiscovery Cloud has a free tier. **Validate with direct vendor conversations against your asset count and scanning scope.**
- Self-hosted open-source solutions require proper infrastructure, legal review of scanning scope, and ongoing maintenance. **Scanning external infrastructure without authorization is illegal**—ensure your deployment only targets assets you own or have written permission to test.

---

**Made for security engineers, red teams, and organizations building transparent attack surface management solutions.**
Let's make Attack Surface Management more open, data-driven, and exposure-aware.
