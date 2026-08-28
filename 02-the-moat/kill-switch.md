# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|---------------|------------|----------------|
| **Provider (Cloud + CDN)** | Primary infra on AWS (EC2/EKS), S3 for asset storage, and CloudFront as primary CDN; selective multi-CDN failover (Fastly/Cloudflare) in high-priority markets. | H | Validate S3 replication, verify multi-CDN routing rules, run playback smoke tests from backup CDN endpoints; prepare pre-signed URL failover playbook. |
| **Abstraction (Playback & DRM)** | Custom player with integrations to Widevine, PlayReady, FairPlay; licensing servers mixed in-house + vendor-managed. | M | Ensure DRM license server redundancy and hot-standby credentials; export player artifact bundle and create a fallback player configuration that removes non-critical features. |
| **Routing (Device integrations / Discovery)** | Heavy reliance on OEM placement (Roku, Samsung, Apple TV, Android TV), remote shortcuts, and platform recommendation surfaces. | H | Audit placement agreements, prepare owned-channel deep-link campaigns (mobile push, email, QR quick-start flows), and test app-opening deeplinks for critical titles. |
| **Eval (ML training & experiments)** | In-house experimentation and retraining pipelines (batch GPUs; managed services for some experiments). | M | Snapshot and archive model artifacts to cross-region durable storage; pin production model versions and verify inference fallback on CPU-only instances. |
| **Content Licensing** | Mix of Originals and licensed third-party content; many third-party rights are time-limited and region-specific. | H | Inventory contracts expiring in 12–24 months, prepare content-priority comms, and secure emergency rights negotiation playbook for high-value titles. |
| **Monetization / Billing** | Multiple global PSPs + Stripe; entitlement service reliant on central auth + billing endpoints. | M | Validate PSP failover routing, run test transactions, and prepare token-caching policy to preserve access during short auth outages. |

## Portability Score
Partial (3/5) — Core services (recommendation, storage, compute) are portable with engineering effort; greatest blockers are DRM ecosystems, device-ecosystem dependencies, and non-technical constraints (content-rights agreements).

## If a primary vendor doubles pricing tomorrow
48-hour response:
- Enact emergency cost-control: throttle non-essential batch jobs, pause non-critical experiments, reduce log retention and verbosity.
- Shift non-latency-critical ingestion/transcoding to cheaper capacity or queued batch; route non-critical traffic through backup CDN for lower-cost regions.
- Preserve playback: maintain hot paths for license servers and playback endpoints; ensure critical caches are retained in hot storage tiers.
- Finance/legal engage vendor for temporary credits/discounts; enable fast procurement/spot-reserve actions.
Longer term:
- Accelerate multi-cloud migration for non-critical workloads, optimize transcoding and storage pipelines, and negotiate committed discounts.

## If a primary vendor ships a competing product or changes discovery to favor their service
What they can replicate:
- OS-level discovery, home-screen placement, remote shortcuts, and frictionless one-click playback — platform owners control these affordances and can favor their own services.
Hard to replicate quickly:
- Years of long-form viewing telemetry (per-second attention, rewatch patterns) tied to a global Originals pipeline; the creative feedback loop from engagement → commissioning → performance.
48-hour defensive posture:
- Commercial: open emergency talks to preserve placement; offer targeted promo windows backed by data showing incremental retention.
- Product/Growth: launch owned-channel acquisition pushes (push/email/social), surface high-lift Originals in app and owned surfaces, and accelerate deep-link campaigns.
- Engineering: deploy quick home-row UX experiments and create campaign deep-link endpoints for partners to use in landing experiences.
Why they struggle to kill quickly:
- Building comparable Originals slate and long-form signal at scale requires years and significant capital; user destination value and historical personalization are durable.

## If a vendor executes a technical kill-switch (sudden service stop)
Immediate priorities (first 48 hours):
1. Scope: identify affected regions/services and impact on playback, DRM, auth, or CDN.
2. Failover: route traffic to backup CDNs, switch license checks to hot-standby DRM endpoints, and use cached entitlement tokens to avoid mass cancellations.
3. Preserve revenue: keep entitlements valid for active subscribers (grace tokens) while fixes are implemented.
4. Communication: status page updates, proactive customer messaging for impacted regions, and internal incident bridge.
Next 72 hours:
- Run rollback and patch playbooks; execute RTO paths (playback fallbacks, degraded UX but functional playback).
- Engage vendor, request remediation/credits, and escalate procurement/legal options.
Post-incident (days 3–30):
- RCA, policy/procurement updates, and accelerate removal of single points of failure identified during incident.

## Summary and Recommended Next Steps (30/90 day horizon)
- Harden multi-CDN coverage and automated cutover playbooks; test cutovers regularly and document runbooks.
- Improve DRM and license-server redundancy; standardize provisioning across geographies and vendors.
- Build and test a lightweight fallback player (reduced features, robust playback) that can be pushed via feature-flag for outages.
- Productize owned discovery channels: richer push/email campaigns, social deep-linking, and watch-party primitives to reduce device-surface reliance.
- Negotiate contract amendments to include portability clauses, kill-switch protections, and stronger SLAs/credits.
- Invest in measurement to quantify the incremental value of platform placements to strengthen commercial negotiations.

Portability summary: Partial (3/5) — technically feasible to migrate most infra but non-technical dependencies (content rights, platform placement) present the largest barriers.
