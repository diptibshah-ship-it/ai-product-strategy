# Cost Curve & Pricing Strategy

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) | | |
| Inference (cascading/triage) | | |
| Infrastructure | | |
| Data/storage | | |
| Human-in-the-loop | | |
| **Total AI COGS** | | |

## Feature Cost Mapping

| Feature | Complexity | Model Tier | Why Cheaper Model? | Cost/Req | Volume % | Weighted |
|---------|-----------|-----------|-------------------|----------|----------|----------|
| | Simple | Small | Reduce COGS, high volume, acceptable latency | $_____ | __% | $_____ |
| | Medium | Mid | Balance quality vs. cost, handles most cases | $_____ | __% | $_____ |
| | Complex | Frontier | Premium accuracy required, lower volume justifies cost | $_____ | __% | __% | $_____ |
| | | | | | **100%** | **$_____** |

**Why cheaper models matter:**
- **Volume:** 70-80% of requests can run on small/mid models (no UX degradation)
- **Margin protection:** Cheaper tiers drop COGS by 10-50x vs. frontier-only
- **Latency:** Small models = faster inference (bonus)
- **Resilience:** Diversified model portfolio = less dependency on single provider

## Cascading Strategy
<!-- Cheap model → frontier model routing logic -->

**Triage model:**
**Frontier model:**
**Routing rule:**
**Expected cascade ratio:** __% / __%

## Pricing Model

### 1. Pricing Strategy Posture

Choose one:
- ☐ **Skim:** Launch premium, lower over time (signal quality) — e.g. Apple, Porsche
- ☐ **Penetrate:** Price low, win volume, optimize costs (race to efficiency) — e.g. Amazon, AWS
- ☐ **Maximize:** Balance revenue & market position (optimize current position) — e.g. Microsoft, HubSpot

**Selected posture:** _____

### 2. How You Charge (Customer Perception)

Choose one:
- ☐ **Seat / Access:** Per user, flat monthly. Human drives the tool.
  - e.g. Figma ($12-$180/user/month), Slack, Notion
  
- ☐ **Hybrid (Base + Usage):** Platform fee + metered AI work.
  - e.g. HubSpot ($50 + $0.50/call), Canva AI, Grammarly
  
- ☐ **Outcome / Resolution:** Pay only when AI delivers the result.
  - e.g. Intercom Fin, Harvey (pay-per-resolution)

**Selected model:** _____

### 3. Pricing Structure

| Component | Value | Notes |
|-----------|-------|-------|
| **Base fee** | $_____ / month | Platform access fee (if hybrid) |
| **Unit of work** | _____ | e.g. resolved conversations, reports generated, workflows completed |
| **Price per unit** | $_____ | Cost to customer per outcome unit |
| **Estimated units/user/month** | _____ | e.g. 120 units/month |
| **Implied revenue/user/month** | $_____ | (Base) + (Units × Price) |

**Key principle:** Name the customer outcome, not the internal model action.
- ✅ "Report generated" (customer sees value)
- ❌ "GPT-4 API call" (internal implementation)

---

## Board One-Pager: Before vs. After

### Before (Traditional SaaS)

| Metric | Value | Formula |
|--------|-------|---------|
| **Revenue per seat** | $_____ / month | Fixed annual contract ÷ 12 |
| **Number of seats** | _____ | Your current customer base |
| **Total revenue** | $_____ / month | Revenue per seat × Seats |
| **COGS (fixed)** | $_____ / month | Server hosting, support, etc. |
| **Gross profit** | $_____ / month | Revenue − COGS |
| **Gross margin %** | ____% | (Gross profit ÷ Revenue) × 100 |

**Narrative:** Traditional SaaS relies on seat-based pricing with predictable, fixed COGS. Margin is stable but limited by CAC/retention constraints.

---

### After (AI-Powered)

| Metric | Value | Formula |
|--------|-------|---------|
| **Base fee** | $_____ / month | Platform access (per seat or flat) |
| **Outcome units/user/month** | _____ | e.g., 120 reports/conversations |
| **Price per outcome unit** | $_____ | e.g., $0.50/report |
| **Variable revenue per user** | $_____ | Units × Price per unit |
| **Total revenue per user** | $_____ | Base + Variable |
| **Total revenue** | $_____ / month | (Base + Variable) × Users |
| **COGS (variable)** | $_____ / month | Blended inference cost × usage |
| **Gross profit** | $_____ / month | Revenue − COGS |
| **Gross margin %** | ____% | (Gross profit ÷ Revenue) × 100 |

**Narrative:** AI-powered model splits revenue (base + usage) and COGS becomes variable. Usage scales independently of seats, creating operating leverage.

---

### Net Margin Shift

| Metric | Change |
|--------|--------|
| **Δ Gross Margin %** | ±____% |
| **Δ Gross $ per Month** | $_____ |
| **NRR Impact** | ___% (net revenue retention) |

**Narrative** *(fill in one or more)*:

**Why margin % moves:**
- [ ] Blended COGS per user drops because cheaper models handle 70% of work
- [ ] Usage scales faster than seat count (operating leverage)
- [ ] Pricing power improves: AI outcomes command premium vs. access
- [ ] Risk: If COGS is higher than expected, margin compresses

**Gross $ / NRR wins:**
- [ ] Expansion revenue from power users (high outcome volume)
- [ ] Cross-sell to adjacent products (AI + existing feature)
- [ ] Lower churn: AI outcomes create stickiness
- [ ] Risk: If usage doesn't scale, revenue stays flat

**Hedge:**
- [ ] Monitor COGS ratio: if inference costs > 30% of gross revenue, tighten pricing or re-route to cheaper models
- [ ] Set outcome unit caps to prevent COGS blow-outs
- [ ] Diversify models (avoid single provider dependency)
- [ ] Lock in volume discounts with LLM providers now

---

## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x | | |
| Heaviest segment doubles | | |
| Model provider raises prices 50% | | |
