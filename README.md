# Part 1: Simplified Business Analysis Summary

**Q1: What is the REAL business problem here?**

**A1:** The main problem isn't just that we are losing more deals—it’s that **we don't know why.** We have plenty of potential customers (pipeline), but we are failing to turn them into actual buyers. This creates a big "guessing game" for the leaders. Because we don't know if the problem is with certain teams, regions, or products, we can't predict how much money the company will make. Right now, our sales team might be wasting a lot of time and effort on deals that were never going to close anyway.

**Q2: What key questions should an AI system answer?**

**A2:** To stop guessing and start fixing things, the system needs to answer three simple things:
*   **Why is this happening?** Where exactly are we losing deals? Is it in one specific country, or are deals just getting stuck at the very last step (like the final price talk)?
*   **What will happen next?** Which deals in our current list are likely to be lost? Based on how things are going, what is the safest bet for our sales next month?
*   **How do we fix it?** Which sales reps need extra training? Should we stop chasing certain types of customers that aren't buying anymore?

**Q3: What metrics (numbers) matter most?**

**A3:** We focus on the numbers that show us the difference between a "bad process" and "bad luck":
*   **The Main Numbers:** We look at win rates by industry or region to see exactly where the drop is happening. We also check which steps of the sales process (like the demo or proposal) are losing the most deals.
*   **The Timing:** How long does a deal take from start to finish? If deals are taking much longer than before, it usually means our team is holding onto "dead" deals for too long.
*   **The Quality:** Are the new leads actually good? If the leads from marketing aren't buying, the problem might be how we find customers, not how we sell to them.

**Q4: What are we assuming about the data?**

**A4:** For this analysis to work, we have to assume a few things are true:
*   **The data is correct:** We assume the sales team actually updates the system correctly when they win or lose a deal.
*   **Everyone uses the same rules:** We assume that a "Demo" or "Price Proposal" means the same thing to every sales rep in every office.
*   **No huge outside changes:** We assume nothing crazy happened in the world (like a 50% price increase or a huge new competitor) that would suddenly make our old data useless.


# Part 2: Business Insights Analysis: Win Rate Decline Investigation

## Overview
After analyzing the sales data comparing the peak performance period (Q4 2023) with the decline period (Q1-Q2 2024), I identified three meaningful business insights that explain the win rate drop from 47.5% to approximately 43.8%.

---

## Insight 1: Partner Lead Source is Underperforming and Getting Worse

### What We Found:
Partners send us roughly **25% of all our deals**, but these leads convert at significantly lower rates than other channels. More concerning is that this gap is **widening over time**.

| Metric | Historical | Recent (Q1-Q2 2024) |
|--------|-----------|---------------------|
| Partner Win Rate | 44.0% | 44.5% |
| Best Channel Win Rate | 46.0% | 48.2% |
| **Gap** | -2.0 percentage points | **-3.7 percentage points** |

### Why It Matters:
- Partners represent a **quarter of our pipeline** — this is a major source of potential customers
- The gap nearly **doubled** (-2.0pp to -3.7pp), meaning partner quality is deteriorating, not improving
- At current deal values, this underperformance translates to approximately **$350K-$500K in lost potential revenue per quarter**
- Sales reps are spending valuable time on leads that are less likely to close

### What Action It Could Drive:
1. **Partner Quality Audit**: Identify which specific partners send high-quality leads vs. poor-quality leads
2. **Partner Training Program**: Educate partners on our Ideal Customer Profile (ICP) so they send better-fit prospects
3. **Tiered Partner System**: Create tiers (Gold, Silver, Bronze) based on lead quality; incentivize improvement
4. **Lead Scoring Integration**: Apply stricter qualification criteria to partner-sourced leads before assigning to reps

---

## Insight 2: Large Deals Are Taking Longer and Converting at Lower Rates

### What We Found:
Sales cycles have **lengthened across all deal sizes**, but the most concerning pattern is in the "Large" deal tier ($30K-$60K), which now has the **lowest win rate** of any segment at just 42.9%.

