<p align="center">
  <img src="banner.png" alt="Hermes Agent" width="100%">
</p>

<p align="center">
  <a href="https://github.com/SchoolOfFreelancing/Hermes-Agent-Training.git/">Hermes Agent Training</a> | <a href="https://github.com/SchoolOfFreelancing/Hermes-Agent-Support.git/">Hermes Agent Support</a>
</p>

<p align="center">
  <a href="https://t.me/SchoolOfFreelancingTraining">
    <img src="https://img.shields.io/badge/Telegram-Get%20Live%20Support-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram Support">
  </a>

  <a href="https://wa.me/8801748973769">
    <img src="https://img.shields.io/badge/WhatsApp-Get%20Live%20Support-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp Support">
  </a>

  <a href="https://nousresearch.com">
    <img src="https://img.shields.io/badge/Built%20by-Nous%20Research-blueviolet?style=for-the-badge" alt="Built by Nous Research">
  </a>
</p>

# Hermes Agent Training  ☤

**Built for Freelancers, by Freelancers** 

## 📌 Overview

A production-ready, hands-on, project-based training curriculum that turns participants into freelance-ready Hermes Agent specialists — capable of installing, deploying, customizing, troubleshooting, maintaining, integrating, migrating, and consulting on Hermes Agent for clients worldwide.
---

## Table of Contents

