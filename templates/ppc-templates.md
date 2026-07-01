---
type: concept
title: Amazon PPC Templates
domain: Amazon PPC / VA Training
created: 2026-06-29
related: [[ppc-sops]], [ppc-workflows]], [ppc-templates]]
---

# Amazon PPC Templates

> Ready-to-use templates for campaign management, reporting, and client communication. Copy and customize.

---

## Template 1: Campaign Build Spreadsheet

### Columns
```
| Campaign Name | Product | Ad Type | Targeting | Keyword | Match Type | Max Bid | Daily Budget | Placement Adj (Top of Search) | Placement Adj (Product Pages) | Start Date | Status |
|---------------|---------|---------|-----------|---------|------------|---------|--------------|-------------------------------|-------------------------------|------------|--------|
| Widget_Auto_Auto | Widget X | SP | Auto | (auto) | Auto | $0.75 | $15 | +25% | +0% | 2026-07-01 | Active |
| Widget_Exact_Top5 | Widget X | SP | Keyword | bluetooth widget | Exact | $1.25 | $20 | +50% | +0% | 2026-07-01 | Active |
| Widget_Phrase_Exp | Widget X | SP | Keyword | wireless widget | Phrase | $0.90 | $15 | +25% | +0% | 2026-07-01 | Active |
| Widget_Prod_Comp1 | Widget X | SP | Product | ASIN B0XXXXX | Product | $0.85 | $10 | +0% | +25% | 2026-07-01 | Active |
| Brand_Widget_SB | Widget X | SB | Keyword | widget brand | Phrase | $1.00 | $15 | +50% | +0% | 2026-07-01 | Active |
```

### Naming Convention
```
[Product]_[Targeting]_[MatchType]_[Qualifier]

Examples:
Widget_Exact_Top5      → Exact match, top 5 keywords
Widget_Phrase_Exp      → Phrase match, expansion
Widget_Auto_Auto       → Auto campaign
Widget_Prod_Comp1      → Product targeting, competitor 1
Brand_Widget_SB        → Sponsored Brands, brand defense
```

### Budget Allocation Rule (70/20/10)
| Campaign Type | Budget % | Rationale |
|---------------|----------|-----------|
| Manual Exact (proven) | 40% | Highest conversion, most efficient |
| Manual Phrase (expansion) | 25% | Discovery, growing keywords |
| Auto (harvesting) | 20% | Continuous discovery |
| Product Targeting | 15% | Competitor conquesting |

---

## Template 2: Search Term Report Analysis

### Analysis Spreadsheet
```
| Search Term | Campaign | Match Type | Impressions | Clicks | CTR | Orders | CVR | ACoS | Spend | Revenue | Action |
|-------------|----------|------------|-------------|--------|-----|--------|-----|------|-------|---------|--------|
| bluetooth widget | Widget_Exact | Exact | 5,000 | 150 | 3.0% | 12 | 8.0% | 22% | $180 | $818 | MAINTAIN |
| wireless audio widget | Widget_Auto | Auto | 3,200 | 85 | 2.7% | 8 | 9.4% | 18% | $102 | $567 | HARVEST → Exact |
| cheap widget | Widget_Phrase | Phrase | 1,800 | 45 | 2.5% | 0 | 0% | ∞ | $54 | $0 | NEGATE |
| widget repair kit | Widget_Auto | Auto | 2,100 | 62 | 3.0% | 1 | 1.6% | 85% | $62 | $73 | BID REDUCE -15% |
```

### Action Rules
| Condition | Action | Priority |
|-----------|--------|----------|
| 2+ orders, ACoS < target | Harvest to manual exact | HIGH |
| 15+ clicks, 0 orders | Negate exact | HIGH |
| ACoS > 2x break-even | Negate or reduce bid | HIGH |
| CVR > 10%, low impressions | Increase bid +20% | MEDIUM |
| CTR < 0.2%, high impressions | Check relevance, consider negate | MEDIUM |

---

## Template 3: Monthly Performance Report

