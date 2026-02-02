# Financial Analysis Prompts

Use these prompts with the AR aging report (09-ar-aging-report.tsv) and monthly revenue summary (10-monthly-revenue-summary.tsv)

---

## Prompt 1: AR Aging Summary

```
ROLE:
You are a financial analyst at Walker Logistics preparing an accounts receivable summary for the weekly collections meeting.

CONTEXT:
The collections team meets every Monday to review overdue accounts and prioritize collection efforts. They need a clear, actionable summary.

Key thresholds:
- Over $10K past due: Escalate to management
- Over 60 days: Consider hold on new shipments
- Over 90 days: Consider collections referral

TASK:
Based on the AR aging data provided, create a summary that includes:

1. EXECUTIVE SUMMARY
   - Total AR outstanding
   - Total past due (and % of total)
   - Week-over-week change (assume last week was similar)

2. AGING BUCKETS
   - Amount and count in each bucket
   - Visual distribution

3. TOP COLLECTION PRIORITIES
   - Ranked list of accounts to focus on
   - For each: amount, days overdue, last contact, recommended action

4. ACCOUNTS OF CONCERN
   - Any accounts trending in wrong direction
   - New customers with payment issues
   - Strategic accounts with AR issues

5. RECOMMENDED ACTIONS
   - Specific calls/emails to make this week
   - Any accounts to escalate
   - Any accounts to place on credit hold

OUTPUT FORMAT:
Meeting-ready summary, one page. Use a table for the priority list. Include specific dollar amounts and contact names.

---

[PASTE AR AGING DATA HERE]
```

---

## Prompt 2: Collection Email Drafts

```
ROLE:
You are an accounts receivable specialist drafting collection emails for overdue accounts.

CONTEXT:
We need to contact several customers about past-due invoices. The tone should be professional and firm but maintain the customer relationship.

Collection approach by days overdue:
- 1-15 days: Friendly reminder
- 16-30 days: Firmer follow-up
- 31-60 days: Escalation warning
- 61-90 days: Final notice before action
- 90+ days: Collections referral warning

TASK:
Based on the AR aging data, draft collection emails for the following accounts:

1. Acme Corporation (7 days overdue, $12,450)
   - Good customer, probably just an oversight
   
2. Delta Retail Systems (37 days overdue, $16,320)
   - They promised payment that didn't arrive
   
3. Global Parts Inc (78 days overdue, $29,800)
   - On payment plan, need to confirm compliance
   
4. Velocity Distribution (32 days overdue, $40,800)
   - Strategic account in contract renewal talks
   
5. Pacific Traders (98 days overdue, $4,200)
   - Former customer, disputed final invoice

For each email, customize the tone to the situation and relationship.

OUTPUT FORMAT:
Five separate email drafts, each with subject line. Note the recommended sender (AR clerk vs AR manager vs sales rep).

---

[PASTE AR AGING DATA FOR CONTEXT]
```

---

## Prompt 3: Cash Flow Projection

```
ROLE:
You are a financial analyst creating a 4-week cash flow projection.

CONTEXT:
Management wants to understand expected cash inflows from AR collections to plan for upcoming disbursements.

Assumptions:
- Current invoices: 95% collected within terms
- 1-30 days overdue: 85% collected within next 2 weeks
- 31-60 days overdue: 60% collected within next 4 weeks
- 61-90 days overdue: 40% collected within next 4 weeks
- 90+ days: 10% chance of collection

Weekly disbursements (approximate):
- Week 1: $195,000
- Week 2: $210,000
- Week 3: $205,000
- Week 4: $198,000

TASK:
Based on the AR aging data, create a 4-week cash flow projection that shows:

1. Expected collections by week (with assumptions)
2. Expected disbursements by week
3. Net cash flow by week
4. Cumulative cash position
5. Any weeks where we might have a shortfall

OUTPUT FORMAT:
Cash flow table by week, followed by a brief narrative explaining the key drivers and any concerns.

---

[PASTE AR AGING DATA HERE]
```

---

## Prompt 4: Monthly Revenue Analysis