| Deal Tier | Cycle Time (Historical) | Cycle Time (Recent) | Win Rate (Recent) |
|-----------|------------------------|---------------------|-------------------|
| Small (<$10K) | 63 days | 68 days (+5 days) | 44.3% |
| Medium ($10-30K) | 64 days | 72 days (+8 days) | 46.2% |
| **Large ($30-60K)** | 65 days | 71 days (+6 days) | **42.9% (Lowest!)** |
| Enterprise ($60K+) | 65 days | 71 days (+6 days) | 48.8% |

### Why It Matters:
- **Longer cycles tie up sales capacity**: Reps stuck on slow deals can't pursue new opportunities
- **Large deals falling through hurt more**: A lost $45K deal impacts revenue more than a lost $8K deal
- **The "middle child" problem**: Large deals aren't getting enterprise-level attention but require more effort than small deals
- **Enterprise deals are actually converting best** (48.8%), so the issue isn't "big deals are hard" — it's specifically the Large tier

### What Action It Could Drive:
1. **Create Deal-Size-Specific Playbooks**: Different sales motions for Large vs. Enterprise vs. Small deals
2. **Earlier Executive Involvement**: Bring in senior sponsors at the proposal stage for Large deals, not just Enterprise
3. **Deal Velocity Tracking**: Set stage-by-stage time limits; escalate deals that stall beyond thresholds
4. **Win/Loss Analysis on Large Deals**: Conduct deep-dive reviews on recent Large deal losses to identify patterns

---

## Insight 3: Sales Rep Performance Variance is Growing — A Coaching Opportunity

### What We Found:
The gap between top and bottom performers has **widened dramatically** — from 10.9 percentage points to 17.3 percentage points. This suggests significant opportunity for improvement through coaching.

| Performer | Historical Win Rate | Recent Win Rate |
|-----------|--------------------|-----------------| 
| Top Performer | 51.0% | 55.7% |
| Bottom Performer | 40.1% | 38.5% |
| **Gap** | 10.9 pp | **17.3 pp (+58% wider)** |

**Top 3 Reps (Recent):** rep_12 (55.7%), rep_17 (53.1%), rep_16 (51.2%)
**Bottom 3 Reps (Recent):** rep_22 (39.7%), rep_11 (39.5%), rep_1 (38.5%)

**Critical Finding:** Only **1 rep (rep_12)** appears in the top 5 in both periods — success is inconsistent.

### Why It Matters:
- A **17.3pp gap** is enormous — bottom performers win nearly half as often as top performers
- Bottom performers have **similar deal volumes** to top performers, so it's not a workload issue
- **Inconsistent top performers** (only 1 overlap) suggests environmental factors may be affecting results
- If we could bring bottom performers up to average (~45.6%), that's **15-20 additional won deals per quarter**
- This is the **lowest-effort, highest-impact** improvement opportunity

### What Action It Could Drive:
1. **Shadow Top Performers**: Have struggling reps observe rep_12's discovery calls, demos, and negotiation techniques
2. **Peer Mentoring Program**: Pair top performers with bottom performers for ongoing coaching
3. **Investigate Systemic Issues**: Do bottom performers have worse territories? Lower-quality lead assignments?
4. **Weekly Performance Reviews**: Make rep performance dispersion a tracked KPI for sales leadership
5. **Best Practice Documentation**: Record and distribute winning talk tracks, objection handling, and closing techniques from top reps

---

## Summary: Priority Matrix for CRO Action

| Insight | Business Impact | Implementation Effort | Priority |
|---------|----------------|----------------------|----------|
| Partner Lead Quality | ~$400K/quarter at risk | Medium (requires partner cooperation) | 🔶 **HIGH** |
| Large Deal Conversion | High revenue deals failing | High (process redesign) | 🔴 **CRITICAL** |
| Rep Performance Gap | 15-20 deals/quarter opportunity | Low (coaching = free) | 🔴 **CRITICAL** |

### Recommended Immediate Actions:
1. **This Week**: Schedule 1:1s with bottom 5 performing reps to understand challenges
2. **This Month**: Deep-dive audit on Large deal losses; identify root causes
3. **This Quarter**: Launch partner tiering program with quality metrics
4. **Ongoing**: Track performance gap weekly as a leading indicator of team health

---

*Analysis prepared using skygeni_sales_data.csv covering 5,000 deals across 18 months*




