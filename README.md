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


# Part 2 – Data Exploration & Insights

📋 Business Insights Summary (Recruiter-Ready)
Insight 1: Partner Lead Source is Underperforming and Getting Worse
What We Found: Partners send 25% of deals but convert at lower rates. The gap widened from -2.0pp to -3.7pp.

Why It Matters:

Quarter of pipeline is underperforming
~$350K-$500K in lost potential revenue per quarter
Sales reps wasting time on low-quality leads
Actions It Could Drive:

Partner quality audit → Identify which partners send good leads
Partner training on ICP
Tiered partner system with incentives
Insight 2: Large Deals Are Taking Longer and Converting at Lower Rates
What We Found: Large deals ($30-60K) have the LOWEST win rate at 42.9%, despite Enterprise deals converting at 48.8%.

Why It Matters:

Longer cycles tie up sales capacity
Lost $45K deals hurt more than lost $8K deals
"Middle child" problem — not getting enough attention
Actions It Could Drive:

Deal-size-specific sales playbooks
Earlier executive involvement for Large deals
Win/loss analysis on recent Large deal failures
Insight 3: Sales Rep Performance Variance is Growing
What We Found: Gap between top and bottom performers WIDENED by 58% (from 10.9pp to 17.3pp).

Why It Matters:

Bottom performers win nearly half as often as top performers
Improving bottom performers = 15-20 additional deals/quarter
Lowest-effort, highest-impact opportunity
Actions It Could Drive:

Shadow top performers (especially rep_12)
Peer mentoring program
Investigate if bottom performers have systemic disadvantages



# Part 3: Decision Engine – Win Rate Driver Analysis

## Option Selected: B – Win Rate Driver Analysis

---

## 1. Problem Definition

**What are we solving?**
The CRO asks: "Why did our win rate drop? What's hurting us, and what should we focus on to improve?"

**The Problem:**
Win rate dropped from 47.5% (Q4 2023) to ~43.8% (Q1-Q2 2024). We need to identify which specific factors are **dragging down** or **boosting** our win rate so sales leaders can take targeted action.

**Simple Explanation:**
Think of it like diagnosing why a sports team's winning percentage dropped. Is it the offense? Defense? Certain opponents? Certain players? We're building a system that answers: "What's helping us win, and what's causing us to lose?"

---

## 2. The Model: Driver Scorecard System

I built a **rule-based scoring system** (not a black-box ML model) for transparency and business usability.

### How It Works:

**Step 1: Identify Key Dimensions**
Analyze win rate by different "cuts" of the data:
- Lead Source (Inbound, Outbound, Partner, Referral)
- Industry (Tech, Finance, Healthcare, etc.)
- Deal Size Tier (Small, Medium, Large, Enterprise)
- Sales Rep
- Product Type

**Step 2: Calculate Impact Score**
For each factor, we calculate:

```
Impact Score = (Win Rate Change) × (Volume Share)
```

**What this means in plain English:**
- **Win Rate Change** = How much worse/better is this segment doing compared to baseline?
- **Volume Share** = How much of our pipeline does this segment represent?
- **Impact Score** = A segment that dropped a lot BUT is small volume has LOW impact. A segment that dropped a little BUT is huge volume has HIGH impact.

**Example:**
| Segment | Win Rate Drop | Volume Share | Impact Score |
|---------|--------------|--------------|--------------|
| Partner Leads | -3.7pp | 25% | **-0.93** (High negative impact) |
| Small Deals | -1.0pp | 38% | -0.38 (Medium impact) |
| Tech Industry | +2.0pp | 15% | +0.30 (Positive impact) |

**Step 3: Rank Drivers**
Sort all segments by Impact Score to show:
- 🔴 **Top Negative Drivers** (hurting win rate the most)
- 🟢 **Top Positive Drivers** (helping win rate)

---

## 3. Actionable Outputs

### Output 1: Driver Scorecard Dashboard

| Rank | Factor | Segment | Win Rate Δ | Volume | Impact | Action |
|------|--------|---------|------------|--------|--------|--------|
| 1 | Lead Source | Partner | -3.7pp | 25% | -0.93 | 🔴 Audit partners |
| 2 | Deal Size | Large | -2.5pp | 15% | -0.38 | 🔴 Review pricing |
| 3 | Rep | rep_1 | -8.0pp | 4% | -0.32 | 🔴 Coaching needed |
| 4 | Industry | Healthcare | -4.0pp | 8% | -0.32 | 🔶 Check ICP fit |
| 5 | Industry | Tech | +2.0pp | 15% | +0.30 | 🟢 Double down |

### Output 2: Root Cause Summary

```
TOP 3 FACTORS HURTING WIN RATE:
1. Partner leads converting 3.7pp worse (25% of pipeline)
2. Large deals ($30-60K) converting 2.5pp worse (15% of pipeline)
3. Bottom 3 reps: rep_1, rep_11, rep_22 (14pp below average)

TOP 2 FACTORS HELPING WIN RATE:
1. Tech industry converting 2.0pp better
2. Enterprise deals converting 3.0pp better
```

### Output 3: Recommended Actions (Auto-Generated)

Based on Impact Scores, the system recommends:

| Priority | Action | Expected Impact | Owner |
|----------|--------|-----------------|-------|
| 🔴 P1 | Coach bottom 3 reps | +15-20 deals/quarter | Sales Manager |
| 🔴 P1 | Audit partner lead quality | +$350K/quarter | Partnerships |
| 🔴 P2 | Create Large deal playbook | Reduce lost revenue | Sales Ops |
| 🟢 P3 | Increase Tech industry targeting | Protect current wins | Marketing |

---

## 4. How a Sales Leader Would Use This

### Weekly Usage:
1. **Open the Dashboard** → See top 5 negative and positive drivers
2. **Click on a driver** → Drill down to see specific deals/reps affected
3. **Track week-over-week** → Is Partner gap getting better or worse?

### Monthly Usage:
1. **Review Driver Trends** → Which factors improved? Which worsened?
2. **Prioritize Initiatives** → Focus coaching on highest-impact areas
3. **Set Targets** → "This month, let's close the Partner gap by 1pp"

### Quarterly Usage:
1. **Strategic Planning** → Should we reduce reliance on Partners?
2. **Resource Allocation** → Where should we add headcount?
3. **ICP Refinement** → Should we stop targeting certain industries?

---

## 5. Why This Approach Works

### Simple, Not Complex:
- **No black-box ML** → Sales leaders can understand and trust it
- **Rule-based scoring** → Anyone can verify the math
- **Transparent formula** → `Impact = (Change) × (Volume)`

### Actionable, Not Academic:
- Each output ties to a **specific action** a leader can take
- **Ranked by impact** → Focus on what moves the needle most
- **Auto-generated recommendations** → No analysis paralysis

### Business-Focused, Not Accuracy-Obsessed:
- We're not predicting exact win rate → We're finding **which levers to pull**
- Directional accuracy matters → "Partner leads are hurting us" is actionable
- Easy to update → Recalculate weekly as new data comes in

---

## Summary

| Element | Our Approach |
|---------|--------------|
| **Problem** | What factors are hurting/helping our win rate? |
| **Model** | Rule-based Impact Score = (Win Rate Change) × (Volume Share) |
| **Output** | Ranked Driver Scorecard with auto-recommendations |
| **Usage** | Weekly review → Monthly priorities → Quarterly strategy |
| **Value** | Tells CRO exactly what to fix for maximum impact |

---

*The goal isn't to build the most sophisticated model — it's to give sales leaders a clear, trustworthy answer to "What should I focus on to improve win rate?"*
