# Data Flywheel Map

> Score each loop 1-5. Your weakest loop is where competitors attack first.
> The four loops below are the M2 starting point - adapt if your product has 2 or 6 loops instead of 4.

## Flywheel Loops

| Loop | What It Measures | Score 1 | Score 5 | Score |
|------|------------------|---------|---------|-------|
| **Correction** | Do users fix AI outputs? Is that signal captured and reused? | No capture | Automated retraining | 4/5 |
| **Preference** | Does the product learn individual / team preferences over time? | Stateless | Deep personalization | 5/5 |
| **Domain Context** | Does usage in one area improve quality in adjacent areas? | Siloed | Cross-domain transfer | 4/5 |
| **Network** | Does each new user / team make the product better for everyone? | Isolated | Strong network effects | 2/5 |

### Correction Loop - 4/5
**What you capture today:**
- Implicit corrections: per-second attention, session completion, rewatches, fast-forwards, and drop-off points captured at scale.
- Explicit signals: thumbs-up/thumbs-down, "Not interested" flags, and short surveys after recommendations or new releases.
- A/B test outcomes and experiment telemetry feed ML pipelines for model updates.

**How it compounds:**
- Operationalizes creative and ranking improvements: editorial and ML teams use large-scale correction signals to refine candidate generation and ranking models, reducing poor recommendations and improving content matching over time. This closes the loop from production performance back into training data.

### Preference Loop - 5/5
**What you capture today:**
- Rich user-level preference profiles: viewing histories across devices, watch time by title/season/episode, genre affinities, time-of-day patterns, and user-level metadata (profiles, kids vs adult profiles).
- Cross-device identity stitching and retention of personalization artifacts (playback position, bookmarks, playlists).

**How it compounds:**
- Personalization improves content discovery and retention, which drives more viewing and more signal. Tailored recommendations increase engagement, enabling better content investment decisions and more successful Originals, which further reinforce personalization.

### Domain Context Loop - 4/5
**What you capture today:**
- Content-level metadata (cast, director, pacing, keywords), creative signals (where viewers drop off, rewatch spikes), and co-viewing sequences that reveal multi-title affinities.
- Localization signals and regional performance that inform content commissioning in local languages.

**How it compounds:**
- Insights transfer across markets and genres to seed recommendations for new titles or markets. Creative signals inform production (editing, pacing, casting) that produces titles more likely to perform globally or in target regions.

### Network Loop - 2/5
**What you capture today:**
- Limited global network effects: shared catalogs and public popularity charts, but weak social graph integration (no platform-native social network beyond basic sharing links and watch parties in some markets).
- Account-sharing behaviors create usage concentration but do not reliably generate acquisition or personalization benefit across distinct social circles.

**How it compounds:**
- Today, new users indirectly add signal to global popularity metrics, but there is little direct mechanism where one user's activity materially improves relevance for another user outside aggregated trends. This makes the network loop the weakest lever.

**Total Flywheel Score: 15/20**
**Weakest Loop:** Network (2/5)
**Fix for weakest loop:** Prioritize features that create explicit, permissioned social signals and cross-user relevance: native watch parties and co-watching primitives, richer friend/family recommendations, creator-led communities around titles, and opt-in social feeds that link actions (reviews, clips, lists) to discoverability. Measure lift in referral and time-to-first-return after social interactions.

---

## Encroachment Threat Assessment

### 1. Platform Encroachment
**Attacker:** Apple / Google / Roku
**Vector:** OS or device-level discovery (home screen recommendations, voice assistants, remote shortcuts), pre-install prominence, and deep-linking to platform-first content.
**Time-to-threat:** 3-12 months (platforms can push UI changes quickly via firmware or app-store promotion cycles).
**% of value at risk:** 25-40% — visibility and ease-of-access loss can materially reduce new-user acquisition and casual viewing sessions.

### 2. Vertical Competitor
**Attacker:** Disney+ / Amazon Prime Video / Warner Bros Discovery (Max)
**Vector:** Exclusive licensing, sequenced release calendars, aggressive bundling (Disney bundle, Prime perks), and leveraging owned IP to lock global franchises.
**Time-to-threat:** 6-24 months (content slates and licensing deals take time but move fast when prioritized).
**% of value at risk:** 30-50% — loss of key titles or audience favorites can drive churn in core demographics.

### 3. Adjacent Expansion
**Attacker:** TikTok / YouTube / Meta
**Vector:** Expand short-form success into long-form or premium scripted content; leverage social distribution and creator ecosystems to surface original long-form that competes for attention.
**Time-to-threat:** 12-36 months (requires investment in production and long-form UX, but distribution power is already there).
**% of value at risk:** 10-30% — attention diversion reduces session time and discovery efficacy.

---

## 90-Day Encroachment Plan

*Your partner played the Big Tech attacker. What was their plan to kill you?*

**Attacker:** Apple (example)
**Attack vector (target the weakest loop):** Ship OS-level discovery and shortcuts that favor Apple TV+ and platform partners, and add native recommendation widgets on TV home screens to surface competing titles before users open apps — effectively stealing discovery and reducing Netflix’s ability to surface personalized recommendations.

**Weeks 1-4 - what they ship:**
- Home-screen recommendation widgets and a prioritized app row that surfaces a unified "Watch" carousel powered by Apple algorithms, with partner slots for featured titles.
- Siri suggestions that deep-link to Apple TV+ or promoted partner content.

**Weeks 5-8 - how they poach users:**
- Drive trial and conversion through one-click playback from home/lock screen widgets and promotional banners for Apple TV+ exclusives; advertise bundles (Apple One) that include Apple TV+ and other services.
- Surface shorter friction purchase/subscription flows tied to Apple ID.

**Weeks 9-12 - why users don't come back:**
- Users habitually start playback from the OS-level surface; the friction of opening Netflix and surfacing Originals increases. Paired with a steady drip of compelling exclusives and bundle pricing, casual users and newly onboarded households anchor to the platform-default experience instead.

**Your defense:**
- Negotiate placement and content promotion deals with platform OEMs where possible; invest in commercial partnerships for persistent presence in recommended rows.
- Accelerate features that reduce reliance on device-level discovery: deep-linking promos via social and owned channels, stronger marketing for new Originals timed to bundle windows, and a rapid launch of co-watching/watch-party features to create social habit.
- Quick-win product moves: implement richer home-screen preview cards, accelerate frictionless playback deeplinks from external sources, and pilot exclusive short-form companion content optimized for platform widgets.
- Longer-term: increase first-party Originals cadence, push global local-language hits that build independent destination value, and invest in measurement to prove incremental value of placement (use data to renegotiate platform terms).