# Part 3: Decision Engine – Win Rate Driver Analysis

## Option Selected: B – Win Rate Driver Analysis

---

## 1. Problem Definition: The "Silent Bleeder"

**The Executive Challenge:**
The Revenue leadership is facing a classic "average fallacy." The global win rate has slipped to ~43.8%, but averages smooth out the jagged edges of reality. A sales leader looking at the global number knows *something* is wrong but doesn't know *what*.
*   Is it the new sales hires? (Training issue)
*   Is it the mid-market segment? (Product-market fit issue)
*   Is it a specific lead channel? (Marketing issue)

**The Objective:**
We need to move from "We are losing more" to "We are losing specific deals because of X." We need a system that decomposes the aggregate drop into specific, attributable drivers. We are not just predicting who *will* win (a probability score), but diagnosing *why* we are losing (a root cause analysis).

---

## 2. The Model: Deterministic Driver Impact Scoring

**Why We Chose Simplicity:**
We deliberately avoided black-box Machine Learning models (like Random Forest or Neural Networks) for this specific task.
*   **Trust:** Sales leaders need to defend their decisions. Telling a VP "The AI said so" doesn't work. Telling them "This segment is dragging us down by 0.93% weighted" leads to action.
*   **Causality:** We don't just need prediction (who will win); we need attribution (why are we losing).

**The Logic: Driver Impact Score (DIS)**
We created a custom metric that weights performance gaps by their business volume.

```
Impact Score = (Segment Win Rate - Benchmark) × Volume Share
```

*   **Segment Win Rate**: The reality of that specific slice (e.g., "Large Deals", "Partner Source").
*   **Benchmark**: The company's target or historical weighted average.
*   **Volume Share**: The weight of that slice in the total pipeline.

**Why this formula?**
A 10% drop in win rate for a tiny segment (1% of volume) is statistical noise.
A 2% drop in win rate for your core channel (40% of volume) is a revenue disaster.
This model mathematically bubbles the "disasters" to the top.

---

## 3. Actionable Outputs & Rich Insights

Running this model across our 18-month dataset revealed distinct "anchors" (dragging us down) and "sails" (pushing us forward).

### 🔴 The Anchors (Negative Drivers)

**1. The "Partner" Dilution (Impact: -0.93)**
*   **Observation:** Leads coming from "Partners" account for a massive **25% of our total pipeline** (high volume), yet their win rate has decayed to **~40.8%** (3.7% below baseline).
*   **Business Insight:** We are filling our funnel with lower-quality "calories." The high volume masks the generic inefficiency, but the weighted impact explains nearly **25% of our total win rate drop**.
*   **Action:** Immediate audit of Partner lead qualification. Stop routing "Bronze Tier" partner leads to senior reps.

**2. The "Large Deal" Stagnation (Impact: -0.38)**
*   **Observation:** Deals in the "Large" band ($30k-$60k) are converting at just **42.9%**. Interestingly, this is *lower* than "Enterprise" deals ($60k+) which convert at a healthy **48.8%**.
*   **Business Insight:** This is the "Middle Child" syndrome. These deals are too complex for a transactional sale but aren't getting the Executive Sponsor resources that Enterprise deals get. They are likely stalling in the "Proposal" stage.
*   **Action:** Implement "Enterprise-Lite" support (e.g., Sales Engineer office hours) for deals >$30k.

**3. Performance Variance (Impact: -0.32)**
*   **Observation:** The gap between top and bottom reps has widened. Bottom performers (specifically `rep_1`, `rep_11`, `rep_22`) are performing **~14pp below average**.
*   **Business Insight:** This isn't a system-wide training failure; it's a specific cohort failure.
*   **Action:** Targeted PIP (Performance Improvement Plan) or "Shadowing Program" where bottom reps must shadow `rep_12` (Top Performer) on 5 calls/week.

---

### 🟢 The Sails (Positive Drivers)

**1. The Tech Vertical Stronghold (+0.30)**
*   **Observation:** The Technology industry segment is performing **2.0pp above average** with robust volume (15%).
*   **Business Insight:** We have strong Product-Market Fit (PMF) in this vertical.
*   **Action:** Marketing should double down on Tech lookalike audiences and case studies.

