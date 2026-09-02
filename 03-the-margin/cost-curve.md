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
| | Complex | Frontier | Premium accuracy required, lower volume justifies cost | $_____ | __% | $_____ |
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

**Current pricing:**
**Proposed AI pricing:**
**Model:** seat-based / usage-based / outcome-based / hybrid

## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x | | |
| Heaviest segment doubles | | |
| Model provider raises prices 50% | | |

## Board One-Pager
<!-- Before/After: Old SaaS revenue vs. AI usage revenue for your product -->

**Before (traditional SaaS):**
**After (AI-enabled):**
**Net margin shift:**