1. [Objective](#objective)
2. [Training Environment](#training-environment)
3. [Course Duration & Format](#course-duration--format)
4. [Learning Objectives](#learning-objectives)
5. [Week 1 – Linux, Cloud & Production Environment](#week-1--linux-cloud--production-environment)
6. [Week 2 – Hermes Agent Installation & Configuration](#week-2--hermes-agent-installation--configuration)
7. [Week 3 – Production Deployment & Client Support](#week-3--production-deployment--client-support)
8. [Week 4 – Freelancing & Real Client Projects](#week-4--freelancing--real-client-projects)
9. [Capstone Project](#capstone-project)
10. [Instructor Notes](#instructor-notes)
11. [Student Workbook Structure](#student-workbook-structure)
12. [FAQs](#faqs)

---

## Objective

Enable participants to become professional freelancers who can confidently deliver Hermes Agent services — installation, deployment, customization, troubleshooting, maintenance, integration, migration, and consulting — and sell those services on Upwork, Freelancer.com, Guru.com, LinkedIn, and direct-client channels.

This is a **project-based course, not a theory course**. Every lesson pairs concepts with a real lab performed on a live production server.

---

## Training Environment

All work is done in a **real production environment**, not a sandbox.

| Component | Tool |
|---|---|
| VPS Provider | DigitalOcean |
| OS | Ubuntu Server 24.04 LTS |
| DNS | Domain/subdomain + Cloudflare (optional) |
| Access | SSH |
| Version Control | GitHub |
| Web Server | NGINX |
| SSL | Certbot |
| Process Manager | systemd |
| Runtime | Python + uv |
| Containers | Docker (where applicable) |
| Local LLM | Ollama |
| Cloud LLMs | OpenAI / Gemini / Anthropic (optional) |

**Prerequisite for each participant:** own DigitalOcean account, own domain or subdomain, and a GitHub account before Day 1.

---

## Course Duration & Format

- **Duration:** 1 month (4 weeks)
- **Schedule:** 5 training days/week, 20 sessions total
- **Session length:** 2 hours (hands-on lab format)
- **Cadence:** Daily assignment → Weekly assessment → Final capstone
- **Class ratio:** Recommended max 1 instructor : 8 participants for effective lab supervision

---

## Learning Objectives

By course completion, participants will be able to:

- Provision and secure an Ubuntu server on DigitalOcean
- Configure DNS records and domains/subdomains
- Install and configure Hermes Agent from source
- Install and manage the Hermes Dashboard
- Configure AI providers (OpenAI, Ollama, Gemini, Anthropic, OpenRouter, etc.)
- Build and configure AI agents, Skills, and Memory
- Integrate MCP servers and tools
- Set up delegation and provider routing
- Configure Telegram, Slack, Discord, and Email integrations
- Secure deployments with NGINX, HTTPS, and Certbot
- Manage Hermes Agent as a systemd service
- Monitor logs, troubleshoot issues, and optimize performance
- Upgrade, back up, restore, and migrate Hermes deployments
- Package and sell Hermes Agent services as a freelancer

---

## Week 1 – Linux, Cloud & Production Environment

**Goal:** Every participant ends the week with a secured, HTTPS-enabled Ubuntu server on their own domain.

### Day 1 — DigitalOcean & Server Provisioning
- **Objectives:** Create and access a droplet; understand VPS sizing/regions
- **Tools:** DigitalOcean account, SSH client
- **Lab:** Generate a local SSH key pair, create a Ubuntu 24.04 LTS droplet (minimum 2GB RAM) through the DigitalOcean dashboard, attach the SSH key, and connect to the server as root
- **Assignment:** Screenshot of successful SSH login; submit droplet IP + region
- **Troubleshooting guide:** Permission denied (publickey) → check SSH config and key path; connection timeout → check DO firewall rules

### Day 2 — Linux Fundamentals & Hardening
- **Objectives:** Filesystem hierarchy, package management, user management, UFW, fail2ban
- **Lab:** Update the system, create a non-root sudo user, configure the UFW firewall to allow SSH and web traffic before enabling it, and install fail2ban for brute-force protection
- **Assignment:** Submit firewall status output and non-root sudo user proof
- **Troubleshooting guide:** Locked out after UFW enable → always allow SSH port *before* enabling UFW

### Day 3 — Domain, DNS & Cloudflare
- **Objectives:** Point a domain/subdomain to the droplet; understand A/CNAME records; optional Cloudflare proxy
- **Lab:** Create an A record pointing your chosen subdomain to the droplet's IP address, and verify propagation using a DNS lookup tool
- **Assignment:** Submit working DNS lookup output
- **Troubleshooting guide:** DNS not resolving → propagation delay (up to 24h) vs. wrong record type

### Day 4 — NGINX, systemd & Certbot
- **Objectives:** Install NGINX, create a reverse proxy stub, issue HTTPS cert
- **Lab:** Install NGINX, create a reverse proxy site configuration pointing the domain at a local backend port, enable the site, then install Certbot and issue an HTTPS certificate for the domain
- **Assignment:** Submit a request showing the site responding correctly over HTTPS with a valid certificate
- **Troubleshooting guide:** Config test fails → syntax error in the server block; Certbot fails → port 80 not open or DNS not yet resolved

### Day 5 — Python, uv & systemd Services
- **Objectives:** Install Python/uv; create and manage a systemd unit for a placeholder service
- **Lab:** Install Python and the uv package manager, create a virtual environment, then write and enable a systemd unit file for a placeholder service and confirm it is running
- **Weekly Assessment (quiz + lab check):**
  - Quiz: 10 MCQs on Linux, DNS, NGINX, systemd, SSL
  - Lab check: instructor verifies live HTTPS site + systemd service running

**Mini Project (Week 1):** Deploy a secure Ubuntu server with HTTPS on a custom domain — graded pass/fail against the rubric below.

---

## Week 2 – Hermes Agent Installation & Configuration

**Goal:** A fully functional Hermes Agent instance, connected to at least one AI provider, with Skills and Memory enabled.

### Day 6 — Hermes Agent Architecture
- **Objectives:** Understand core components: agent runtime, dashboard, config store, provider layer, MCP layer
- **Lab:** Diagram the architecture based on official docs; identify config file locations
- **Assignment:** Submit an architecture diagram (hand-drawn or digital)

### Day 7 — Source Installation
- **Objectives:** Clone, build, and run Hermes Agent from source
- **Lab:** Clone the Hermes Agent source repository, install dependencies, prepare the environment configuration file, and start the agent locally
- **Assignment:** Submit terminal output of successful startup
- **Troubleshooting guide:** Dependency conflicts → pin the required Python version; port in use → identify and stop the conflicting process

### Day 8 — Hermes Dashboard & Authentication
- **Objectives:** Install dashboard, configure admin auth, connect to reverse proxy from Week 1
- **Lab:** Update the NGINX reverse proxy target to point at Hermes; set dashboard admin password/token
- **Assignment:** Submit screenshot of dashboard login over HTTPS

### Day 9 — AI Provider Configuration
- **Objectives:** Configure Ollama (local), plus at least one cloud provider (OpenAI/Gemini/Anthropic)
- **Lab:** Install Ollama and pull a local model, then configure Hermes to use it as a provider; separately configure Hermes with credentials for at least one cloud AI provider
- **Assignment:** Submit a successful test conversation using two different providers
- **Troubleshooting guide:** Provider timeout → check API key env var and outbound firewall rules

### Day 10 — Skills, Memory & MCP Basics
- **Objectives:** Create a custom Skill, enable persistent Memory, connect one MCP server/tool
- **Lab:** Build a simple "weather lookup" or "ticket triage" Skill; enable Memory backend; register an MCP tool
- **Weekly Assessment:**
  - Quiz: 10 MCQs on Hermes architecture, providers, Skills, MCP
  - Lab check: live demo of agent answering via configured provider + one working Skill

**Mini Project (Week 2):** Deploy a fully functional Hermes Agent instance connected to an AI model, with one custom Skill and Memory enabled.

---

## Week 3 – Production Deployment & Client Support

**Goal:** A hardened, monitored, documented, production-grade Hermes deployment.

### Day 11 — Reverse Proxy & SSL Automation
- **Objectives:** Harden NGINX config (headers, rate limiting), automate cert renewal
- **Lab:** Add security headers (X-Frame-Options, X-Content-Type-Options, HSTS) to the NGINX configuration, and confirm certificate auto-renewal is correctly scheduled
- **Assignment:** Submit NGINX config with security headers + passing SSL Labs scan (or local equivalent check)

### Day 12 — systemd Service Management for Hermes
- **Objectives:** Run Hermes as a managed systemd service with auto-restart
- **Lab:** Write a systemd unit file for Hermes Agent that runs it under a dedicated user, restarts automatically on failure, and starts on boot; enable and start the service
- **Assignment:** Kill the process manually and prove systemd auto-restarts it

### Day 13 — Logging, Monitoring & Performance
- **Objectives:** Centralize logs, monitor resource usage, tune for load
- **Lab:** Tail the Hermes Agent service logs in real time and observe CPU/RAM usage under a simulated load
- **Assignment:** Submit a log excerpt with an intentionally triggered error, plus root-cause note
- **Troubleshooting guide:** High memory usage → check Memory backend size limits; slow responses → check provider latency vs. local inference load

### Day 14 — Backup, Restore & Upgrades
- **Objectives:** Back up config/data, simulate disaster recovery, perform a safe version upgrade
- **Lab:** Archive the configuration and data directories as a backup, simulate a failure, then restore from the backup and perform a version upgrade
- **Assignment:** Submit before/after proof of a successful restore

### Day 15 — Troubleshooting Common Deployment Issues
- **Objectives:** Diagnose and fix 5 seeded/injected failures (bad config, expired cert, wrong provider key, systemd misconfig, NGINX 502)
- **Weekly Assessment:**
  - Timed lab: instructor injects 3 faults; participant must diagnose and fix within 45 minutes
  - Quiz: 10 MCQs on production ops

**Mini Project (Week 3):** Deploy a production-ready Hermes Agent environment that is secure, stable, monitored, and fully documented (README + runbook).

---

## Week 4 – Freelancing & Real Client Projects

**Goal:** Convert technical skill into a sellable freelance service.

### Day 16 — Marketplace Profile & Positioning
- **Objectives:** Build a professional Upwork/Freelancer.com/Guru.com profile positioned as a "Hermes Agent Deployment & Support Specialist"
- **Activities:** Write headline, overview, and skills list; select portfolio pieces from Weeks 1–3 projects
- **Assignment:** Submit completed profile draft for peer + instructor review

### Day 17 — Pricing, Proposals & Client Interviews
- **Objectives:** Learn value-based pricing, write winning proposals, handle client interviews
- **Activities:** Draft 3 tiered service packages (Basic Install / Full Deployment / Managed Support); write 2 real job proposals; run a mock client interview
- **Assignment:** Submit pricing sheet + 2 proposals for feedback

### Day 18 — Scoping, SOWs & SLAs
- **Objectives:** Define project scope, write a Statement of Work and a Service Level Agreement
- **Activities:** Draft an SOW and SLA for a sample "Deploy Hermes Agent with Telegram integration" project
- **Assignment:** Submit SOW + SLA documents

### Day 19 — Integrations Deep Dive (Telegram / Slack / Discord / Email)
- **Objectives:** Add a chat-platform integration as a premium upsell service
- **Lab:** Configure the chosen platform's bot credentials in the Hermes environment configuration, enable the corresponding channel, and restart the service
- **Assignment:** Submit proof of a working Telegram (or Slack/Discord) integration
- **Troubleshooting guide:** Webhook not firing → check bot token, HTTPS webhook URL, and firewall

### Day 20 — Client Onboarding, Documentation & Handover
- **Objectives:** Package a full client deliverable: documentation, maintenance plan, handover checklist
- **Activities:** Prepare a client-facing handover document; simulate final walkthrough call
- **Weekly Assessment:** Peer-reviewed mock client proposal + handover package

**Mini Project (Week 4):** Complete freelancer profile, 3 service packages, 1 SOW/SLA pair, and 1 integration case study — ready to publish.

---

## Capstone Project

**Deliverable:** End-to-end Hermes Agent deployment for a simulated client, including:

1. VPS provisioning (DigitalOcean, Ubuntu 24.04)
2. Domain/subdomain configuration
3. HTTPS setup (NGINX + Certbot)
4. Hermes Agent installation from source
5. At least one AI provider integrated (cloud or local)
6. At least one Skill and Memory configured
7. At least one chat-platform integration (Telegram/Slack/Discord/Email)
8. Security hardening (UFW, fail2ban, NGINX headers)
9. systemd service with auto-restart
10. Full documentation (README, runbook, backup/restore procedure)
11. Client handover package (SOW, SLA, maintenance plan)
12. Live demo/presentation to instructor + peers (15 minutes)

**Grading:** Pass requires all 12 items present and functional; distinction requires clean documentation and a polished client-ready presentation.

---

## Instructor Notes

- Enforce **"own server, own domain"** from Day 1 — no shared sandboxes; real production experience is the differentiator of this course.
- Seed intentional faults during Week 3 and the final exam (bad NGINX config, expired token, wrong systemd path) to build genuine debugging reflexes, not memorized steps.
- Weeks 1–3 should end with a **graded live check** on the participant's actual running server, not a slide review.
- Week 4 mock client interviews should be run by instructor or peer acting as a skeptical client — reward participants who ask clarifying scoping questions before quoting price.
- Maintain a shared repo of proposal templates, SOW/SLA templates, and pricing sheets for participants to fork and customize.
- Encourage participants to record their capstone demo — it becomes portfolio/marketing content for their freelance profile and YouTube/LinkedIn presence.

---

## Student Workbook Structure

Each participant maintains a workbook (repo or document) with:

1. `/week1-server-setup/` — commands run, screenshots, DNS records, UFW/Certbot proof
2. `/week2-hermes-install/` — install logs, provider configs (secrets redacted), architecture diagram
3. `/week3-production/` — NGINX configs, systemd unit files, backup logs, fault-fix write-ups
4. `/week4-freelance/` — profile draft, pricing sheet, proposals, SOW/SLA, integration proof
5. `/capstone/` — full documentation, runbook, handover package, demo recording link
6. `/notes/` — daily reflections and troubleshooting log (personal knowledge base for future client work)

This workbook doubles as the participant's **portfolio evidence** for marketplace profiles and client pitches.

---

# FAQs

<details>
<summary><b>What is Hermes Agent?</b></summary>
A self-hosted AI agent platform. Training covers installation, configuration, and deployment for client use.
</details>

<details>
<summary><b>Do I need coding experience?</b></summary>
No. Basic Linux command-line familiarity is enough to start.
</details>

<details>
<summary><b>How long is the course?</b></summary>
15 modules, ~30 hours total, at 3 hours/day.
</details>

<details>
<summary><b>What will I be able to do after completing it?</b></summary>
Deploy, configure, and support Hermes Agent for freelance clients, including troubleshooting and Upwork-ready delivery.
</details>

<details>
<summary><b>What is Guaranteed Minimum Income (GMI)?</b></summary>
School of Freelancing's Guaranteed Minimum Income (GMI) ensures eligible trainees earn a minimum income after completing the program by following our guidelines.
</details>

<details>
<summary><b>What is Credential Verification Support?</b></summary>
School of Freelancing offers Credential Verification Support — if any organization wants to confirm a student's training, they can verify your credentials directly with us.
</details>

<details>
<summary><b>Can I pay installments for join this training?</b></summary>
No we don't offer any installments payment to join our training.
</details>

# Hermes Agent Web Dashboard

```
───────────────────────────────────────────────
✧(｡•̀ᴗ-)✧ Hermes Agent: Stable Release
───────────────────────────────────────────────
```

![Hermes Agent](web.png)

<br/>

## Disclaimer
This repository is intended to provide Hermes Agent installation Freelance Support. Product names, trademarks, and service names belong to [Nous Research](https://nousresearch.com/).

⭐ If this repository helps you, please consider starring it and sharing it with others.

<div align="center">

[![Twitter Follow](https://img.shields.io/twitter/follow/AnythingLinux?style=social)](https://twitter.com/AnythingLinux)

</div>

<div align="center"> Made with ❤️ in Bangladesh </div>