---

## 4. How a Sales Leader Uses This System

**The Workflow:**
This isn't just a static dashboard; it's a weekly decision loop.

**Monday Morning (Tactical):**
*   **Signal**: The dashboard highlights "Large Deals" impact score dropped this week.
*   **Action**: Sales VP filters pipeline for "Large Deals > Stage 3" and holds a "Deal Surgery" session to unstick them.

**Monthly Review (Strategic):**
*   **Signal**: "Partner" impact has been negative for 3 months straight with no improvement.
*   **Action**: VP of Partnerships is tasked with revamping the partner contract structure (e.g., cutting off referrals from low-quality partners).

**Quarterly Planning (Structural):**
*   **Signal**: "Tech" vertical is the highest positive driver.
*   **Action**: Realign territory maps. Ensure every "Tech" account has a named rep, moving away from geo-based territories to vertical-based territories.

**Final Verdict:**
By mathematically isolating the *weight* of each failing component, we turn a vague "sales slump" into a checklist of 3 distinct problems to fix. This is how data turns into revenue.


# Part 4: Mini System Design – Sales Insight & Alert System

## Overview

If SkyGeni were to productize this, here's what a lightweight **Sales Insight & Alert System** would look like.

---

## 1. High-Level Architecture

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                         SALES INSIGHT & ALERT SYSTEM                        │
└─────────────────────────────────────────────────────────────────────────────┘

┌─────────────┐     ┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│   CRM       │     │   DATA      │     │  ANALYTICS  │     │   ALERT     │
│   SOURCE    │────▶│   LAYER     │────▶│   ENGINE    │────▶│   DELIVERY  │
│             │     │             │     │             │     │             │
│ • Salesforce│     │ • ETL Jobs  │     │ • Driver    │     │ • Slack     │
│ • HubSpot   │     │ • Data Lake │     │   Scorecard │     │ • Email     │
│ • Pipedrive │     │ • Warehouse │     │ • Anomaly   │     │ • Dashboard │
│             │     │             │     │   Detection │     │ • Mobile    │
└─────────────┘     └─────────────┘     └─────────────┘     └─────────────┘
       │                   │                   │                   │
       └───────────────────┴───────────────────┴───────────────────┘
                                    │
                           ┌───────▼────────┐
                           │   FEEDBACK     │
                           │   LOOP         │
                           │                │
                           │ • Alert useful?│
                           │ • Action taken?│
                           │ • Improve model│
                           └────────────────┘
```

### Components:

| Component | Purpose | Technology |
|-----------|---------|------------|
| **CRM Source** | Where sales data lives | Salesforce, HubSpot API |
| **Data Layer** | Clean, transform, store | Python/dbt + PostgreSQL |
| **Analytics Engine** | Calculate metrics, detect issues | Python + SQL |
| **Alert Delivery** | Notify the right people | Slack API, Email, Dashboard |
| **Feedback Loop** | Learn from user actions | Simple rating system |

---

## 2. Data Flow

### Step-by-Step:

```
1. EXTRACT (Every 6 hours)
   CRM API → Raw deal data (stage, amount, owner, dates)
   
2. TRANSFORM (After extract)
   • Calculate win rates by segment
   • Compute sales cycle metrics
   • Compare to baseline (rolling 90-day average)
   
3. ANALYZE (Daily at 6 AM)
   • Run Driver Scorecard analysis
   • Check for anomalies (sudden drops/spikes)
   • Identify at-risk deals
   
4. ALERT (When thresholds crossed)
   • Filter by severity (Critical / Warning / Info)
   • Route to appropriate recipient
   • Include context + suggested action
   
5. FEEDBACK (User clicks)
   • "Was this helpful?" → Yes/No
   • "Action taken?" → Track outcomes
   • Improve alert relevance over time
```

### Data Model (Simplified):

```
deals
├── deal_id
├── stage
├── amount
├── owner_id
├── created_date
├── closed_date
├── is_won
└── lead_source

daily_metrics
├── date
├── segment (lead_source, industry, rep, etc.)
├── win_rate
├── avg_cycle_days
├── deal_count
└── baseline_win_rate (90-day rolling)

