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

# Hermes Agent Training ☤

## Built for Freelancers, by Freelancers

### 📌 Hands-on Training Overview

**A 2-week, project-based training that turns you into a freelance Hermes Agent Support Specialist. Master installation, deployment, troubleshooting, and integration — then land clients on Upwork, Freelancer, Guru, and direct channels.**

---

## Table of Contents

1. [Objective](#objective)
2. [Training Environment](#training-environment)
3. [Training Price, Duration & Format](#training-price-duration--format)
4. [Learning Objectives](#learning-objectives)
5. [Week 1 – Server Setup & Hermes Deployment](#week-1--server-setup--hermes-deployment)
6. [Week 2 – Production Hardening & Freelancing](#week-2--production-hardening--freelancing)
7. [Capstone Project](#capstone-project)
8. [Instructor Notes](#instructor-notes)
9. [Student Workbook Structure](#student-workbook-structure)
10. [FAQs](#faqs)

---

## Objective

Enable participants to become professional freelancers who can confidently deliver Hermes Agent services — installation, deployment, customization, troubleshooting, maintenance, integration, migration, and consulting — and sell those services on Upwork, Freelancer.com, Guru.com, LinkedIn, and direct-client channels.

This is a **project-based course, not a theory course**. Every lesson pairs concepts with a real lab performed on a live production server.

---

## Training Environment

All work is done in a **real production environment**, not a sandbox.

**Training Prerequisites**
- DigitalOcean: Ubuntu Linux Server (24.04 or 26.04 LTS recommended)
- Domain: Any domain or subdomain will work
- Freelance Marketplace: Verified Upwork · Guru · Freelancer account
- Land Direct Clients: LinkedIn and YouTube account
- Rigorous: Patience and concentration required during all sessions

**Connectivity**
- Portable messaging device for 24/7 client communication
- Reliable fiber-optic internet for uninterrupted sessions

---

## Training Price, Duration & Format

- **Fee:** $250
- **Duration:** 2 weeks
- **Schedule:** 5 training days/week, 20 hours total
- **Session length:** 2 hours (hands-on)
- **Marketplace:** Upwork · Guru · Freelancer

---

## Learning Objectives

By course completion, participants will be able to:

- Provision and secure an Ubuntu server on DigitalOcean
- Configure DNS records and domains/subdomains
- Install and configure Hermes Agent from source, incl. dashboard
- Configure AI providers (OpenAI, Ollama, Gemini, Anthropic, OpenRouter)
- Build Skills, enable Memory, integrate MCP servers/tools
- Configure Telegram/Slack/Discord/Email integrations
- Secure deployments with NGINX, HTTPS, Certbot, UFW, fail2ban
- Run Hermes as a systemd service with auto-restart
- Monitor logs, troubleshoot issues, back up/restore/upgrade
- Package and sell Hermes Agent services as a freelancer

---

## Week 1 – Server Setup & Hermes Deployment

**Goal:** A secured, HTTPS-enabled server running a fully functional Hermes Agent instance with a provider, Skill, and Memory configured.

### Day 1 — Server Provisioning & Linux Hardening
- **Objectives:** Create/access droplet; non-root sudo user; UFW; fail2ban
- **Lab:** Generate an SSH key pair, create an Ubuntu 24.04 LTS droplet (min 2GB RAM), create a non-root sudo user, allow SSH/web ports in UFW before enabling it, install fail2ban
- **Assignment:** Firewall status output + non-root user proof
- **Troubleshooting:** Locked out after UFW enable → always allow SSH *before* enabling; connection timeout → check DO firewall

### Day 2 — DNS, NGINX & HTTPS
- **Objectives:** Point domain to droplet; reverse proxy stub; issue SSL cert
- **Lab:** Create an A record to the droplet IP and verify propagation, install NGINX with a reverse proxy site config, install Certbot and issue an HTTPS cert
- **Assignment:** Working DNS lookup + site responding over valid HTTPS
- **Troubleshooting:** DNS not resolving → propagation delay vs wrong record type; Certbot fails → port 80 closed or DNS not propagated

### Day 3 — Hermes Agent Source Install & Dashboard
- **Objectives:** Clone/build/run Hermes from source; install dashboard; connect to reverse proxy
- **Lab:** Clone the repo, install dependencies, configure environment file, start the agent, point NGINX at it, set dashboard admin auth
- **Assignment:** Terminal output of successful startup + dashboard login screenshot over HTTPS
- **Troubleshooting:** Dependency conflicts → pin Python version; port in use → stop conflicting process

### Day 4 — AI Providers, Skills, Memory & MCP
- **Objectives:** Configure Ollama (local) + one cloud provider; build a custom Skill; enable Memory; register an MCP tool
- **Lab:** Pull a local model via Ollama and set it as a provider, configure a cloud AI provider, build a simple Skill (e.g. weather lookup), enable Memory backend, register an MCP tool
- **Assignment:** Successful test conversation using both providers + working Skill demo
- **Troubleshooting:** Provider timeout → check API key env var and outbound firewall rules

### Day 5 — systemd Service & Week 1 Assessment
- **Objectives:** Run Hermes as a managed systemd service with auto-restart on boot/failure
- **Lab:** Write and enable a systemd unit under a dedicated user; kill the process manually and confirm auto-restart
- **Weekly Assessment:** 10 MCQs (Linux, DNS, NGINX, systemd, providers, Skills, MCP) + live lab check of running HTTPS Hermes instance with provider, Skill, and Memory

**Mini Project (Week 1):** A fully deployed, HTTPS-secured Hermes Agent instance with provider, Skill, and Memory — running as a systemd service.

---

## Week 2 – Production Hardening & Freelancing

**Goal:** A hardened, monitored, integrated, client-ready Hermes deployment — plus a freelance profile and pricing package ready to publish.

### Day 6 — Security Hardening & Backup/Restore
- **Objectives:** Harden NGINX (headers, rate limiting); automate cert renewal; back up/restore/upgrade
- **Lab:** Add security headers (X-Frame-Options, X-Content-Type-Options, HSTS), confirm cert auto-renewal, archive config/data directories, simulate failure, restore from backup, perform a version upgrade
- **Assignment:** Hardened NGINX config + before/after proof of a successful restore

### Day 7 — Logging, Monitoring & Chat Integration
- **Objectives:** Monitor logs/resource usage; add Telegram/Slack/Discord/Email as an upsell integration
- **Lab:** Tail service logs under simulated load, configure a chosen platform's bot credentials, enable the channel, restart the service
- **Assignment:** Log excerpt with a triggered error + root-cause note; proof of working integration
- **Troubleshooting:** High memory → check Memory backend size limits; webhook not firing → check bot token, HTTPS webhook URL, firewall

### Day 8 — Troubleshooting Lab & Week 2 Technical Assessment
- **Objectives:** Diagnose and fix seeded failures (bad config, expired cert, wrong provider key, systemd misconfig, NGINX 502)
- **Timed Lab:** Instructor injects 3 faults; participant diagnoses and fixes within 45 minutes
- **Quiz:** 10 MCQs on production ops

### Day 9 — Marketplace Profile, Pricing & Proposals
- **Objectives:** Build an Upwork/Freelancer/Guru profile as a "Hermes Agent Deployment & Support Specialist"; value-based pricing; winning proposals
- **Activities:** Write headline/overview/skills list using Week 1–2 projects as portfolio; draft 3 tiered packages (Basic Install / Full Deployment / Managed Support); write 2 real job proposals; run a mock client interview
- **Assignment:** Completed profile draft + pricing sheet + 2 proposals

### Day 10 — Scoping, Handover & Capstone Presentation
- **Objectives:** Write a Statement of Work and SLA; package a client handover deliverable; present the capstone
- **Activities:** Draft an SOW/SLA for a sample "Deploy Hermes Agent with Telegram integration" project; prepare a client-facing handover document; present the capstone (15 min) to instructor + peers
- **Weekly Assessment:** Peer-reviewed mock client proposal + handover package + capstone demo

**Mini Project (Week 2):** A hardened, monitored, integrated production deployment, plus a freelancer profile, pricing sheet, SOW/SLA, and handover package ready to publish.

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

- Enforce **"own server, own domain"** from Day 1 — no shared sandboxes.
- Seed intentional faults on Day 8 (bad NGINX config, expired token, wrong systemd path) to build genuine debugging reflexes.
- Both weeks end with a **graded live check** on the participant's actual running server, not a slide review.
- Day 9 mock client interview should be run by instructor or peer acting as a skeptical client — reward participants who ask clarifying scoping questions before quoting price.
- Maintain a shared repo of proposal templates, SOW/SLA templates, and pricing sheets for participants to fork and customize.
- Encourage participants to record their capstone demo — it becomes portfolio/marketing content for their freelance profile and YouTube/LinkedIn presence.

---

## Student Workbook Structure

Each participant maintains a workbook (repo or document) with:

1. `/week1-server-hermes/` — commands run, screenshots, DNS records, UFW/Certbot proof, provider/Skill/Memory configs (secrets redacted)
2. `/week2-production-freelance/` — hardened NGINX config, systemd unit, backup logs, fault-fix write-ups, profile draft, pricing sheet, SOW/SLA
3. `/capstone/` — full documentation, runbook, handover package, demo recording link
4. `/notes/` — daily reflections and troubleshooting log (personal knowledge base for future client work)

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
2 weeks, 10 sessions, 20 hours total, at 2 hours/day.
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
<summary><b>Can I pay in installments to join this training?</b></summary>
No, we don't offer installment payments to join our training.
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
