# Master Prompt Library - Quick Reference

This guide provides a quick reference to all prompts organized by use case.

---

## How to Use These Prompts

1. **Find the prompt** for your task in this reference
2. **Copy the prompt** from the appropriate file
3. **Paste your data** where indicated (e.g., [PASTE RFP HERE])
4. **Run in any model** - ChatGPT, Claude, Gemini, etc.
5. **Iterate** - If the output isn't right, adjust the prompt and try again

---

## Prompt Files

| File | Use Case | # of Prompts |
|------|----------|--------------|
| 01-rfp-analysis-prompts.md | Analyzing RFPs and building quotes | 5 |
| 02-rate-lookup-prompts.md | Responding to rate requests | 8 |
| 03-customer-communication-prompts.md | Writing customer emails | 8 |
| 04-process-mapping-prompts.md | Creating flowcharts and documentation | 6 |
| 05-customer-onboarding-prompts.md | New customer implementation | 7 |
| 06-financial-analysis-prompts.md | AR and revenue analysis | 7 |

---

## Quick Reference by Task

### "I need to analyze an RFP..."

| Task | Prompt File | Prompt Name |
|------|-------------|-------------|
| Extract key requirements | 01 | Basic RFP Extraction |
| Assess if it's a good fit | 01 | RFP Fit Assessment |
| Generate questions for discovery call | 01 | Generate Clarifying Questions |
| Write the scope of work | 01 | Scope of Work Draft |
| Position against competitors | 01 | Competitive Positioning |

---

### "I need to respond to a rate request..."

| Task | Prompt File | Prompt Name |
|------|-------------|-------------|
| Any rate request (master prompt) | 02 | Master Rate Lookup Prompt |
| Simple LTL shipment | 02 | Rate Request #1 |
| Weekly/recurring FTL lane | 02 | Rate Request #2 |
| LTL with accessorials (liftgate, etc) | 02 | Rate Request #3 |
| Urgent/expedited shipment | 02 | Rate Request #4 |
| Multi-stop truckload | 02 | Rate Request #5 |
| Vague request (need more info) | 02 | Rate Request #6 |
| International/cross-border | 02 | Rate Request #7 |

---

### "I need to write a customer email..."

| Situation | Prompt File | Prompt Name |
|-----------|-------------|-------------|
| Shipment is delayed | 03 | Scenario A: Delay Notification |
| Following up on a quote | 03 | Scenario B: Quote Follow-Up |
| Responding to damage claim | 03 | Scenario C: Damage Claim Response |
| Apologizing for our mistake | 03 | Scenario D: Service Issue Apology |
| Starting contract renewal conversation | 03 | Scenario E: Contract Renewal |
| Notifying of price increase | 03 | Scenario F: Price Increase |
| Trying to win back lost customer | 03 | Scenario G: Win-Back Attempt |
| Thanking a customer | 03 | Scenario H: Thank You |

---

### "I need to create a process map..."

| Task | Prompt File | Prompt Name |
|------|-------------|-------------|
| Basic flowchart from description | 04 | Basic Process Flowchart |
| Flowchart with pain points highlighted | 04 | Process Map with Pain Points |
| Find where AI can help | 04 | Identify AI Integration Points |
| Current state vs future state | 04 | Current State vs Future State |
| Swimlane diagram (who does what) | 04 | Swimlane Diagram |
| Full process documentation | 04 | Process Documentation Generator |

---

### "I need to onboard a new customer..."

| Task | Prompt File | Prompt Name |
|------|-------------|-------------|
| Generate task list | 05 | Onboarding Task Generator |
| Create implementation timeline | 05 | Implementation Timeline |
| Prepare kick-off meeting | 05 | Kick-Off Meeting Agenda |
| Create welcome packet | 05 | Welcome Packet Content |
| Assess implementation risks | 05 | Risk Assessment |
| Write status update | 05 | Status Update Generator |
| Create customer-specific SOP | 05 | SOP Generator |

---

### "I need to analyze financial data..."

| Task | Prompt File | Prompt Name |
|------|-------------|-------------|
| Summarize AR for collections meeting | 06 | AR Aging Summary |
| Draft collection emails | 06 | Collection Email Drafts |
| Project cash flow | 06 | Cash Flow Projection |
| Analyze monthly revenue | 06 | Monthly Revenue Analysis |
| Assess account health | 06 | Account Health Assessment |
| CEO weekly summary | 06 | Financial Executive Summary |
| Analyze customer profitability | 06 | Customer Profitability Analysis |

---

## The Four Building Blocks (Always Use This Structure)

Every prompt should include:

```
ROLE:
[Who is the AI acting as?]

CONTEXT:
[What background information does it need?]

TASK:
[What specifically should it do?]

OUTPUT FORMAT:
[How should the output look?]
```

---

## Pro Tips

### Make Prompts Better

1. **Be specific** - "Write a 150-word email" not "Write a short email"
2. **Give examples** - Show what good output looks like
3. **State constraints** - "Do not include..." or "Make sure to..."
4. **Request structure** - "Use bullet points" or "Create a table"

### When Output Isn't Right

1. **Add more context** - The model might be missing information
2. **Be more specific about format** - Show exactly what you want
3. **Break into steps** - "First... then... finally..."
4. **Try a different model** - Claude might handle it better than GPT (or vice versa)

### For Business-Critical Output

1. **Always verify facts** - Especially numbers, rates, dates
2. **Check for hallucinations** - Did it make something up?
3. **Review tone** - Is it appropriate for the recipient?
4. **Add your judgment** - AI is a first draft, not final copy

---

## Sample Workflow: Using Multiple Prompts Together

**Scenario: New RFP arrives, need to respond**

1. Use **RFP Fit Assessment** → Decide if we should pursue
2. Use **Generate Clarifying Questions** → Prepare for discovery call
3. Use **Scope of Work Draft** → Create proposal content
4. Use **Competitive Positioning** → Sharpen our message
5. Use **Quote Follow-Up** → Send if no response

**Scenario: New customer signs, need to onboard**

1. Use **Risk Assessment** → Identify potential issues
2. Use **Onboarding Task Generator** → Create task list
3. Use **Implementation Timeline** → Build project plan
4. Use **Kick-Off Meeting Agenda** → Prepare first meeting
5. Use **Welcome Packet Content** → Send to customer
6. Use **SOP Generator** → Document their requirements
7. Use **Status Update Generator** → Keep stakeholders informed

---

## Customization

These prompts are templates. Always customize by:

- Adding Walker-specific details (locations, services, rates)
- Including relevant customer history
- Adjusting tone for the specific relationship
- Adding any constraints or requirements

The more context you provide, the better the output.