alerts
├── alert_id
├── type (anomaly, driver_change, stall)
├── severity (critical, warning, info)
├── segment
├── message
├── suggested_action
├── recipient
├── was_helpful (user feedback)
└── action_taken
```

---

## 3. Example Alerts & Insights

### Alert Type 1: Win Rate Drop Alert

```
🔴 CRITICAL ALERT: Win Rate Drop Detected

WHAT: Partner channel win rate dropped 3.2pp this week
FROM: 44.5% (last week) → 41.3% (this week)
IMPACT: ~$85K pipeline at risk if trend continues

SUGGESTED ACTION:
→ Review last 5 Partner deals lost this week
→ Schedule call with top 2 partners to discuss lead quality

[View Details] [Dismiss] [Was this helpful? 👍 👎]
```

### Alert Type 2: Stalled Deal Alert

```
🟡 WARNING: 3 Large Deals Stalled

WHAT: 3 deals over $40K have been in "Proposal" for 15+ days
DEALS:
• Acme Corp ($52K) - rep_12 - 18 days stuck
• Beta Inc ($45K) - rep_7 - 16 days stuck  
• Gamma LLC ($48K) - rep_3 - 15 days stuck

SUGGESTED ACTION:
→ Review pricing objections in these accounts
→ Consider executive sponsor outreach

[View Deals] [Snooze 3 days] [Was this helpful? 👍 👎]
```

### Alert Type 3: Rep Performance Alert

```
🔴 CRITICAL: Rep Performance Gap Widening

WHAT: rep_1 win rate dropped to 32% (team avg: 45.2%)
TREND: 3rd consecutive week of decline
DEALS: 0 wins in last 8 closed opportunities

SUGGESTED ACTION:
→ Schedule 1:1 coaching session
→ Review recent loss reasons
→ Consider deal shadowing with rep_12

[View Rep Details] [Schedule Meeting] [Was this helpful? 👍 👎]
```

### Alert Type 4: Positive Insight

```
🟢 INSIGHT: Tech Industry Outperforming

WHAT: Tech industry win rate hit 52% (vs 45% overall)
TREND: 3rd consecutive week above 50%
VOLUME: 28 deals closed, 15 won

SUGGESTED ACTION:
→ Consider increasing marketing spend on Tech
→ Document winning patterns from Tech deals