```
ROLE:
You are a financial analyst preparing a monthly revenue analysis for the executive team.

CONTEXT:
The executive team wants to understand revenue trends and any accounts requiring attention. They have limited time, so the analysis must be concise and actionable.

Key metrics they care about:
- Total revenue vs budget vs prior month
- Customer concentration (any over-reliance on single accounts)
- New vs existing customer revenue
- Revenue by service type
- Facility utilization

TASK:
Based on the monthly revenue data, create an executive summary that includes:

1. HEADLINE METRICS
   - Month-to-date revenue
   - Variance to budget ($ and %)
   - Variance to prior month ($ and %)

2. CUSTOMER ANALYSIS
   - Top 5 customers by revenue
   - Any concentration concerns
   - Customers trending up/down significantly
   - New customer performance

3. SERVICE MIX
   - Revenue by service type
   - Any shifts in mix from prior periods

4. LOCATION PERFORMANCE
   - Revenue by facility
   - Utilization concerns
   - Capacity constraints

5. ITEMS REQUIRING ATTENTION
   - Accounts declining
   - Accounts at risk
   - Growth opportunities
   - Capacity decisions needed

OUTPUT FORMAT:
Executive dashboard format - mostly bullets and tables. Include one recommendation or action item for each concern noted.

---

[PASTE REVENUE SUMMARY DATA HERE]
```

---

## Prompt 5: Account Health Assessment

```
ROLE:
You are a customer success analyst evaluating the health of key accounts.

CONTEXT:
We want to proactively identify at-risk accounts before they churn. Combining financial data with operational metrics gives a better picture.

Health indicators:
- Revenue trend (growing, flat, declining)
- Payment behavior (current, slow, problematic)
- Volume trend (increasing, stable, decreasing)
- Relationship length
- Contract status

Risk signals:
- Revenue declining >10%
- Payment consistently late
- Mentioned "evaluating options"
- Contract expiring soon with no renewal discussion

TASK:
Based on the financial data provided, create an account health scorecard that:

1. Rates each major account (Green/Yellow/Red)
2. Identifies the top 3 at-risk accounts
3. Notes early warning signs
4. Recommends proactive actions

OUTPUT FORMAT:
Scorecard format with color-coded ratings. Include a brief action recommendation for Yellow and Red accounts.

---

[PASTE AR AGING AND REVENUE DATA HERE]
```

---

## Prompt 6: Financial Executive Summary

```
ROLE:
You are the Controller at Walker Logistics preparing a weekly financial summary for the CEO.

CONTEXT:
The CEO wants a single-page summary every Monday morning covering AR, revenue, and cash position. She reads it in about 2 minutes.

She cares about:
- Are we on track for the month?
- Any surprises (good or bad)?
- What actions are being taken on issues?
- What does she need to know or decide?

TASK:
Combine the AR aging and revenue data to create a CEO briefing that includes:

1. BOTTOM LINE (3-4 bullet points)
   - Overall financial health this week
   - Key number vs target
   - Main concern and what we're doing about it

2. REVENUE SNAPSHOT
   - MTD vs budget
   - Projection for month-end
   - New business won/lost

3. AR SNAPSHOT
   - Total AR and past due %
   - Collection actions this week
   - Anything over $25K past due

4. ITEMS FOR YOUR AWARENESS
   - Any escalations needed
   - Any decisions required
   - Upcoming items on the horizon

OUTPUT FORMAT:
One page maximum. Use bold headers. Lead with the most important information. No fluff.

---

[PASTE BOTH AR AND REVENUE DATA]
```

---

## Prompt 7: Customer Profitability Quick Analysis

```
ROLE:
You are a financial analyst evaluating customer profitability.

CONTEXT:
Not all revenue is equal. We want to understand which customers are most profitable so we can prioritize accordingly.

General profitability drivers:
- Revenue mix (storage vs handling vs VAS)
- Payment terms and behavior
- Service complexity
- Volume consistency

High-margin indicators: Storage-heavy, standard service, pays on time
Low-margin indicators: Handling-heavy, lots of special requirements, slow payer

TASK:
Based on the revenue data provided, create a quick profitability analysis that:

1. Ranks customers by estimated profitability (not just revenue)
2. Identifies which customers might be underpriced
3. Identifies which customers provide the best margin
4. Notes any accounts where we should consider rate increases
5. Notes any accounts we should try to grow

OUTPUT FORMAT:
Ranked list with brief rationale. Include recommendations for the top 3 accounts to focus on for profitability improvement.

---

[PASTE REVENUE DATA HERE]
```
