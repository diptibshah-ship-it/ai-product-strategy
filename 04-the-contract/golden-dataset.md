# Golden Dataset & Reliability Contract

## Golden Dataset Spec

| # | Input | Expected Output | Edge Case? | Judge Type |
|---|-------|----------------|-----------|-----------|
| 1 | | | Y/N | rule / LLM |
| 2 | | | Y/N | rule / LLM |
| 3 | | | Y/N | rule / LLM |
| 4 | | | Y/N | rule / LLM |
| 5 | | | Y/N | rule / LLM |

**Adversarial rows included:** __
**Coverage gaps identified by partner:**

## Confidence UX Design

**Approach:** Tiered confidence with reasoning transparency and human-in-loop escalation. Show uncertainty early. Hedge language for uncertain outputs. Route low-confidence cases to human review or request clarifying input before customer-facing content is generated.

### High Confidence (>90%)
**UI State:** Green badge "Confident"  
**Output Behavior:** Full, direct answer. Surface evidence and key drivers. Enable inline approval/rejection with quick-action buttons ("Approve," "Edit," "Reject").  
**Language:** Affirmative tone. "Based on [X evidence], the answer is [Y]."  
**AI Guardrails:** Generate proactively. Show citations and confidence score.

### Medium Confidence (70-90%)
**UI State:** Yellow badge "Uncertain" with an evidence panel.  
**Output Behavior:** Soften recommendations. Highlight key drivers and gaps. Request one clarifying input before proceeding (e.g., "Do you have budget constraints?" or "Is speed or quality the priority?").  
**Language:** Hedged tone. "Based on available data, [answer] is likely, but consider [caveat]."  
**AI Guardrails:** Don't auto-generate customer-facing content. Show alternative interpretations. Flag which inputs are missing or weak.

### Low Confidence (<70%)
**UI State:** Red badge "Not Confident" with escalation prompt.  
**Output Behavior:** Don't generate. Instead show:  
  - What evidence is missing (e.g., "No recent data for [X]")  
  - Recommended clarifications (e.g., "Provide last 3 months of usage logs")  
  - Option to escalate to human expert or retry after input.  
**Language:** Transparent. "Insufficient evidence to recommend. Please provide [X] or escalate to [team]."  
**AI Guardrails:** Block generation. Queue for HITL review.

### User Control Surface
- **Confidence threshold slider:** Users can adjust the threshold (e.g., "Show me answers >50% confidence" for exploration, ">90%" for critical decisions).
- **Reasoning transparency:** Every output includes an expandable "Why?" panel showing top 3–5 drivers, evidence strength, and missing signals.
- **Feedback loop:** Buttons on each output: "Accurate," "Wrong driver," "Missing context," "Too aggressive," "Not actionable." Labels auto-tag corrections and feed back into evaluation datasets.
- **Override capability:** Users can approve medium/low confidence outputs manually; these approvals become training signals (with user consent).
- **Escalation:** Low-confidence cases route to expert queue with 1-click handoff; SME feedback updates the model.

## Reliability Contract

| Metric | Target | Measurement | Alert Threshold |
|--------|--------|-------------|-----------------|
| Accuracy | | | |
| Hallucination rate | | | |
| Latency (p95) | | | |
| Drift velocity | | | |

## HITL Architecture
<!-- When does a human step in? What's the escalation path? -->

## Red-Team Findings
*What failure mode did your partner find that you missed?*
