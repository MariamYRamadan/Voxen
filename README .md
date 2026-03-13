# Voxen — AI-Powered Customer Intelligence Platform

> A product management tool that transforms raw customer feedback into prioritized feature backlogs, sentiment visualizations, Agile sprint boards, and responsible AI audits — built for data-driven PMs.

![Voxen](https://img.shields.io/badge/Voxen-Customer%20Intelligence-7c6ef7?style=flat-square) ![Agile](https://img.shields.io/badge/Methodology-Agile%2FScrum-a78bfa?style=flat-square) ![Responsible AI](https://img.shields.io/badge/Responsible%20AI-Audited-fbbf24?style=flat-square)

**Live demo:** [mariamyramadan.github.io/Voxen](https://mariamyramadan.github.io/Voxen)

---

## Problem Statement

Product teams collect enormous volumes of customer feedback — support tickets, NPS surveys, app store reviews, user interviews — but lack a fast, consistent way to extract signal from the noise. PMs often spend hours manually tagging themes and estimating priorities before a single sprint can be planned.

**Voxen solves this by using a large language model to:**
- Classify sentiment at scale
- Extract and rank feature requests by mention frequency
- Auto-generate user stories and story point estimates
- Surface responsible AI limitations so teams make decisions with appropriate confidence

---

## Features

| Feature | Description | JD Alignment |
|---|---|---|
| **Sentiment Analysis** | Positive / Negative / Neutral breakdown with donut chart | Analytics & data visualization |
| **Feature Prioritization** | High / Med / Low ranked by user mentions, with bar chart | Roadmap planning & prioritization |
| **Agile Sprint Board** | Auto-generated user stories, acceptance criteria, story points | Agile ceremonies & sprint planning |
| **Responsible AI Audit** | Confidence scores, bias flags, data minimization disclosure | Responsible & ethical AI practices |
| **CSV Export** | Download sprint backlog for Jira/Linear import | Cross-functional collaboration |
| **Sample Dataset** | Pre-loaded SaaS platform demo data | User-centered thinking |

---

## How It Works

```
User pastes feedback
        ↓
AI model classifies sentiment,
extracts features, generates user stories
        ↓
App renders charts (Chart.js), sprint board,
and responsible AI audit panel
        ↓
PM exports CSV → imports to Jira for sprint planning
```

**Technical stack:**
- Vanilla HTML/CSS/JavaScript (zero dependencies except Chart.js)
- Large language model API via REST
- Chart.js for data visualization
- Structured JSON prompt engineering for consistent AI outputs

---

## Agile Process — How This Project Was Built

This project was developed using Agile methodology across 3 simulated sprints:

### Sprint 1 — Discovery & MVP
**Sprint Goal:** Validate that LLM-based feedback classification produces actionable PM outputs.

| ID | User Story | Points | Status |
|---|---|---|---|
| US-001 | As a PM, I want to paste raw feedback and get sentiment scores, so I can quickly understand user mood | 5 | Done |
| US-002 | As a PM, I want feature requests extracted and ranked, so I can prioritize my roadmap | 8 | Done |
| US-003 | As a PM, I want sample feedback datasets, so I can demo the tool without real data | 3 | Done |

### Sprint 2 — Data Visualization & Agile Export
**Sprint Goal:** Make insights visual and actionable for engineering handoff.

| ID | User Story | Points | Status |
|---|---|---|---|
| US-004 | As a PM, I want a sentiment donut chart, so I can share findings in stakeholder decks | 5 | Done |
| US-005 | As a PM, I want a feature mention bar chart, so I can justify prioritization decisions with data | 5 | Done |
| US-006 | As a PM, I want auto-generated user stories with story points, so I can start sprint planning immediately | 8 | Done |
| US-007 | As a PM, I want to export the backlog as CSV, so I can import it into Jira or Linear | 3 | Done |

### Sprint 3 — Responsible AI & Polish
**Sprint Goal:** Ensure the tool meets responsible AI standards before stakeholder demo.

| ID | User Story | Points | Status |
|---|---|---|---|
| US-008 | As a PM, I want to see model confidence scores, so I know when to validate AI outputs with more research | 5 | Done |
| US-009 | As a stakeholder, I want bias flags surfaced automatically, so I can make decisions with appropriate caution | 5 | Done |
| US-010 | As a user, I want a clear data privacy disclosure, so I know my feedback data is not stored | 3 | Done |

---

## Responsible AI Design

Voxen was built with responsible AI principles embedded in the product — not bolted on as an afterthought.

**Transparency:** Every analysis includes a model confidence score and explicit limitations. Users are reminded that AI outputs require human validation before roadmap commitment.

**Bias awareness:** The tool surfaces potential bias flags per analysis — for example, vocal minority effects, small sample size warnings, and language representation issues.

**Data minimization:** No feedback data is stored, logged, or transmitted to any third party. The session is fully ephemeral.

**Human oversight:** Story point estimates are explicitly labeled as illustrative. The sprint board is a starting point for engineering discussion, not a substitute for team estimation.

**Ethical AI frameworks referenced:**
- IBM AI Ethics principles (ibm.com/artificial-intelligence/ethics)
- EU AI Act transparency requirements for AI-assisted decision tools
- NIST AI Risk Management Framework

---

## Getting Started

1. Clone this repo:
```bash
git clone https://github.com/MariamYRamadan/Voxen.git
cd Voxen
```

2. Open `index.html` in your browser — no build step, no install needed.

3. Click **Analyze Feedback** — the demo loads automatically.

---

## Product Learnings

Building Voxen reinforced three core PM skills:

**Translating ML outputs into user value.** The hardest part was not calling the API — it was designing the JSON schema so the model's outputs mapped directly to PM artifacts (user stories, acceptance criteria, sprint goals) without post-processing.

**Responsible AI is a product quality issue.** A model that surfaces confident but wrong priorities erodes trust faster than a bug. Adding confidence scores and bias flags made the tool more trustworthy, not more complicated.

**Data visualization changes decisions.** The bar chart of feature mentions by priority made the prioritization argument instantly obvious in a way that a numbered list never could. Good PM tools make the right decision feel obvious.

---

## Roadmap (Backlog)

- Multi-session history
- Competitive analysis mode (compare two products' feedback)
- Slack integration to pull feedback from support channels
- PDF stakeholder report export
- RICE scoring calculator overlay

---

## License

MIT — free to use, fork, and build on.

---

*Built by Mariam Elsayed*
