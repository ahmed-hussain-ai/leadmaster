<p align="center">
  <img src="assets/hero.svg" alt="LeadMaster — AI cold-outreach engine. 8,778 emails sent, 3.7% reply rate, 11,978 leads processed, 17 campaigns" width="100%"/>
</p>

<p align="center">
  <a href="https://leadmaster.ahmedhussain.tech"><img src="https://img.shields.io/website?url=https%3A%2F%2Fleadmaster.ahmedhussain.tech&label=status&up_message=live&down_message=offline&up_color=3DD68C&style=for-the-badge&labelColor=101018" alt="Live status"/></a>
  <img src="https://img.shields.io/badge/In%20production-since%20April%202026-2FB980?style=for-the-badge&labelColor=101018" alt="In production since April 2026"/>
  <img src="https://img.shields.io/badge/Reply%20rate-3.7%25-3DD68C?style=for-the-badge&labelColor=101018" alt="Reply rate 3.7%"/>
  <img src="https://img.shields.io/badge/AI%20writing-Claude%20%2B%20GPT--4o-9B8CFF?style=for-the-badge&labelColor=101018" alt="AI writing"/>
</p>

<p align="center">
  <a href="#01"><b>Why</b></a> &nbsp;·&nbsp; <a href="#02"><b>Dashboard</b></a> &nbsp;·&nbsp; <a href="#03"><b>Features</b></a> &nbsp;·&nbsp; <a href="#04"><b>Pipeline</b></a> &nbsp;·&nbsp; <a href="#05"><b>Results</b></a> &nbsp;·&nbsp; <a href="#06"><b>Production</b></a> &nbsp;·&nbsp; <a href="#07"><b>Stack</b></a>
</p>

<br/>

<a id="01"></a>
<img src="assets/s01.svg" alt="01 · Why LeadMaster" width="100%"/>

**LeadMaster replaces manual lead research and copywriting for B2B cold outreach.** For every lead it reads their LinkedIn profile and company website, writes a personal first email with Claude or GPT-4o, sends from several Gmail inboxes, follows up three times in the same thread, and stops the moment the lead replies.

<p align="center"><img src="assets/problem-solution.svg" alt="Manual outreach vs LeadMaster" width="100%"/></p>

<br/>

<a id="02"></a>
<img src="assets/s02.svg" alt="02 · The live dashboard" width="100%"/>

<p align="center"><img src="assets/dashboard-framed.png" alt="LeadMaster production dashboard: 11,978 leads processed, 8,778 emails sent, 3.7% reply rate, 5 of 17 campaigns active" width="100%"/></p>
<p align="center"><sub>The production dashboard: leads processed, lifetime emails sent, reply rate across all campaigns, and leads grouped by industry.</sub></p>

<br/>

<a id="03"></a>
<img src="assets/s03.svg" alt="03 · What it does" width="100%"/>

<p align="center"><img src="assets/features.svg" alt="Lead management, research, AI writing, multi-inbox sending, follow-ups, analytics" width="100%"/></p>

<br/>

<a id="04"></a>
<img src="assets/s04.svg" alt="04 · How it works" width="100%"/>

<p align="center"><img src="assets/architecture.svg" alt="LeadMaster pipeline" width="100%"/></p>

<details>
<summary><b>The life of one lead</b> (state diagram)</summary>
<br/>

```mermaid
%%{init: {'theme':'dark', 'themeVariables': {'primaryColor':'#181822','primaryTextColor':'#F5F5F8','primaryBorderColor':'#2FB980','lineColor':'#3DD68C'}}}%%
stateDiagram-v2
    direction LR
    [*] --> Imported: CSV / Apify / Apollo
    Imported --> Researched: n8n reads LinkedIn + website
    Researched --> Drafted: Claude or GPT-4o writes
    Drafted --> Sent: Gmail inbox N
    Sent --> FollowUp: no reply yet
    FollowUp --> FollowUp: up to 3, same thread
    Sent --> Replied: reply matched by thread ID
    FollowUp --> Replied
    Replied --> [*]: sequence stops
    FollowUp --> Completed: no reply after 3
    Completed --> [*]
```

</details>

<br/>

<a id="05"></a>
<img src="assets/s05.svg" alt="05 · Results" width="100%"/>

<p align="center"><img src="assets/results.svg" alt="8,778 emails sent, 3.7% reply rate, 11,978 leads processed, 17 campaigns" width="100%"/></p>
<p align="center"><img src="assets/benchmark.svg" alt="LeadMaster's 3.7% reply rate vs the typical 1–3% for cold email" width="100%"/></p>

<br/>

<a id="06"></a>
<img src="assets/s06.svg" alt="06 · Built for production" width="100%"/>

| Decision | Why |
|---|---|
| **Research before writing** | A personal first line comes from real facts about the lead, not a merge field. That is what lifts replies above the usual 1–3%. |
| **Sending from real Gmail inboxes** | Mail comes from a real person's inbox, and volume is spread across several inboxes to protect deliverability. |
| **Threaded follow-ups** | Follow-ups land in the same thread, so the lead sees one conversation instead of four cold emails. |
| **Reply matching by thread ID** | Every inbox is scanned, and a reply stops that lead's sequence, so nobody gets a follow-up after answering. |
| **Background workers** | Sending and inbox scanning run in workers, so the dashboard never waits on Gmail. |
| **Per-campaign, per-day analytics** | Sends, replies and bounces show which segment and which message work, so campaigns change on results. |

<br/>

<a id="07"></a>
<img src="assets/s07.svg" alt="07 · Tech stack" width="100%"/>

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,fastapi,react,vite,tailwind,postgres,nginx,linux&theme=dark" alt="Python, FastAPI, React, Vite, Tailwind, PostgreSQL, Nginx, Linux"/>
</p>
<p align="center">
  <img src="https://img.shields.io/badge/Gmail%20API-101018?style=for-the-badge&logo=gmail&logoColor=F0616D" alt="Gmail API"/>
  <img src="https://img.shields.io/badge/n8n-101018?style=for-the-badge&logo=n8n&logoColor=F0616D" alt="n8n"/>
  <img src="https://img.shields.io/badge/OpenAI-101018?style=for-the-badge&logo=openai&logoColor=F5F5F8" alt="OpenAI"/>
  <img src="https://img.shields.io/badge/Claude-101018?style=for-the-badge&logo=anthropic&logoColor=D06CC0" alt="Claude"/>
  <img src="https://img.shields.io/badge/AG%20Grid-101018?style=for-the-badge" alt="AG Grid"/>
  <img src="https://img.shields.io/badge/Apify-101018?style=for-the-badge" alt="Apify"/>
</p>

<br/>

<p align="center">
  <a href="https://ahmedhussain.tech"><img src="assets/footer.svg" alt="Built by Ahmed Hussain with Maria Bano" width="100%"/></a>
  <br/><sub>The source code is private. Happy to walk through it in an interview.</sub>
</p>
