# Process Mapping & Mermaid Prompts

Use these prompts with the messy process description (08-messy-process-description.md)

---

## Prompt 1: Basic Process Flowchart

```
ROLE:
You are a business process analyst helping document a sales workflow.

CONTEXT:
I have several descriptions of our quote process from different team members. The descriptions are informal and somewhat inconsistent, but together they paint a picture of how things actually work.

TASK:
Based on the process descriptions below, create a Mermaid flowchart diagram that shows:
1. The main steps in the process from RFP receipt to quote sent
2. Decision points (where the process branches)
3. The general sequence and flow
4. Any loops or iterations

OUTPUT FORMAT:
Valid Mermaid code that I can paste into a Mermaid renderer. Use the flowchart TD (top-down) format. Include clear node labels.

---

[PASTE MESSY PROCESS DESCRIPTION HERE]
```

---

## Prompt 2: Process Map with Pain Points Highlighted

```
ROLE:
You are a process improvement consultant analyzing a workflow for optimization opportunities.

CONTEXT:
I have descriptions of our current quote process from the sales team. The process has several known pain points that slow things down or cause errors.

TASK:
Create a Mermaid flowchart that:
1. Maps the current state process
2. Highlights pain points in RED
3. Highlights waiting/delay points in YELLOW
4. Shows where handoffs occur between people/systems
5. Includes time estimates where mentioned

OUTPUT FORMAT:
Mermaid code with styling to color-code problem areas. Add a legend at the bottom.

Example of styling to use:
```
style NodeName fill:#ff6b6b
style WaitNode fill:#ffd93d
```

---

[PASTE MESSY PROCESS DESCRIPTION HERE]
```

---

## Prompt 3: Identify AI Integration Points

```
ROLE:
You are an AI implementation consultant analyzing a business process for automation opportunities.

CONTEXT:
I have a description of our current quote process. We want to identify where AI/automation could help without replacing human judgment where it's needed.

Good candidates for AI assistance:
- Repetitive tasks done the same way each time
- Information extraction from documents
- First drafts that humans then review
- Data lookups across multiple sources
- Calculations and comparisons

Not good candidates for AI (keep human):
- Relationship decisions
- Complex negotiations
- Exception handling requiring judgment
- Final approval on significant deals

TASK:
1. Analyze the process description
2. Create a Mermaid flowchart of the current process
3. Add comments indicating where AI could help
4. For each AI opportunity, note:
   - What the AI would do
   - What the human still does
   - Estimated time savings

OUTPUT FORMAT:
Mermaid flowchart code, followed by a table of AI integration opportunities with details.

---

[PASTE MESSY PROCESS DESCRIPTION HERE]
```

---

## Prompt 4: Current State vs Future State

```
ROLE:
You are a business transformation consultant creating process documentation.

CONTEXT:
I have a description of our current quote process. We want to visualize:
1. How it works today (current state)
2. How it could work with AI assistance (future state)

TASK:
Create TWO Mermaid flowcharts:

CHART 1 - Current State:
- Show the process as it exists today
- Include manual steps
- Show wait times and delays
- Highlight inefficiencies

CHART 2 - Future State:
- Show the optimized process with AI integration
- Use different colors for AI-assisted steps vs human steps
- Show reduced wait times
- Include notes on what changed

OUTPUT FORMAT:
Two separate Mermaid code blocks, clearly labeled. Add a comparison summary showing:
- Estimated current process time: X hours
- Estimated future process time: Y hours
- Time savings: Z%

---

[PASTE MESSY PROCESS DESCRIPTION HERE]
```

---

## Prompt 5: Swimlane Diagram (Who Does What)

```
ROLE:
You are a business analyst creating a swimlane process diagram to clarify roles and responsibilities.

CONTEXT:
Our quote process involves multiple people:
- Sales Rep (does most of the work)
- Sales Manager (approves large deals)
- Operations Team (checks capacity)
- Customer (provides information, makes decisions)

The current process has unclear handoffs and people aren't sure who's responsible for what.

TASK:
Create a Mermaid swimlane diagram that shows:
1. Each role as a separate lane
2. Which tasks belong to which role
3. Where handoffs occur between roles
4. Where bottlenecks happen (waiting for someone else)

OUTPUT FORMAT:
Mermaid code using the subgraph feature to create swimlanes. Example structure:

```
flowchart LR
    subgraph Sales Rep
        A[Task 1]
        B[Task 2]
    end
    subgraph Sales Manager
        C[Approval]
    end
    A --> B --> C
```

---

[PASTE MESSY PROCESS DESCRIPTION HERE]
```

---

## Prompt 6: Process Documentation Generator

```
ROLE:
You are a technical writer creating formal process documentation from informal descriptions.

CONTEXT:
I have informal descriptions of our quote process from team interviews. I need to turn this into professional documentation suitable for:
- New employee training
- ISO compliance
- Process improvement baseline

TASK:
Based on the descriptions provided, create:

1. PROCESS OVERVIEW
   - Purpose of the process
   - Scope (start and end points)
   - Key stakeholders

2. PROCESS STEPS
   - Numbered steps with clear descriptions
   - Inputs and outputs for each step
   - Responsible party for each step
   - Estimated time for each step

3. DECISION POINTS
   - List each decision point
   - Criteria for each decision
   - Outcomes/branches

4. SYSTEMS AND TOOLS
   - What systems are used
   - What documents/templates are needed

5. METRICS
   - How we measure success
   - Current performance (if mentioned)

6. KNOWN ISSUES
   - Pain points from the descriptions
   - Improvement opportunities

OUTPUT FORMAT:
Professional documentation format with headers and sections. Write in third person, present tense ("The sales rep reviews..."). Include a process summary flowchart in Mermaid at the end.

---

[PASTE MESSY PROCESS DESCRIPTION HERE]
```

---

## Quick Mermaid Demo Prompts

### Simple Flowchart
```
Create a Mermaid flowchart for this process: Customer submits order, warehouse picks items, warehouse packs items, shipping creates label, carrier picks up, customer receives delivery.
```

### Decision Tree
```
Create a Mermaid flowchart showing: If order value is over $10,000 then manager approval is required, otherwise auto-approve. If approved, process order. If rejected, notify customer.
```

### Sequence Diagram
```
Create a Mermaid sequence diagram showing the interaction between: Customer, Sales Rep, WMS System, and Carrier. Customer places order, sales rep enters in WMS, WMS sends to carrier, carrier confirms pickup, WMS notifies customer.
```
