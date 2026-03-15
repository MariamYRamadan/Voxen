# Voxen — AI Customer Intelligence Platform

> Transforms raw customer feedback into prioritized feature backlogs, sprint boards, competitive insights, and responsible AI audits — in seconds.

![Version](https://img.shields.io/badge/version-8.0-f97316?style=flat-square) ![Stack](https://img.shields.io/badge/stack-Vanilla%20JS-f97316?style=flat-square) ![AI](https://img.shields.io/badge/AI-Powered-ec4899?style=flat-square) ![Responsible AI](https://img.shields.io/badge/Responsible%20AI-Audited-fbbf24?style=flat-square)

**Live demo:** [mariamyramadan.github.io/Voxen](https://mariamyramadan.github.io/Voxen)

---

## Problem Statement

Product teams collect enormous volumes of customer feedback — support tickets, NPS surveys, app store reviews, user interviews — but lack a fast, consistent way to extract signal from the noise. PMs often spend hours manually tagging themes and estimating priorities before a single sprint can be planned.

**Voxen solves this end-to-end:**

- Classifies sentiment at scale with per-feature confidence scores
- Extracts and ranks feature requests using a weighted priority scoring model
- Auto-generates user stories, acceptance criteria, and story points
- Groups stories into product epics by theme
- Produces a 3-month AI-generated roadmap
- Surfaces responsible AI limitations so teams decide with appropriate confidence

---

## What's Inside

| Section | Description |
|---|---|
| **Raw Feedback Dataset** | 6 tagged customer entries with sentiment and friction labels |
| **NLP Extraction Pipeline** | Shows how the AI extracts features and severity signals from text |
| **KPI Overview** | Positive %, Negative %, Features extracted, Estimated NPS |
| **Sentiment Charts** | Donut (sentiment split) + bar chart (feature mentions by priority) |
| **Weekly Complaint Trend** | 5-week escalation chart with severity signal breakdown |
| **AI Priority Score Formula** | Weighted algorithm: Mentions × 3 + Sentiment × 2 + Churn Risk × 5 + Impact × 4 |
| **Impact × Effort Matrix** | Do Now / Plan Next / Quick Win prioritization framework |
| **Feature Backlog + Evidence** | 6 ranked features with supporting customer quotes and AI confidence % |
| **AI-Generated Epics** | 3 epics with goals and stories grouped by theme |
| **Customer Journey Friction Map** | 4-stage journey showing exactly where users struggle |
| **Competitive Intelligence** | Signal, Opportunity, Risk, and Moat strategy cards |
| **Customer Segment Analysis** | Enterprise, SMB, Mobile, Power Users — impact by segment |
| **Retention Impact Analysis** | Per-feature retention risk + AI confidence bars |
| **Feature Mention Trend** | Week-over-week emerging vs declining requests |
| **Themes + PM Recommendation** | Key themes and a full first-person PM recommendation |
| **Agile Sprint Backlog** | User stories + acceptance criteria + story points, Jira-ready |
| **3-Month Roadmap** | AI-generated roadmap with sprint velocities per month |
| **AI Product Brief** | Downloadable one-page product summary |
| **AI PM Assistant** | Ask questions about the dataset — decision-oriented answers |
| **Responsible AI Audit** | Confidence scores, bias flags, transparency disclosure, human oversight |

---

## Priority Scoring Model

```
Priority Score =
  (Feature Mentions    × 3)
  + (Negative Sentiment  × 2)
  + (Churn Risk Score    × 5)
  + (Product Impact      × 4)
```

This makes prioritization transparent and auditable — not just a ranked list.

---

## How It Works

```
Paste raw customer feedback
         ↓
AI classifies sentiment, extracts features,
detects severity signals and churn language
         ↓
Weighted scoring model ranks features
by business impact and user urgency
         ↓
App generates charts, backlog, epics,
roadmap, and responsible AI audit
         ↓
PM exports CSV → imports to Jira for sprint planning
```

**Technical stack:**
- Vanilla HTML / CSS / JavaScript — zero build step, zero dependencies
- Chart.js 4.4 for data visualization
- Clash Display + Inter + JetBrains Mono type system
- 8px spacing grid, 4-level surface hierarchy, SVG icon system

---

## Agile Process — How This Was Built

Developed across 3 simulated sprints:

### Sprint 1 — Discovery & Core Analysis

| ID | User Story | Points | Status |
|---|---|---|---|
| US-001 | As a PM, I want sentiment classified from raw text, so I can understand user mood at scale | 5 | Done |
| US-002 | As a PM, I want feature requests extracted and ranked, so I can prioritize my roadmap | 8 | Done |
| US-003 | As a PM, I want a weighted priority score formula, so prioritization is transparent and defensible | 5 | Done |

### Sprint 2 — Visualization, Backlog & Roadmap

| ID | User Story | Points | Status |
|---|---|---|---|
| US-004 | As a PM, I want sentiment and feature charts, so I can share findings in stakeholder decks | 5 | Done |
| US-005 | As a PM, I want auto-generated user stories with acceptance criteria, so I can start sprint planning | 8 | Done |
| US-006 | As a PM, I want an AI-generated 3-month roadmap, so I can align the team on sequencing | 8 | Done |
| US-007 | As a PM, I want CSV export, so I can import the backlog into Jira or Linear | 3 | Done |

### Sprint 3 — Intelligence, AI Audit & Polish

| ID | User Story | Points | Status |
|---|---|---|---|
| US-008 | As a PM, I want per-feature AI confidence scores with evidence, so I know when to validate | 5 | Done |
| US-009 | As a PM, I want retention impact and competitive intelligence, so I can make business-level arguments | 8 | Done |
| US-010 | As a stakeholder, I want bias flags and a responsible AI audit, so I trust the outputs | 5 | Done |
| US-011 | As a user, I want an AI PM Assistant I can query, so I get decision-oriented answers instantly | 8 | Done |

---

## Responsible AI Design

Responsible AI was embedded from the start — not added as an afterthought.

**Transparency:** Every analysis includes model confidence scores and explicit AI limitations. Users are reminded outputs require human validation before sprint commitment.

**Bias awareness:** The tool surfaces potential bias flags — vocal minority effects, single-channel sampling risk, and demographic data gaps.

**Data minimization:** No feedback data is stored, logged, or transmitted to any third party. Every session is fully ephemeral.

**Human oversight:** Story point estimates are explicitly labeled as illustrative. The sprint board is a starting point for team estimation, not a substitute.

**Confidence methodology:** Scores are derived from keyword frequency, sentiment intensity, cross-entry agreement, and churn language detection — all explained in the audit panel.

**Frameworks referenced:**
- IBM AI Ethics principles
- EU AI Act transparency requirements
- NIST AI Risk Management Framework

---

## Getting Started

```bash
git clone https://github.com/MariamYRamadan/Voxen.git
cd Voxen
open index.html
```

No build step. No install. Works in any modern browser. Click **Analyze Feedback** — demo loads automatically.

---

## Product Learnings

**Translating ML outputs into PM artifacts.** The hardest part was not calling the model — it was designing the scoring logic so AI outputs mapped directly to business decisions without manual post-processing.

**Responsible AI is a trust problem, not a compliance checkbox.** A model that surfaces confident but wrong priorities destroys PM credibility faster than a bug. Confidence scores and bias flags made the tool more trustworthy — not more complicated.

**Visualization changes decisions.** The bar chart of feature mentions by priority made the prioritization argument immediately obvious. The best PM tools make the right decision feel inevitable.

**Churn signals matter more than mention counts alone.** Adding churn risk as a scoring dimension (×5 weight) completely changed the ranking. "Dashboard Performance" had 5 mentions but the cancellation language in F001 made it 4× more urgent than "Dark Mode" with 2 mentions. That's the difference between counting and understanding.

---

## Roadmap

- Real-time API integration with Zendesk, App Store, and Slack
- Multi-session history with trend detection
- Competitive analysis mode — compare two products' feedback
- PDF stakeholder report export
- RICE and ICE scoring overlays
- Team collaboration mode

---

## License

MIT — free to use, fork, and build on.

---

*Built by Mariam Ramadan · IBM Product Manager Intern 2026*
