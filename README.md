<p align="center">
  <img src="assets/banner.svg" alt="LeadMaster — AI cold-outreach engine: 8,778 emails sent, 3.7% reply rate, 11,978 leads processed, 17 campaigns" width="100%"/>
</p>

<p align="center">
  <a href="https://leadmaster.ahmedhussain.tech"><img src="https://img.shields.io/website?url=https%3A%2F%2Fleadmaster.ahmedhussain.tech&label=LeadMaster&up_message=live&down_message=offline&up_color=3DD68C&style=for-the-badge&labelColor=101018" alt="LeadMaster status"/></a>
  <img src="https://img.shields.io/badge/In%20production-since%20April%202026-2FB980?style=for-the-badge&labelColor=101018" alt="In production since April 2026"/>
  <img src="https://img.shields.io/badge/Reply%20rate-3.7%25-3DD68C?style=for-the-badge&labelColor=101018" alt="Reply rate 3.7%"/>
</p>

**LeadMaster replaces manual lead research and copywriting for B2B cold outreach.** For every lead it reads their LinkedIn profile and company website, writes a personal first email with Claude or GPT-4o, sends from several Gmail inboxes, follows up three times in the same thread, and stops the moment the lead replies.

It runs real campaigns: **8,778 emails sent with a 3.7% reply rate**, above the 1–3% usually quoted for cold email.

## The live dashboard

<p align="center">
  <img src="screenshots/dashboard.png" alt="LeadMaster dashboard: 11,978 leads processed, 8,778 emails sent, 3.7% reply rate, 5 of 17 campaigns active" width="100%"/>
</p>
<p align="center"><sub>The production dashboard: leads processed, lifetime emails sent, reply rate across all campaigns, and leads grouped by industry.</sub></p>

## How it works

<p align="center">
  <img src="assets/architecture.svg" alt="LeadMaster pipeline: lead lists → categories → research → AI writer → campaigns → follow-ups → reply detection → sequence stop → dashboard" width="100%"/>
</p>

| Step | What happens |
|---|---|
| **1. Collect** | Leads come in by CSV upload or from scraping and data tools (Apify, Apollo), and are grouped into categories by industry and region. |
| **2. Research** | An n8n workflow reads each lead's LinkedIn profile and company website. |
| **3. Write** | Claude or GPT-4o writes a personal first email from that research, following the campaign's template and tone. |
| **4. Send** | Campaigns spread sending across several Gmail inboxes, with three threaded follow-ups per lead. |
| **5. Listen** | Every inbox is scanned for replies. Each reply is matched to its lead by thread ID, that lead's sequence stops, and the dashboard updates. |
| **6. Improve** | Sends, replies and bounces per campaign and per day show which segment and which message work. |

## Results

| Measure | Value |
|---|---:|
| Leads processed | **11,978** |
| Emails sent (lifetime) | **8,778** |
| Reply rate, all campaigns | **3.7%** |
| Campaigns run | **17** |
| Lead categories | **12** |

## Production practices

- **Background workers** do the sending and the reply scanning, so the dashboard never waits on Gmail.
- **Reply-safe sequences:** a lead who replies never gets another automated follow-up.
- **Multi-inbox sending** spreads volume across inboxes to protect deliverability.
- **Accounts** are verified with an emailed one-time code (OTP).
- **Deployment:** Nginx with TLS in front of FastAPI on a Linux server, with PostgreSQL.

## Tech stack

<p>
  <img src="https://img.shields.io/badge/Python-101018?style=for-the-badge&logo=python&logoColor=3DD68C" alt="Python"/>
  <img src="https://img.shields.io/badge/FastAPI-101018?style=for-the-badge&logo=fastapi&logoColor=3DD68C" alt="FastAPI"/>
  <img src="https://img.shields.io/badge/React-101018?style=for-the-badge&logo=react&logoColor=5AB4F5" alt="React"/>
  <img src="https://img.shields.io/badge/AG%20Grid-101018?style=for-the-badge" alt="AG Grid"/>
  <img src="https://img.shields.io/badge/PostgreSQL-101018?style=for-the-badge&logo=postgresql&logoColor=5AB4F5" alt="PostgreSQL"/>
  <img src="https://img.shields.io/badge/Gmail%20API-101018?style=for-the-badge&logo=gmail&logoColor=F0616D" alt="Gmail API"/>
  <img src="https://img.shields.io/badge/OpenAI-101018?style=for-the-badge&logo=openai&logoColor=F5F5F8" alt="OpenAI"/>
  <img src="https://img.shields.io/badge/Claude-101018?style=for-the-badge&logo=anthropic&logoColor=D06CC0" alt="Claude"/>
  <img src="https://img.shields.io/badge/n8n-101018?style=for-the-badge&logo=n8n&logoColor=F0616D" alt="n8n"/>
</p>

---

<p align="center">
  Built by <a href="https://github.com/ahmed-hussain-ai"><b>Ahmed Hussain</b></a> · <a href="https://ahmedhussain.tech">ahmedhussain.tech</a><br/>
  <sub>The source code is kept in a private repository. Happy to walk through it in an interview.</sub>
</p>