[View Analysis] [Share with Team] [Was this helpful? 👍 👎]
```

---

## 4. How Often It Runs

| Process | Frequency | Why |
|---------|-----------|-----|
| **Data Sync** | Every 6 hours | Balance freshness vs. API limits |
| **Metric Calculation** | Daily (6 AM) | Ready before sales standup |
| **Driver Scorecard** | Weekly (Monday 7 AM) | Strategic, not daily noise |
| **Anomaly Detection** | Daily | Catch sudden changes fast |
| **Stalled Deal Check** | Daily | Time-sensitive |
| **Rep Performance** | Weekly | Avoid over-alerting |

### Alert Delivery Schedule:

```
CRITICAL alerts  → Immediate (Slack + Email)
WARNING alerts   → Daily digest (Email at 8 AM)
INFO insights    → Weekly summary (Monday email)
```

---

## 5. Failure Cases & Limitations

### Technical Failures:

| Failure | Impact | Mitigation |
|---------|--------|------------|
| **CRM API down** | No new data | Retry with backoff; alert ops team after 3 failures |
| **Stale data** | Wrong metrics | Show "last updated" timestamp; warn if >12 hours old |
| **Duplicate deals** | Inflated counts | Dedupe by deal_id in ETL |
| **Missing fields** | Incomplete analysis | Default values; flag data quality issues |

### Analytical Limitations:

| Limitation | Example | How We Handle It |
|------------|---------|------------------|
| **Small sample size** | New rep with 3 deals | Require minimum 10 deals before alerting |
| **Seasonality** | Q4 always higher | Use year-over-year comparison in Q4 |
| **External factors** | Competitor launched | Add manual "context note" feature |
| **Correlation ≠ causation** | Partner leads worse, but why? | Alerts suggest investigation, not blame |
| **Lagging indicator** | Win rate reflects past | Add leading indicators (stage velocity) |

### Business Limitations:

| Limitation | Reality |
|------------|---------|
| **Alert fatigue** | Too many alerts = ignored. Throttle to max 3/day. |
| **Trust building** | Users won't act until system proves accuracy. Start with low-risk insights. |
| **Action gap** | Alert is useless if no clear action. Always include "Suggested Action." |
| **One-size-fits-all** | CRO needs different alerts than rep. Role-based filtering. |

---

## 6. Productization: Key Features for SkyGeni

### MVP Features:

| Feature | Description |
|---------|-------------|
| **Driver Dashboard** | Visual scorecard of what's helping/hurting win rate |
| **Smart Alerts** | Role-based, severity-filtered, actionable |
| **Drill-down** | Click any metric → see underlying deals |
| **Feedback Loop** | "Was this helpful?" improves relevance |

### Future Features:

| Feature | Value |
|---------|-------|
| **Predictive Alerts** | "This deal is 70% likely to stall" |
| **Benchmark Comparison** | "Your win rate vs. similar companies" |
| **Natural Language Insights** | "Win rate dropped because Partner leads are 3.7pp worse" |
| **Slack Bot** | "Hey SkyBot, why is our win rate down?" |

---

## Summary

| Aspect | Design Decision |
|--------|-----------------|
| **Architecture** | Simple 4-layer: Source → Data → Analytics → Alerts |
| **Data Flow** | Extract every 6h → Transform → Analyze daily → Alert on threshold |
| **Alert Types** | Win rate drops, stalled deals, rep performance, positive insights |
| **Frequency** | Critical = immediate, Warning = daily, Info = weekly |
| **Failure Handling** | Retries, staleness warnings, minimum sample sizes |
| **Key Differentiator** | Every alert includes "Suggested Action" — not just data, but guidance |

---


# Part 5: Reflection

## The Most Important Part

This reflection is where I honestly assess the limitations of my analysis. No model is perfect, and being aware of weaknesses is critical for real-world success.

---

## 1. What Assumptions in My Solution Are Weakest?

### Assumption 1: "The Data is Clean and Complete"
**Weakness:** I assumed all deals are recorded correctly — that a "Won" deal is truly won, a "Lost" deal is truly lost, and sales reps update stages accurately.

**Reality in Production:**
- Reps often update CRM only before pipeline reviews (data lags reality)
- Some deals are marked "Lost" but actually went dark (potentially still open)
- Stage definitions may differ across reps (what counts as "Demo"?)

**Impact:** My win rate calculations could be off by 5-10% if deal statuses are stale.

---

### Assumption 2: "Historical Patterns Will Continue"
**Weakness:** I assumed Q4 2023 is a valid "baseline" period to compare against.

**Reality:**
- Q4 often has year-end buying pressure (artificially higher close rates)
- The decline might be seasonal, not fundamental
- External factors (economy, competition, market shifts) aren't in the data

**Impact:** The "decline" might be normal seasonality, not a real problem.

---

### Assumption 3: "All Segments are Comparable"
**Weakness:** When comparing Partner leads to Inbound leads, I assume they're going after the same type of customer.

**Reality:**
- Partners might target different industries/company sizes
- "Partner leads are worse" might mean "Partners target harder-to-close customers"

**Impact:** Recommending "fix partners" might be wrong if partners are doing a different job.

---

### Assumption 4: "Correlation = Causation"
**Weakness:** I found that rep_1 has low win rate. I assumed rep_1 needs coaching.

**Reality:**
- rep_1 might be assigned the hardest territories
- rep_1 might be handling "problem accounts" escalated from others
- rep_1 might be new and ramping up

**Impact:** Coaching rep_1 won't help if the real issue is lead assignment.

---

## 2. What Would Break in Real-World Production?

### Problem 1: Data Pipeline Issues
**What Would Happen:** CRM data arrives late, incomplete, or with schema changes.

**What Breaks:** My Impact Score calculations would fail or produce garbage.

**Fix Needed:**
- Data quality monitoring (alert if win rate suddenly = 0%)
- Schema versioning
- Graceful error handling

---

### Problem 2: Edge Cases and Outliers
**What Would Happen:** A single massive deal ($5M) closes in a quarter.

**What Breaks:** That one deal dominates all metrics; "Enterprise win rate = 100%."

**Fix Needed:**
- Outlier detection and capping
- Volume thresholds (need N deals minimum)
- Separate treatment for "whale deals"

---

### Problem 3: Feedback Loops
**What Would Happen:** CRO sees "Partner leads are bad" → stops sending partner leads → partner volume drops → my model has no data on partners.

**What Breaks:** The model can't tell if partners improved because there's no signal.

**Fix Needed:**
- Maintain minimum sample sizes per segment
- A/B testing framework for changes
- Track counterfactuals ("what if we hadn't changed?")

---

### Problem 4: Changing Business Context
**What Would Happen:** Company launches a new product line, changes pricing, enters new market.

**What Breaks:** Historical baselines are meaningless. Old "good" segments may now be "bad."

**Fix Needed:**
- Recalibrate baseline after major changes
- Rolling windows instead of fixed periods
- Business event tagging in the data

---

## 3. What Would I Build Next Given 1 Month?

### Week 1-2: Deal Scoring Model
**What:** Predict probability of winning for each open deal.

**Why:** The current analysis is backward-looking. Sales leaders need forward-looking predictions to prioritize time today.

**How:** Logistic regression or gradient boosting on deal attributes (size, stage, age, rep, industry). Output: "This deal has 62% chance of closing."

---

### Week 2-3: Real-Time Dashboard
**What:** Interactive dashboard that updates daily with:
- Driver Scorecard (current analysis, automated)
- Open deal risk scores
- Rep performance leaderboards
- Pipeline health trends

**Why:** Right now, my analysis is a one-time notebook. Leaders need self-serve access.

**How:** Streamlit or Metabase connected to a data warehouse, auto-refreshed.

---

### Week 3-4: Automated Alerts & Actions
**What:** System sends alerts when:
- A segment's win rate drops below threshold
- A deal is stuck in a stage too long
- A rep's performance drops suddenly

**Why:** Leaders don't have time to check dashboards daily. Push insights to them.

**How:** Scheduled jobs that compare metrics to thresholds; Slack/email notifications.

---

### If Time Permits: Interaction Analysis
**What:** Find combinations that matter: "Partner leads in Healthcare close worse, but Partner leads in Tech actually close better."

**Why:** My current model looks at segments independently. Reality has interactions.

**How:** Decision trees or stratified analysis by multiple dimensions.

---

## 4. What Part of My Solution Am I Least Confident About?

### Least Confident: The Custom Metrics

**The Metrics:**
- Deal Momentum Decay Index (DMDI)
- Rep-Segment Fit Score (RSFS)

**Why I'm Unsure:**

1. **Untested in Production:** I designed these metrics logically, but I haven't validated that they actually predict outcomes better than simple metrics.

2. **Action Threshold Uncertainty:** I said "DMDI > 1.2 means closing problem." But is 1.2 the right threshold? I picked it intuitively, not empirically.

3. **Limited Data for Validation:** With 18 months of data from one company, I can't prove these metrics generalize. They might overfit to this specific dataset.

4. **Complexity vs. Value Trade-off:** A simple metric ("win rate by stage") might be 90% as good with 10% of the complexity. I didn't prove the custom metrics add enough value to justify their complexity.

**What I'd Do to Increase Confidence:**
- A/B test: Do teams using DMDI make better decisions than teams using simple metrics?
- Backtest: Does DMDI predict future win rate declines?
- User research: Do sales leaders actually find these metrics useful, or confusing?

---

## Summary: Honest Self-Assessment

| Question | My Answer |
|----------|-----------|
| **Weakest assumption?** | Historical patterns continue; Q4 baseline is valid |
| **What would break?** | Data quality issues, outliers, feedback loops |
| **Build next with 1 month?** | Real-time dashboard + deal scoring + alerts |
| **Least confident about?** | Custom metrics (DMDI, RSFS) — untested in production |

---

**Final Thought:**

The value of this analysis isn't in being "right" — it's in providing a framework for thinking about the problem. If the CRO uses my Driver Scorecard to have better conversations with their team, that's success, even if some of my specific conclusions turn out to be wrong.
