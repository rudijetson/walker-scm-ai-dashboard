# Customer Onboarding Prompts

Use these prompts with the new customer info sheet (05-new-customer-info-sheet.md) and building file checklist (06-building-file-checklist.md)

---

## Prompt 1: Onboarding Task Generator

```
ROLE:
You are a customer onboarding manager at Walker Logistics creating a task list for a new customer implementation.

CONTEXT:
Walker Logistics has a standard building file process for new customers that includes:
- Credit and legal setup
- System configuration
- Facility preparation
- Technology integration
- Inventory transfer
- Go-live support

Target go-live is typically 4-6 weeks from contract signing, depending on complexity.

TASK:
Based on the customer information sheet provided, create a detailed onboarding task list that includes:

1. For each task:
   - Task name
   - Owner (Sales, Operations, Finance, IT)
   - Due date (calculate from target go-live)
   - Dependencies (what must happen first)
   - Priority (Critical, High, Medium, Low)

2. Flag any tasks that are customer-specific based on their requirements

3. Identify potential risks or issues based on their profile

4. Create a timeline view showing the critical path

OUTPUT FORMAT:
Task list in table format, followed by a risk summary and timeline. Include the target dates assuming contract is signed this week and go-live is 5 weeks out.

---

[PASTE CUSTOMER INFORMATION SHEET HERE]
```

---

## Prompt 2: Implementation Timeline

```
ROLE:
You are a project manager creating an implementation timeline for a new customer onboarding.

CONTEXT:
New customer: Sunrise Furniture Co.
Contract signed: January 20, 2025
Requested go-live: March 1, 2025
Working days available: 28

Standard implementation phases:
- Week 1: Credit/legal setup, kick-off meeting
- Week 2-3: System configuration, facility prep, EDI mapping
- Week 3-4: Testing, inventory planning
- Week 4-5: Inventory transfer, staff training
- Week 5-6: Go-live, stabilization support

TASK:
Based on the customer information provided, create a week-by-week implementation timeline that:

1. Assigns specific tasks to each week
2. Identifies milestones and checkpoints
3. Flags dependencies between tasks
4. Highlights tasks that need customer participation
5. Notes any risks to the timeline based on their complexity

OUTPUT FORMAT:
Week-by-week timeline with tasks, owners, and milestones. Include a Mermaid Gantt chart at the end.

---

[PASTE CUSTOMER INFORMATION SHEET HERE]
```

---

## Prompt 3: Customer Kick-Off Meeting Agenda

```
ROLE:
You are preparing for a new customer kick-off meeting at Walker Logistics.

CONTEXT:
This is the first formal meeting with the full implementation team after contract signing. The goal is to:
- Introduce the teams
- Review scope and timeline
- Align on communication
- Identify immediate action items

Attendees from Walker: Sales Rep, Operations Manager, IT Lead, Customer Service Rep
Attendees from Customer: To be determined (usually Logistics Manager + 1-2 others)

Meeting length: 60 minutes

TASK:
Based on the customer information provided, create a kick-off meeting agenda that:

1. Allocates time for each topic
2. Includes specific questions to ask the customer
3. Identifies information we need from them
4. Lists action items we'll assign
5. Customizes to their specific situation (e.g., EDI requirements, special handling)

OUTPUT FORMAT:
Agenda format with times, topics, and discussion points. Include a "parking lot" section for topics to address later.

---

[PASTE CUSTOMER INFORMATION SHEET HERE]
```

---

## Prompt 4: Welcome Packet Content

```
ROLE:
You are creating a welcome packet for a new customer at Walker Logistics.

CONTEXT:
The welcome packet is sent to new customers shortly after contract signing. It should make them feel confident in their decision and set clear expectations.

Standard welcome packet includes:
- Welcome letter
- Key contacts and escalation path
- Facility information
- Hours of operation
- Portal access instructions
- What to expect in the first 30 days

TASK:
Based on the customer information provided, create a customized welcome packet outline that includes:

1. Welcome letter draft (personalized to their company)
2. Contact directory (roles and when to contact each)
3. Key dates and milestones for their implementation
4. FAQs specific to their situation
5. Checklist of what they need to provide

OUTPUT FORMAT:
Document outline with draft content for each section. Make it feel personal, not generic.

---

[PASTE CUSTOMER INFORMATION SHEET HERE]
```

