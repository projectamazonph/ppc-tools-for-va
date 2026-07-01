---
type: concept
title: Amazon PPC Automation Tools & Processes
domain: Amazon PPC / VA Training
created: 2026-06-29
related: [[ppc-sops]], [ppc-workflows]], [ppc-templates]]
---

# Amazon PPC Automation Tools & Processes

> Comprehensive guide to PPC automation: tools, rules, workflows, and when to automate vs. manual manage.

---

## What PPC Automation Actually Automates

| Task | Automatable? | Tool |
|------|-------------|------|
| Bid adjustments | ✅ Yes | Adtomic, Ad Badger, rules-based tools |
| Budget pacing | ✅ Yes | Most PPC tools, Amazon rules |
| Negative keyword harvesting | ⚠️ Partial | Adtomic, manual review recommended |
| Keyword harvesting | ⚠️ Partial | Adtomic, manual verification needed |
| Search term analysis | ❌ No (needs judgment) | Manual — the VA's expertise |
| Campaign strategy | ❌ No (needs expertise) | Manual — the specialist's value |
| Client communication | ❌ No (needs relationship) | Manual — the VA's professionalism |
| Reporting | ⚠️ Partial | Automated dashboards + human analysis |

**Key Insight:** Automation handles the *mechanical* work. You handle the *strategic* work. The VA who can do both is worth 2-3x more than one who only automates.

---

## Tool Comparison: Top 10 Amazon PPC Tools (2026)

### Tier 1: Essential (Everyone Should Know)

#### 1. Amazon Campaign Manager (Native)
- **Price:** Free (included with Seller Central)
- **Best for:** Learning fundamentals, small accounts
- **Features:** Basic campaign creation, bid adjustments, search term reports
- **Limitations:** No automation, no AI, clunky interface, manual everything
- **Verdict:** Good starting point, you'll outgrow it fast

#### 2. Helium 10 Adtomic
- **Price:** $79-$229/mo (included in Helium 10 plans)
- **Best for:** Sellers using Helium 10 ecosystem
- **Features:** AI-powered bid optimization, keyword harvesting, negative keyword automation, rule-based automation
- **Automation Level:** Rules-based + AI learning
- **Key Advantage:** Integrates with Cerebro/Magnet for keyword research
- **Key Limitation:** 2% ad spend fee on some plans
- **Verdict:** Best all-in-one for mid-size sellers

#### 3. Helium 10 (Full Suite)
- **Price:** $79-$229/mo
- **Key Tools:**
  - **Cerebro** — Competitor keyword research
  - **Magnet** — Keyword discovery
  - **Adtomic** — PPC automation
  - **Keyword Tracker** — Rank monitoring
  - **Market Tracker** — Market share tracking
- **Verdict:** The Swiss Army knife of Amazon selling

### Tier 2: Professional (Agency/Advanced)

#### 4. Perpetua (formerly Sellics)
- **Price:** Custom (based on ad spend)
- **Best for:** Large accounts, agencies
- **Features:** AI-driven optimization, cross-channel (Amazon + Walmart), advanced analytics
- **Automation Level:** Full AI
- **Verdict:** Enterprise-grade, price reflects it

#### 5. Quartile
- **Price:** Custom (based on ad spend)
- **Best for:** Enterprise brands
- **Features:** AI-powered, cross-marketplace, advanced attribution
- **Automation Level:** Full AI
- **Verdict:** Best for $100K+/month ad spend

#### 6. Teikametrics
- **Price:** Free tier available, paid plans scale
- **Best for:** Multi-marketplace sellers
- **Features:** AI bid optimization, Walmart integration, analytics
- **Automation Level:** AI-driven
- **Verdict:** Good for Amazon + Walmart sellers

### Tier 3: Budget-Friendly

#### 7. PPC Entourage (Carbon6)
- **Price:** From $50/mo
- **Best for:** Budget-conscious sellers
- **Features:** Dayparting, automated bid rules, keyword harvesting
- **Automation Level:** Rules-based
- **Verdict:** Affordable entry point for automation

#### 8. BidX
- **Price:** From $49/mo
- **Best for:** Small to mid-size sellers
- **Features:** Bid automation, keyword management, bulk operations
- **Automation Level:** Rules-based
- **Verdict:** Simple, affordable, gets the job done

#### 9. Ad Badger
- **Price:** From $99/mo
- **Best for:** Sellers wanting strong negative keyword automation
- **Features:** Bid optimization, negative keyword automation, dayparting
- **Automation Level:** Rules-based + some AI
- **Verdict:** Strong on negative keywords

#### 10. Zon.Tools
- **Price:** From $9/mo (very affordable)
- **Best for:** Beginners, very small budgets
- **Features:** Basic bid automation, campaign management
- **Automation Level:** Rules-based
- **Verdict:** Cheapest option, limited features

### Tier 4: Free/Low-Cost

