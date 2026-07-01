---
type: concept
title: Amazon PPC Standard Operating Procedures
domain: Amazon PPC / VA Training
created: 2026-06-29
related: [[ppc-workflows]], [ppc-templates]], [amazon-ppc-fundamentals]]
---

# Amazon PPC Standard Operating Procedures

> Ready-to-implement SOPs for Amazon PPC management. Each SOP includes: objective, inputs, steps, decision rules, outputs, and escalation criteria.

---

## SOP-01: Daily PPC Health Check

**Objective:** Ensure all campaigns are running correctly and catch anomalies early.
**Time:** 15 minutes per account
**Frequency:** Daily (every workday)
**Owner:** PPC Specialist / VA

### Inputs
- Amazon Advertising Console access
- Campaign performance dashboard

### Steps
1. **Budget Check (3 min)**
   - Review daily spend for each campaign
   - Flag: any campaign that hit budget before end of day
   - Flag: any campaign with 0 spend (potential suppression)
   - Action: increase budget if profitable, investigate if 0 spend

2. **Anomaly Scan (5 min)**
   - Check for: sudden ACoS spikes (>20% increase from 7-day average)
   - Check for: sudden CTR drops (>30% decrease)
   - Check for: impression drops (>50% decrease)
   - Check for: CPC spikes (>25% increase)
   - Action: investigate root cause before making changes

3. **Out-of-Stock Check (3 min)**
   - Verify all advertised products are in stock
   - Flag: any product with <7 days inventory
   - Action: pause ads for OOS products, alert client

4. **Budget Pacing (4 min)**
   - Calculate: is spend tracking toward daily budget?
   - If spending too fast: review bid adjustments
   - If spending too slow: check keyword bids, auction competitiveness

### Decision Rules
| Condition | Action |
|-----------|--------|
| Campaign hit budget before 6 PM | Increase budget by 20% if ACoS is profitable |
| Campaign has $0 spend for 24+ hours | Check: paused? OOS? Bid too low? |
| ACoS increased >20% from 7-day avg | Investigate: new keywords? competitor? CPC spike? |
| Product OOS | Pause campaign immediately, notify client |
| CTR dropped >30% | Check: listing changed? Main image? Price? |

### Outputs
- Daily health check log (spreadsheet or Notion)
- Anomaly alerts sent to client (if critical)
- Budget adjustments documented

### Escalation
- If ACoS exceeds 2x break-even: escalate to senior specialist
- If product suppressed: notify client immediately
- If account access issues: escalate to client within 1 hour

---

## SOP-02: Weekly Search Term Report Analysis

**Objective:** Identify harvesting opportunities and negative keyword candidates.
**Time:** 30-45 minutes per account
**Frequency:** Weekly (Monday recommended)
**Owner:** PPC Specialist / VA

### Inputs
- Search Term Report (last 7 days)
- Campaign performance data
- Negative keyword list (current)

### Steps
1. **Download & Sort (5 min)**
   - Download Search Term Report from Amazon Advertising Console
   - Sort by: Spend (descending)
   - Filter: minimum 5 clicks (for statistical relevance)

2. **Identify Harvesting Candidates (15 min)**
   - Look for: search terms with 2+ orders AND ACoS < target
   - These are winning terms — add as exact match in manual campaigns
   - Check: is this term already targeted? If yes, skip
   - Action: add to manual campaign with appropriate bid

3. **Identify Negative Candidates (15 min)**
   - Look for: search terms with 15+ clicks AND 0 orders
   - Look for: search terms with ACoS > 2x break-even
   - Check: is this term relevant to the product? Sometimes high ACoS = listing issue, not keyword issue
   - Action: add as negative exact (or negative phrase if completely irrelevant)

4. **Identify Bid Adjustment Candidates (5 min)**
   - Look for: terms with high impressions but low CTR (<0.2%)
   - Look for: terms with high CVR but low impressions (bid too low)
   - Action: adjust bids accordingly

5. **Document & Update (5 min)**
   - Log all changes made
   - Update negative keyword list
   - Note any trends or patterns for client report

### Decision Rules
| Condition | Action |
|-----------|--------|
| 2+ orders, ACoS < target | Harvest to manual exact match |
| 15+ clicks, 0 orders | Add as negative exact |
| ACoS > 2x break-even | Add as negative exact (unless high CVR) |
| CTR < 0.2%, impressions > 1000 | Check listing relevance, consider negating |
| High CVR, low impressions | Increase bid by 20-30% |

### Outputs
- Updated campaign structure (new keywords added)
- Updated negative keyword list
- Weekly analysis log
- Client report section

---

## SOP-03: Bid Optimization

**Objective:** Adjust bids to hit target ACoS while maximizing volume.
**Time:** 20-30 minutes per account
**Frequency:** 2-3x per week
**Owner:** PPC Specialist / VA

### Inputs
- Campaign performance data (7-day rolling)
- Target ACoS per campaign
- Current bid levels