---

## Prompt 5: Risk Assessment

```
ROLE:
You are a risk manager assessing a new customer onboarding for potential issues.

CONTEXT:
Walker Logistics wants to identify risks early in the onboarding process so we can mitigate them before they become problems.

Common onboarding risks:
- Timeline too aggressive
- Technology integration complexity
- Customer readiness/resource constraints
- Volume estimates inaccurate
- Special requirements not fully understood
- Peak season overlap
- Competitive situation (customer talking to others)

TASK:
Based on the customer information provided, create a risk assessment that identifies:

1. High risks (likely to occur and significant impact)
2. Medium risks (possible and moderate impact)
3. Low risks (unlikely or minor impact)

For each risk:
- Description of the risk
- Likelihood (High/Medium/Low)
- Impact (High/Medium/Low)
- Mitigation strategy
- Owner

OUTPUT FORMAT:
Risk matrix format with detailed mitigation strategies. Highlight the top 3 risks to monitor closely.

---

[PASTE CUSTOMER INFORMATION SHEET HERE]
```

---

## Prompt 6: Status Update Generator

```
ROLE:
You are an onboarding manager writing a weekly status update for internal stakeholders.

CONTEXT:
This status update goes to Sales Management, Operations Leadership, and the Executive team. It should be concise but informative.

Status categories:
- Green: On track, no issues
- Yellow: Minor issues, being managed
- Red: Significant issues, needs escalation

TASK:
Based on the customer information and the progress we've made (assume we're in Week 2 of implementation), create a status update that includes:

1. Overall status (Green/Yellow/Red)
2. Key accomplishments this week
3. Activities planned for next week
4. Issues and risks (with status)
5. Customer engagement/responsiveness
6. Go-live confidence level

OUTPUT FORMAT:
Executive summary format - one page maximum. Use bullet points for easy scanning. Lead with the bottom line.

---

Customer: Sunrise Furniture Co.
Implementation Start: January 20, 2025
Target Go-Live: March 1, 2025
Current Week: 2 of 5

Week 2 Progress (assume these are done):
- Kick-off meeting completed
- Credit approved
- Item master received (but not yet loaded)
- EDI mapping started (about 40% complete)
- Facility space allocated

Week 2 Issues:
- Customer hasn't provided W-9 yet
- Their IT contact was out sick, slowing EDI work

[PASTE CUSTOMER INFORMATION SHEET FOR ADDITIONAL CONTEXT]
```

---

## Prompt 7: SOP Generator for Customer-Specific Procedures

```
ROLE:
You are an operations manager creating a customer-specific Standard Operating Procedure (SOP) for your warehouse team.

CONTEXT:
Each customer may have unique requirements beyond our standard processes. These need to be documented so the warehouse team handles their freight correctly.

This SOP will be used by:
- Receiving team
- Inventory team
- Pick/pack team
- Shipping team

TASK:
Based on the customer information provided, create a customer-specific SOP that documents:

1. RECEIVING
   - How their product arrives (carriers, container vs palletized)
   - Special inspection requirements
   - Put-away rules

2. STORAGE
   - Storage requirements (location, conditions)
   - Handling restrictions
   - Inventory rules (FIFO, lot tracking, etc.)

3. FULFILLMENT
   - Order types they send
   - Pick/pack requirements
   - Assembly/value-added services
   - Quality checks before shipping

4. SHIPPING
   - Preferred carriers
   - Label requirements
   - Documentation needs
   - Delivery appointment requirements

5. SPECIAL INSTRUCTIONS
   - Anything unique to this customer
   - Do's and Don'ts

OUTPUT FORMAT:
SOP format suitable for printing and posting in the warehouse. Use clear headers, numbered steps, and bullet points. Include any warnings or critical notes in bold.

---

[PASTE CUSTOMER INFORMATION SHEET HERE]
```