#### 11. Amazon Bulk Operations
- **Price:** Free
- **Features:** Download CSV, make changes in Excel, upload
- **Best for:** Budget management, bulk bid changes
- **Verdict:** Free and powerful if you know Excel

#### 12. Google Sheets + Amazon API
- **Price:** Free (DIY)
- **Features:** Custom reporting, data analysis, automation scripts
- **Best for:** Tech-savvy sellers who want custom solutions
- **Verdict:** Maximum flexibility, requires technical skill

---

## Automation Rules: What to Set Up

### Bid Automation Rules

| Rule | Condition | Action | Frequency |
|------|-----------|--------|-----------|
| ACoS Too High | ACoS > Target × 1.5 | Reduce bid by 15% | Daily |
| ACoS Perfect | ACoS within ±20% of target | No change | Daily |
| ACoS Too Low | ACoS < Target × 0.5 AND Orders > 3 | Increase bid by 10% | Daily |
| No Conversions | 20+ clicks, 0 orders | Negate keyword | Weekly |
| New Keyword | < 14 days data | No changes | Wait |
| CPC Spike | CPC increased > 25% in 7 days | Investigate, reduce if needed | Weekly |

### Budget Automation Rules

| Rule | Condition | Action |
|------|-----------|--------|
| Budget Hit Early | Campaign hits budget before 5 PM | Increase by 20% (if profitable) |
| Budget Not Spent | < 50% budget spent by end of day | Check: paused? Low bids? OOS? |
| Weekly Scale | Campaign ACoS < target for 7 days | Increase budget by 15% |
| Monthly Review | Monthly ACoS > target | Reduce budget by 10% |

### Negative Keyword Rules

| Rule | Condition | Action |
|------|-----------|--------|
| Waste Detector | 15+ clicks, 0 orders | Add negative exact |
| High Cost Waste | ACoS > 3x break-even | Add negative exact |
| Irrelevant Term | Term has nothing to do with product | Add negative phrase |
| Brand Leak | Non-branded term in brand campaign | Add negative phrase |
| Competitor Term | Competitor brand in non-comp campaign | Consider negating |

---

## Helium 10 Adtomic: Setup Guide

### Step 1: Connect Account
1. Go to Adtomic dashboard
2. Connect Amazon Advertising Console
3. Select campaigns to manage

### Step 2: Set ACoS Targets
- Per campaign: set target ACoS
- Default: use break-even ACoS as starting point
- Adjust based on goals (lower for profit, higher for growth)

### Step 3: Configure Rules
```
Rule 1: If ACoS > Target × 1.5 for 3+ days → Reduce bid by 15%
Rule 2: If ACoS < Target × 0.5 AND Orders > 5 for 7 days → Increase bid by 10%
Rule 3: If Clicks > 20 AND Orders = 0 → Add as negative keyword
Rule 4: If new keyword < 14 days → No changes (learning phase)
```