### Steps
1. **Pull Data (3 min)**
   - Export keyword-level performance (last 7 days)
   - Calculate: 7-day ACoS per keyword
   - Compare to target ACoS

2. **Apply Bid Rules (15 min)**
   - See decision rules below
   - Make changes in bulk operations or manually
   - Maximum bid change: 20% per adjustment (avoid volatility)

3. **Review Placement Adjustments (5 min)**
   - Check: Top of Search performance
   - If Top of Search CVR > 2x average: increase placement bid
   - If Rest of Search performing better: decrease placement bid

4. **Document Changes (5 min)**
   - Log all bid changes with reasoning
   - Note any patterns (CPC inflation, competition changes)

### Decision Rules
| 7-Day ACoS | Action | Bid Change |
|------------|--------|------------|
| < 50% of target | Increase bid (room for more volume) | +15% |
| 50-80% of target | Maintain or slight increase | +5-10% |
| 80-120% of target | Maintain (at target) | 0% |
| 120-150% of target | Decrease bid | -10-15% |
| 150-200% of target | Decrease bid significantly | -20-25% |
| > 200% of target | Evaluate: negate or major reduction | -30% or negate |

### Special Rules
- **New keywords (<14 days data):** Don't adjust — let data accumulate
- **Seasonal keywords:** Adjust based on historical seasonal patterns
- **Brand keywords:** Maintain competitive bids (protect brand)
- **Competitor keywords:** Aggressive bids if CVR is strong

---

## SOP-04: Campaign Launch (New Product)

**Objective:** Set up PPC campaigns for a new product from scratch.
**Time:** 2-3 hours per product
**Frequency:** As needed
**Owner:** PPC Specialist / VA

### Pre-Launch Checklist
- [ ] Product listing optimized (title, bullets, images, A+ Content)
- [ ] Product in stock (FBA or FBM with Prime)
- [ ] Competitive pricing set
- [ ] Review strategy in place (Vine, early reviews)
- [ ] Brand Registry confirmed (if running SB/SD)

### Steps
1. **Keyword Research (30 min)**
   - Use Helium 10 Cerebro/Magnet or manual research
   - Identify: 50-100 relevant keywords
   - Categorize: exact match (top 10), phrase match (20-30), broad match (remaining)
   - Check search volume and competition

2. **Campaign Structure Setup (30 min)**
   - Create portfolio: [Product Name] PPC
   - Campaign 1: Auto (discovery) — $10-15/day
   - Campaign 2: Manual Exact (proven terms) — $15-20/day
   - Campaign 3: Manual Phrase (expansion) — $10-15/day
   - Total daily budget: $35-50/day

3. **Keyword Loading (20 min)**
   - Auto campaign: let Amazon use listing data
   - Manual Exact: add top 10 keywords with calculated bids
   - Manual Phrase: add 20-30 keywords with slightly lower bids
   - Set match types correctly

4. **Bid Setting (15 min)**
   - Calculate initial bid: Target ACoS × Product Price × Estimated CVR
   - Start conservative (lower than calculated)
   - Add placement adjustments: +25% Top of Search for exact match

5. **Negative Keywords (15 min)**
   - Add common negatives: "free," "cheap," "DIY," "repair"
   - Add category-specific negatives
   - Set up shared negative keyword list

6. **Naming Convention (5 min)**
   - Format: [Product]_[Type]_[MatchType]_[Date]
   - Example: KitchenWidget_Auto_Auto_20260629

7. **Documentation (15 min)**
   - Screenshot initial setup
   - Document keyword list and bids
   - Set review date: 14 days from launch

### Post-Launch Timeline
| Day | Action |
|-----|--------|
| Day 1-3 | Monitor only — no changes |
| Day 4-7 | First search term review — identify early patterns |
| Day 7-14 | First bid adjustments based on data |
| Day 14 | Full review: harvest, negate, restructure if needed |
| Day 30 | Comprehensive performance review, client report |

---

## SOP-05: Campaign Restructuring

**Objective:** Reorganize a poorly performing or unstructured account.
**Time:** 4-8 hours (depending on account size)
**Frequency:** As needed
**Owner:** Senior PPC Specialist

### When to Restructure
- ACoS consistently >2x break-even despite optimization
- More than 20 campaigns with < $5/day budget each
- No clear campaign hierarchy or naming convention
- Auto and manual campaigns mixed without strategy
- Zero negative keywords

### Steps
1. **Audit & Document (1-2 hours)**
   - Screenshot everything before changes
   - Catalog all campaigns, ad groups, keywords
   - Identify: dead campaigns, winners, losers
   - Calculate: current ACoS, CVR, CTR per campaign
   - Document: current budget allocation

2. **Design New Structure (1 hour)**
   - Define portfolio hierarchy
   - Set campaign naming convention
   - Plan: which campaigns to keep, merge, archive
   - Plan: new campaigns to create

3. **Create New Campaigns (1-2 hours)**
   - Build new campaign structure
   - Migrate winning keywords from old campaigns
   - Set appropriate bids and budgets
   - Add negative keywords

