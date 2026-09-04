# My AI Product Strategy

> A living strategy built across 6 sessions. Each module adds one component. By Module 6, this repo IS your strategy — version-controlled, board-ready, portable.

---

## Strategy at a Glance

| Component | Module | Status | Key Artifact |
|-----------|--------|--------|-------------|
| **The Bet** | M1 | [x] | `01-the-bet/` |
| **The Moat** | M2 | [ ] | `02-the-moat/` |
| **The Margin** | M3 | [ ] | `03-the-margin/` |
| **The Contract** | M4 | [x] | `04-the-contract/` |
| **The Guardrails** | M5 | [ ] | `05-the-guardrails/` |
| **The Pitch** | M6 | [ ] | `06-the-pitch/` |

---

## The Bet (M1)

**What we're building, for whom, why now.**

- **Product:** SalesAssist — AI meeting notes, summary, and next-step generator for B2B sales teams.
- **AI Value Archetype:** Workflow automation + knowledge augmentation (summarization, action extraction, personalization).
- **Vulnerability Scores:** Moat 2/5 · Data 4/5 · Platform 3/5
- **Top Risk:** Incorrect action items (hallucinated next steps) or privacy concerns from ingesting customer data.
- **Confidence:** M
- **Prototype:** https://prototype.example.com/salesassist (placeholder)
- **Kill Criteria:** Retention < 20% at 3 months; more than 1 high-severity hallucination per 100 active sessions; unresolved data privacy blockers.

Example product that helps in this module

SalesAssist is a focused product that demonstrates how to use small, high-ROI AI features to prove a bet fast:

- Problem: Sales teams spend hours writing meeting notes and following up with manual next-step tracking.
- Solution: Use ASR + LLM summarization to produce accurate, timestamped notes, extract action items, and propose personalized next steps and templates for outreach.
- Why now: Improvements in ASR for noisy conference calls, cheap LLM inference, and available CRM integrations create a low friction path to value.
- Early success metric: % of meetings where users accept at least one generated action item within 48 hours.

→ Details: [`01-the-bet/`](01-the-bet/)

---

## The Moat (M2)

**Why this won't get copied in 6 months.**

- **Data Flywheel Score:** __/20
- **Weakest Loop:**
- **Competitive Position:** [describe axes + placement]
- **Encroachment Defense:**
- **Vendor Portability:** Ready / Partial / Locked

→ Details: [`02-the-moat/`](02-the-moat/)

---

## The Margin (M3)

**Will this make money or bleed it?**

- **Gross Margin (current):**
- **Gross Margin (AI-adjusted):**
- **Pricing Model:**
- **Cascading Strategy:**
- **Break-even at:**

→ Details: [`03-the-margin/`](03-the-margin/)

---

## The Contract (M4)

**Why users will trust a probabilistic system.**

This module includes a Golden Dataset Builder to curate evaluation data: examples with inputs, known-correct outputs, edge cases, and judge types. Use the dataset to measure accuracy, surface adversarial failures, and define clear kill/accept criteria.

- **Reliability Target:**
- **Golden Dataset:** See `04-the-contract/GOLDEN_DATASET.md` for the builder, templates, and dataset health guidance.
- **Confidence UX:** [approach]
- **HITL Architecture:**
- **Failure Mode Coverage:**

→ Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)

**What breaks when this scales — and what compounds.**

- **Compounding System:** [describe feedback loops]
- **Governance Posture:** [approach]
- **Shadow AI Status:** __ tools found, __ triaged
- **Agent Boundaries:**
- **Regulatory Exposure:**

→ Details: [`05-the-guardrails/`](05-the-guardrails/)

---

## The Pitch (M6)

**How you get this funded, shipped, and adopted.**

- **Horizon 1 (Now):**
- **Horizon 2 (Next):**
- **Horizon 3 (Bet):**
- **Board Narrative:** [1-sentence thesis]
- **Key Metric:**

→ Details: [`06-the-pitch/`](06-the-pitch/)
