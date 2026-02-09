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