4. **Archive Old Campaigns (30 min)**
   - Archive (don't delete) old campaigns
   - Preserve historical data
   - Document what was archived and why

5. **Monitor Transition (2-4 weeks)**
   - Daily health checks
   - Weekly performance comparison (old vs. new)
   - Adjust as needed — don't make more changes for 14 days

---

## SOP-06: Monthly Performance Report

**Objective:** Provide clients with clear, actionable performance insights.
**Time:** 1-2 hours per account
**Frequency:** Monthly (1st of each month)
**Owner:** PPC Specialist / VA

### Report Structure
1. **Executive Summary (3 bullets max)**
   - Overall performance: up/down/flat
   - Key win from last month
   - Key focus for next month

2. **Metrics Dashboard**
   | Metric | Last Month | This Month | Target | Trend |
   |--------|-----------|------------|--------|-------|
   | Total Ad Spend | | | | |
   | Total Ad Revenue | | | | |
   | ACoS | | | | |
   | ROAS | | | | |
   | TACoS | | | | |
   | Clicks | | | | |
   | Impressions | | | | |
   | CTR | | | | |
   | CVR | | | | |
   | CPC | | | | |

3. **What Worked**
   - Top 3 performing campaigns
   - Top 5 performing keywords
   - Key optimizations made and their impact

4. **What Didn't Work**
   - Underperforming campaigns (and why)
   - Keywords negated and total savings
   - Lessons learned

5. **Recommendations**
   - Specific actions for next month
   - Budget adjustments proposed
   - New opportunities identified

6. **Competitive Landscape**
   - Any new competitors observed
   - CPC trends in category
   - Market share changes

### Delivery
- Send via email by 5th of each month
- Include spreadsheet with full data
- Schedule 30-min call to discuss (optional)

---

## SOP-07: Client Onboarding

**Objective:** Set up new PPC client for success.
**Time:** 3-5 hours total
**Frequency:** Per new client
**Owner:** PPC Specialist / VA

### Steps
1. **Discovery Call (1 hour)**
   - Goals: revenue target, ACoS target, timeline
   - Budget: monthly PPC budget, flexibility
   - Products: which products to advertise, priority
   - Competition: who are the main competitors
   - Past performance: any historical PPC data

2. **Account Access (30 min)**
   - Request Seller Central access (user permissions)
   - Request Advertising Console access
   - Verify: Brand Registry status
   - Verify: product catalog and inventory

3. **Audit (1-2 hours)**
   - Full account audit (if existing campaigns)
   - OR: product/keyword research (if new to PPC)
   - Document findings in audit template

4. **Strategy Proposal (1 hour)**
   - Write strategy document
   - Include: campaign structure, budget allocation, timeline, KPIs
   - Present to client for approval

5. **Implementation (1-2 hours)**
   - Build campaigns per approved strategy
   - Set up reporting templates
   - Set up communication cadence

6. **Kickoff (30 min)**
   - Walk client through what was set up
   - Confirm reporting schedule
   - Set expectations: first 2 weeks = data collection, not optimization

---

## SOP-08: Escalation Procedures

**Objective:** Define when and how to escalate issues to client or senior specialist.

### Escalation Levels

| Level | Condition | Action | Timeline |
|-------|-----------|--------|----------|
| **L1 — Monitor** | Minor ACoS fluctuation (<20%) | Log and monitor | No escalation |
| **L2 — Alert** | Significant ACoS spike (>20%), CTR drop, CPC increase | Investigate, prepare report, alert client next business day | Within 24 hours |
| **L3 — Urgent** | Product suppressed, account warning, budget depletion | Notify client immediately via phone/Slack | Within 2 hours |
| **L4 — Critical** | Account suspension, policy violation, billing issue | Contact client immediately, escalate to Amazon support | Immediately |

### Escalation Message Template
```
Subject: [L2/Urgent/L3] PPC Alert — [Account Name]

Issue: [Brief description]
Impact: [What's affected — campaigns, metrics, revenue]
Timeline: [When it started, how long ongoing]
Investigation: [What I've checked so far]
Recommendation: [What I suggest doing]
Action needed: [Client decision required? Or I'll proceed?]
```

---

## Using SOPs in Coaching

### For VA Training
1. Walk through each SOP line-by-line
2. Have student practice on a test account
3. Time them — set efficiency targets
4. Review their execution against SOP steps
5. Gradually reduce oversight as competency grows

### For Assessment
- Give student an unstructured account
- Ask them to follow SOP-05 (Restructuring)
- Grade on: completeness, documentation, decision-making

### For Client Work
- SOPs become the "how" behind every client deliverable
- Clients see consistency and professionalism
- VAs can work independently with SOPs as reference

---
*Sources: Trellis SOP-to-workflow guide, My Amazon Guy SOP tracking, Jarvio blog, Amazon Ads documentation*
*Last updated: 2026-06-29*