### Executive Summary
```
ACCOUNT: [Client Name]
PERIOD: [Month Year]
PREPARED BY: [Your Name]

EXECUTIVE SUMMARY
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
• Overall: [Revenue increased/decreased] [X]% month-over-month
• Key Win: [Specific achievement — e.g., "Reduced ACoS from 35% to 25% on top product"]
• Focus Next Month: [Specific goal — e.g., "Expand to Sponsored Display for retargeting"]

KEY METRICS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
| Metric | Last Month | This Month | Change | Target | Status |
|--------|-----------|------------|--------|--------|--------|
| Total Ad Spend | $X,XXX | $X,XXX | +X% | $X,XXX | ✅/⚠️/❌ |
| Total Ad Revenue | $X,XXX | $X,XXX | +X% | $X,XXX | ✅/⚠️/❌ |
| ACoS | XX% | XX% | -X% | XX% | ✅/⚠️/❌ |
| ROAS | X.Xx | X.Xx | +X% | X.Xx | ✅/⚠️/❌ |
| TACoS | XX% | XX% | -X% | XX% | ✅/⚠️/❌ |
| Total Sales (all) | $X,XXX | $X,XXX | +X% | — | ✅/⚠️/❌ |
| Clicks | X,XXX | X,XXX | +X% | — | ✅/⚠️/❌ |
| Impressions | XX,XXX | XX,XXX | +X% | — | ✅/⚠️/❌ |
| CTR | X.XX% | X.XX% | +X% | — | ✅/⚠️/❌ |
| CVR | X.XX% | X.XX% | +X% | — | ✅/⚠️/❌ |
| CPC | $X.XX | $X.XX | -X% | — | ✅/⚠️/❌ |

WHAT WORKED
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. [Campaign/keyword that performed well] — [specific metric improvement]
2. [Optimization made and its impact]
3. [New opportunity discovered]

WHAT DIDN'T WORK
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. [Underperforming area] — [what was tried, what happened]
2. [Keywords negated] — [total savings: $X]
3. [Lesson learned]

RECOMMENDATIONS FOR NEXT MONTH
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. [Specific action] — [expected impact]
2. [Budget adjustment] — [rationale]
3. [New strategy] — [test plan]

COMPETITIVE LANDSCAPE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
• New competitors: [observations]
• CPC trends: [increasing/decreasing/stable]
• Market share: [estimate]
```

---

## Template 4: Client Communication Templates

### Weekly Update (Email/Slack)
```
Subject: PPC Weekly Update — [Client Name] — [Date Range]

Hi [Client Name],

Quick weekly update:

📊 PERFORMANCE
• Spend: $[X] ([X]% of budget)
• Revenue: $[X]
• ACoS: [X]% (target: [X]%)
• Status: ✅ On track / ⚠️ Needs attention

✅ DONE THIS WEEK
• [Action 1 — e.g., "Harvested 8 new keywords from search term report"]
• [Action 2 — e.g., "Reduced bids on 12 keywords to improve ACoS"]
• [Action 3 — e.g., "Added 15 negative keywords ($[X] savings)"]

📋 NEXT WEEK
• [Planned action 1]
• [Planned action 2]

Let me know if you have any questions!

[Your Name]
```

### Monthly Review (Email)
```
Subject: Monthly PPC Report — [Client Name] — [Month Year]

Hi [Client Name],

Attached is your monthly PPC performance report.

KEY HIGHLIGHTS:
• [Top achievement]
• [Biggest improvement]
• [Opportunity identified]

MONTH AT A GLANCE:
• Revenue: $[X] (+[X]% vs last month)
• ACoS: [X]% (target: [X]%)
• TACoS: [X]%

FULL REPORT: [Attached/Link]

Can we schedule a 30-min call this week to discuss? I have some recommendations for next month.

[Your Name]
```

### Escalation Notice
```
Subject: ⚠️ URGENT: PPC Alert — [Client Name]

Hi [Client Name],

I noticed an issue that needs your attention:

ISSUE: [Brief description — e.g., "Product X is out of stock in FBA"]
IMPACT: [What's affected — e.g., "PPC campaigns for this product are paused; ~$50/day in potential sales affected"]
TIMELINE: [When it started — e.g., "Started this morning at 9 AM"]
ACTION TAKEN: [What you did — e.g., "Paused all campaigns for this product to prevent wasted spend"]
NEXT STEP: [What client needs to do — e.g., "Please restock FBA inventory or switch to FBM"]

Let me know how you'd like to proceed.

[Your Name]
```

---

## Template 5: Keyword Research Template