### Step 4: Set Guardrails
- Minimum bid: $0.30 (don't go below this)
- Maximum bid: $5.00 (don't go above this without approval)
- Maximum daily change: 20% (prevent volatility)

### Step 5: Monitor
- Check Adtomic dashboard daily (5 min)
- Review changes made by automation
- Override if needed (document why)
- Weekly: review overall performance trend

---

## DIY Automation: Google Sheets + Scripts

### Basic Automation Script (Google Apps Script)
```javascript
// Auto-pull Amazon data and flag anomalies
function checkPPCAnomalies() {
  var sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
  var data = sheet.getDataRange().getValues();
  
  for (var i = 1; i < data.length; i++) {
    var acos = data[i][3]; // Column D = ACoS
    var target = data[i][4]; // Column E = Target ACoS
    
    if (acos > target * 1.5) {
      // Flag: ACoS too high
      sheet.getRange(i + 1, 8).setValue("⚠️ REDUCE BID");
    } else if (acos < target * 0.5) {
      // Flag: ACoS very low — room to scale
      sheet.getRange(i + 1, 8).setValue("📈 INCREASE BID");
    } else {
      sheet.getRange(i + 1, 8).setValue("✅ OK");
    }
  }
}
```

### Automated Report Generator
```javascript
// Generate weekly report from raw data
function generateWeeklyReport() {
  var ss = SpreadsheetApp.getActiveSpreadsheet();
  var raw = ss.getSheetByName("Raw Data");
  var report = ss.getSheetByName("Weekly Report");
  
  // Calculate totals
  var totalSpend = sumColumn(raw, "Spend");
  var totalRevenue = sumColumn(raw, "Revenue");
  var acos = (totalSpend / totalRevenue * 100).toFixed(1);
  
  // Write to report
  report.getRange("B2").setValue(totalSpend);
  report.getRange("B3").setValue(totalRevenue);
  report.getRange("B4").setValue(acos + "%");
}
```

---

## When to Automate vs. Manual Manage

### Automate These
| Task | Why Automate | Risk Level |
|------|-------------|------------|
| Bid adjustments (proven campaigns) | Consistent, data-driven | Low |
| Budget pacing | Prevent overspend | Low |
| Negative keyword harvesting (clear rules) | Save time, reduce waste | Low |
| Reporting (data collection) | Consistent, fast | Low |
| Alert monitoring (anomalies) | Catch issues early | Low |

### Keep Manual These
| Task | Why Manual | Risk if Automated Wrong |
|------|-----------|------------------------|
| Campaign strategy | Requires business judgment | Wrong direction = wasted budget |
| New product launches | Unique per product | Generic rules don't fit |
| Client communication | Relationship-driven | Tone/expectation mismatches |
| Search term analysis (edge cases) | Needs context and nuance | False positives/negatives |
| Seasonal adjustments | Requires market knowledge | Rules can't predict trends |
| Competitor response | Strategic decision | Over-reaction or under-reaction |

### The Hybrid Approach
**Best practice:** Automate the *execution*, manual the *decisions*.

Example:
1. **Manual:** You decide to reduce bids on keyword X (strategic decision)
2. **Automate:** The tool executes the 15% bid reduction (mechanical task)
3. **Manual:** You review results after 7 days and decide next step

---

## Automation Maturity Model

### Level 1: Manual (Starting)
- All work done manually in Amazon Console
- No automation tools
- Time: 15-20 hours/week per account
- Best for: Learning, 1-2 small accounts

### Level 2: Basic Rules
- Using bulk operations for bid changes
- Basic negative keyword rules
- Spreadsheet tracking
- Time: 10-15 hours/week per account
- Best for: 2-5 accounts

### Level 3: Tool-Assisted
- Helium 10 Adtomic or similar
- Automated bid rules active
- Automated reporting dashboards
- Time: 5-10 hours/week per account
- Best for: 5-10 accounts

### Level 4: Smart Automation
- AI-driven bid optimization
- Automated harvesting + negation
- Predictive budget allocation
- Time: 3-5 hours/week per account
- Best for: 10+ accounts, agency level

### Level 5: Full Stack
- Custom automation (API + scripts)
- Cross-marketplace optimization
- Automated client reporting
- Predictive analytics
- Time: 2-3 hours/week per account
- Best for: Enterprise, large agencies

---

## Cost-Benefit Analysis

### Tool Costs vs. Time Saved
| Tool | Monthly Cost | Time Saved/Week | Hourly Rate | Net Value |
|------|-------------|-----------------|-------------|-----------|
| Amazon Console (free) | $0 | 0 hrs | — | Baseline |
| BidX ($49/mo) | $49 | 3 hrs | $15/hr = $45/wk | +$131/mo |
| Ad Badger ($99/mo) | $99 | 5 hrs | $15/hr = $75/wk | +$201/mo |
| Helium 10 ($149/mo) | $149 | 8 hrs | $15/hr = $120/wk | +$331/mo |
| Perpetua (custom) | $500+ | 15 hrs | $15/hr = $225/wk | +$400/mo |

**Key calculation:** If your hourly rate is $15 (typical VA rate), and a tool saves you 8 hours/week, that's $120/week or $480/month in time value. A $149/month tool that saves 8 hours = net positive $331/month.

### ROI Formula
```
ROI = (Hours Saved × Hourly Rate × 4 weeks) - Tool Cost

Example (Helium 10):
ROI = (8 hrs × $15 × 4) - $149 = $480 - $149 = +$331/month
```

---

## Training VAs on Automation

### Progressive Automation Training
1. **Month 1-2:** Manual only — learn the fundamentals
2. **Month 3:** Introduce bulk operations (Excel-based)
3. **Month 4:** Set up basic automation rules (bid rules)
4. **Month 5:** Introduce Helium 10 Adtomic (if available)
5. **Month 6:** Full automation management with manual oversight

### Assessment Questions
1. "When should you NOT rely on automation?" (Answer: edge cases, new products, strategy decisions)
2. "How do you verify automation is working correctly?" (Answer: daily dashboard check, weekly override review)
3. "What's the risk of 'set and forget' automation?" (Answer: market changes, competitor actions, listing changes)

---

## Quick Reference: Tool Selection Guide

```
START: What's your budget?
│
├─ $0 (Free only)
│  └─ Amazon Console + Bulk Operations + Google Sheets
│
├─ $50-100/month
│  ├─ Zon.Tools ($9) — basics
│  ├─ BidX ($49) — good value
│  └─ PPC Entourage ($50) — solid features
│
├─ $100-200/month
│  ├─ Helium 10 ($149) — best all-in-one
│  └─ Ad Badger ($99) — strong negation
│
├─ $200-500/month
│  ├─ Helium 10 Premium ($229)
│  └─ Teikametrics (custom)
│
└─ $500+/month
   ├─ Perpetua (enterprise)
   ├─ Quartile (enterprise)
   └─ Custom API solutions
```

---
*Sources: Helium 10 blog, IGPPC comparison guide, Jarvio top 10 tools, Reddit r/FulfillmentByAmazon, Amazon Ads documentation*
*Last updated: 2026-06-29*
