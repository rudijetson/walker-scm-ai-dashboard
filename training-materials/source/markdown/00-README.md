# Mock Assets for AI Training Session

## Overview

These files are realistic mock data for Walker Logistics to use in tomorrow's hands-on AI training session. All company names, contacts, and data are fictional.

---

## File List

| File | Type | Purpose |
|------|------|---------|
| 01-sample-rfp.md | Markdown | Full RFP to practice extraction prompts |
| 02-walker-rate-sheet.tsv | TSV/Excel | Rate lookup reference data |
| 03-quote-template.md | Markdown | Quote document structure |
| 04-sample-rate-requests.md | Markdown | 7 email scenarios for rate quotes |
| 05-new-customer-info-sheet.md | Markdown | Customer onboarding data |
| 06-building-file-checklist.md | Markdown | Full onboarding process checklist |
| 07-scenario-cards.md | Markdown | 8 email writing scenarios |
| 08-messy-process-description.md | Markdown | Raw process description for mapping |
| 09-ar-aging-report.tsv | TSV/Excel | Accounts receivable data |
| 10-monthly-revenue-summary.tsv | TSV/Excel | Financial summary data |

---

## How to Use Each File

### For RFP/Quote Workflow (Hour 1)

**Primary files:**
- `01-sample-rfp.md` — Paste this into ChatGPT/Claude to practice RFP extraction
- `02-walker-rate-sheet.tsv` — Reference for building quotes
- `03-quote-template.md` — Show what the final output should look like

**Exercise flow:**
1. Show the RFP
2. Build a prompt to extract key requirements
3. Test across models
4. Show how extracted info maps to quote template

---

### For Rate Lookup Workflow

**Primary files:**
- `04-sample-rate-requests.md` — 7 realistic rate request emails
- `02-walker-rate-sheet.tsv` — Internal rate reference

**Exercise flow:**
1. Pick a rate request email
2. Build a prompt to parse the request and recommend rates
3. Test with internal rates vs. web search for market rates
4. Compare ChatGPT vs. Perplexity for current rate data

**Note:** Request #6 is intentionally vague/incomplete — good for showing how AI can identify missing information.

---

### For Customer Onboarding / Building File

**Primary files:**
- `05-new-customer-info-sheet.md` — Sample customer data
- `06-building-file-checklist.md` — Full process checklist

**Exercise flow:**
1. Show the customer info sheet
2. Build a prompt to generate onboarding tasks
3. Use the checklist to show how AI can track status
4. Practice generating customer communications

---

### For Process Mapping / Mermaid Demo

**Primary file:**
- `08-messy-process-description.md` — Raw, unstructured process description

**Exercise flow:**
1. Show the messy description (read a section aloud)
2. Paste into Claude/ChatGPT with prompt: "Create a Mermaid flowchart for this process"
3. Show the instant visualization
4. Discuss how to identify AI integration points on the map

---

### For Customer Communications

**Primary file:**
- `07-scenario-cards.md` — 8 different email scenarios

**Scenarios included:**
- A: Shipment delay notification
- B: Quote follow-up
- C: Damage claim response
- D: Service issue apology (our fault)
- E: Contract renewal outreach
- F: Price increase notification
- G: Win-back attempt (lost customer)
- H: Thank you / relationship building

**Exercise flow:**
1. Pick a scenario
2. Build prompt with role, context, task, format
3. Generate email draft
4. Discuss what to verify/personalize before sending

---

### For Financial / Cash Flow

**Primary files:**
- `09-ar-aging-report.tsv` — Detailed AR data
- `10-monthly-revenue-summary.tsv` — Revenue and cash flow data

**Exercise flow:**
1. Show the data
2. Practice prompts for:
   - Summarizing AR status
   - Identifying collection priorities
   - Drafting collection emails
   - Analyzing revenue trends
   - Generating executive summaries

---

## TSV Files — How to Use

The `.tsv` files can be:

1. **Opened directly in Excel** — File > Open > Select the .tsv file
2. **Copy/pasted into Excel** — Open in text editor, select all, paste into Excel
3. **Pasted into AI tools** — Works directly in ChatGPT, Claude, etc.

TSV (Tab-Separated Values) maintains column structure when pasted.

---

## Tips for the Session

1. **Start simple** — Use the RFP extraction first, it's the clearest demo
2. **Let them pick** — Ask which scenario interests them most
3. **Show iteration** — Run a prompt, show the output, ask "what would we change?", run again
4. **Compare models** — Same prompt in ChatGPT vs Claude shows different strengths
5. **Connect to their work** — "Where do you see this in your daily job?"

---

## Customization

Feel free to modify these files to better match Walker's actual:
- Service offerings
- Locations
- Customer types
- Rate structures
- Internal processes

The more realistic, the more valuable the training.