### Research Spreadsheet
```
| Keyword | Source | Search Volume | Competition | Relevance (1-10) | CPC Est. | Priority | Campaign Assignment |
|---------|--------|---------------|-------------|-------------------|----------|----------|---------------------|
| bluetooth widget | Cerebro | 12,000/mo | High | 10 | $1.20 | TOP 5 | Manual Exact |
| wireless widget | Magnet | 8,500/mo | Medium | 9 | $0.95 | TOP 10 | Manual Exact |
| widget for home | Cerebro | 3,200/mo | Low | 8 | $0.60 | EXPAND | Manual Phrase |
| best widget 2026 | Magnet | 2,100/mo | Medium | 7 | $0.85 | EXPAND | Manual Phrase |
| widget accessories | Cerebro | 1,500/mo | Low | 6 | $0.45 | TEST | Auto |
```

### Research Process
1. **Cerebro** (competitor ASIN) → Find keywords competitors rank for
2. **Magnet** (seed keyword) → Expand to related terms
3. **Amazon Auto** → Let Amazon discover terms
4. **Manual Search** → Type seed keyword, see suggestions
5. **Google Trends** → Seasonal demand patterns

### Priority Rules
| Priority | Criteria | Campaign |
|----------|----------|----------|
| TOP 5 | Volume > 5K, Relevance 9-10 | Manual Exact |
| TOP 10 | Volume > 2K, Relevance 7-8 | Manual Exact |
| EXPAND | Volume > 1K, Relevance 6-7 | Manual Phrase |
| TEST | Volume > 500, Relevance 5-6 | Auto |

---

## Template 6: Campaign Audit Checklist

```
ACCOUNT AUDIT CHECKLIST
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

STRUCTURE
□ Campaign naming convention consistent
□ Portfolio organization logical
□ No more than 5-7 campaigns per product
□ Budget allocation follows 70/20/10 rule
□ Minimum $10/day per active campaign

KEYWORDS
□ Auto campaigns running for discovery
□ Manual exact match for proven terms
□ Phrase/broad for expansion
□ Negative keywords implemented
□ No keyword overlap between campaigns

BIDS & BUDGETS
□ Bids aligned with ACoS targets
□ No campaigns hitting daily budget before end of day
□ Placement adjustments optimized
□ Dynamic bidding strategy set correctly

LISTINGS
□ Main image optimized (high CTR)
□ Title includes primary keywords
□ Bullet points highlight benefits
□ A+ Content live (if Brand Registry)
□ Price competitive in category

REPORTING
□ Search term reports downloaded weekly
□ Performance tracked over time
□ Client reports delivered on schedule
□ Changes documented

SECURITY
□ Account access limited to authorized users
□ Two-factor authentication enabled
□ Billing information secure
```

---

## Template 7: A/B Test Tracker

```
| Test ID | Product | Element | Control | Variant | Metric | Start Date | End Date | Sample Size | Control Result | Variant Result | Winner | Confidence | Notes |
|---------|---------|---------|---------|---------|--------|------------|----------|-------------|----------------|----------------|--------|------------|-------|
| AB-001 | Widget X | Main Image | White bg | Lifestyle | CTR | 2026-07-01 | 2026-07-15 | 5,000 imp. | 0.35% | 0.52% | Variant | 95% | Lifestyle won |
| AB-002 | Widget X | Price | $29.99 | $27.99 | CVR | 2026-07-15 | 2026-07-29 | 3,000 clicks | 8.2% | 9.1% | Variant | 88% | Extend test |
| AB-003 | Gadget Y | Title | Short | Keyword-rich | CTR | 2026-08-01 | 2026-08-15 | 4,000 imp. | — | — | — | — | In progress |
```

---

## Using Templates in Coaching

### For VA Training
1. Provide blank templates as downloadable files
2. Walk through each template line-by-line
3. Have student fill in with real account data
4. Review and correct their entries
5. Gradually have them build templates from scratch

### For Assessment
- Give student raw data
- Ask them to fill in: Search Term Analysis, Performance Report, Audit Checklist
- Grade on: accuracy, completeness, action recommendations

### For Client Work
- Templates ensure consistency across clients
- New VAs can produce professional output immediately
- Client recognizes quality and reliability

---
*Sources: eComEngine search term template, Supermetrics PPC templates, PorterMetrics Amazon templates, Amazon Ads documentation*
*Last updated: 2026-06-29*
