# RFP Analysis Prompts

Use these prompts with the sample RFP (01-sample-rfp.md)

---

## Prompt 1: Basic RFP Extraction

```
ROLE: 
You are a logistics sales analyst at Walker Logistics, a company that provides warehousing, transportation, and supply chain services.

CONTEXT:
Walker Logistics operates distribution centers in Atlanta, Chicago, Dallas, and Los Angeles. Our services include:
- Warehousing (storage, pick/pack, inventory management)
- Transportation (FTL, LTL, expedited)
- Value-added services (kitting, labeling, light assembly, returns)

I've received an RFP from a potential customer and need to quickly understand what they're asking for.

TASK:
Analyze the attached RFP and extract the following information:
1. Customer company name and primary contact
2. Services requested (warehousing, transportation, or both)
3. Locations/geography involved
4. Volume estimates (storage, inbound, outbound)
5. Special requirements or unique needs
6. Technology/integration requirements
7. Timeline and key dates
8. Evaluation criteria (what matters most to them)
9. Contract terms they're requesting
10. Any red flags or concerns
11. Questions we should ask before quoting

OUTPUT FORMAT:
Present this as a structured summary that I can review in under 3 minutes. Use bullet points. Put the most critical information first. If any information is missing or unclear, note it as "NOT SPECIFIED - need to clarify."

---

[PASTE RFP HERE]
```

---

## Prompt 2: RFP Fit Assessment

```
ROLE:
You are a senior sales manager at Walker Logistics evaluating whether an RFP is a good fit for our capabilities.

CONTEXT:
Walker Logistics capabilities:
- Locations: Atlanta (150K sq ft, 85% utilized), Chicago (200K sq ft, 87% utilized), Dallas (120K sq ft, 68% utilized), Los Angeles (80K sq ft, 91% utilized)
- Services: Warehousing, pick/pack, transportation management, kitting, light assembly, returns processing
- Technology: WMS with EDI capability (940, 945, 856, 810), customer portal, API available
- Ideal customer profile: $20K-$150K monthly revenue, retail or manufacturing, Midwest or Southeast focus
- We do NOT handle: Hazmat, frozen/refrigerated, firearms, pharmaceuticals

TASK:
Review this RFP and provide a fit assessment:
1. Overall fit score (1-10) with explanation
2. Which Walker location would best serve this customer?
3. Do we have capacity for their volume?
4. Can we meet their technology requirements?
5. Are there any services they need that we don't offer?
6. What are the top 3 reasons to pursue this opportunity?
7. What are the top 3 risks or concerns?
8. Recommendation: Pursue, Pursue with Caveats, or Decline

OUTPUT FORMAT:
Executive summary format - start with the recommendation and fit score, then provide supporting details. Keep it to one page equivalent.

---

[PASTE RFP HERE]
```

---

## Prompt 3: Generate Clarifying Questions

```
ROLE:
You are preparing for a discovery call with a prospect who sent an RFP.

CONTEXT:
We've received an RFP and reviewed it, but before we invest time building a detailed quote, we need to clarify several points. The discovery call is scheduled for 30 minutes.

TASK:
Based on this RFP, generate a list of clarifying questions organized by category:
1. Volume & Growth - questions about their projections and accuracy
2. Operations - questions about their current process and pain points
3. Technology - questions about integration complexity
4. Timeline - questions about their decision process
5. Competition - tactful questions about who else they're considering
6. Deal Breakers - questions to uncover any non-negotiables

For each question, note WHY we're asking (what will the answer tell us).

OUTPUT FORMAT:
Numbered list organized by category. Include 3-5 questions per category. Add a "priority" flag to the 5 most important questions we must ask.

---

[PASTE RFP HERE]
```

---

## Prompt 4: Scope of Work Draft

```
ROLE:
You are a logistics sales professional drafting the scope of work section for a customer proposal.

CONTEXT:
Walker Logistics has reviewed the customer's RFP and determined we can meet their requirements. Our proposed solution:
- Facility: Walker Chicago Distribution Center (200K sq ft, 24' clear height, 12 dock doors)
- We will provide warehousing, pick/pack, and outbound transportation coordination
- Standard hours: Monday-Friday 6am-6pm, Saturday available during peak

I need to draft the scope of work section that clearly describes what we will and won't do.

TASK:
Based on the RFP requirements, draft a comprehensive Scope of Work that includes:
1. Facility description and specifications
2. Receiving services (what's included, turnaround commitments)
3. Storage services (types, conditions, inventory management)
4. Outbound services (order fulfillment, shipping, carrier coordination)
5. Value-added services (if applicable)
6. Technology and reporting
7. Hours of operation
8. Exclusions (what is NOT included)
9. Customer responsibilities

OUTPUT FORMAT:
Professional proposal language, written in complete sentences. Use headers for each section. Be specific about commitments (e.g., "within 24 hours" not "quickly"). Approximately 2 pages.

---

[PASTE RFP HERE]
```

---

## Prompt 5: Competitive Positioning

```
ROLE:
You are a sales strategist helping position Walker Logistics against competitors for this opportunity.

CONTEXT:
The prospect mentioned they are also talking to XPO Logistics and Kenco. 

General competitive landscape:
- XPO: Larger national footprint, strong technology, but can be impersonal and slow to respond. Higher pricing.
- Kenco: Good regional player, competitive pricing, but technology is dated. Strong in manufacturing sector.
- Walker (us): Mid-size, responsive, strong customer service, good technology, competitive pricing. Known for flexibility and partnership approach.

TASK:
Based on this RFP and what the customer seems to value, develop a competitive positioning strategy:
1. What does this customer seem to value most? (based on their evaluation criteria and language)
2. Where does Walker have an advantage over XPO for this customer?
3. Where does Walker have an advantage over Kenco for this customer?
4. What objections might they have about Walker? How do we address them?
5. What proof points or references should we highlight?
6. Suggested key messages for our proposal and presentations

OUTPUT FORMAT:
Strategic brief format. Concise bullet points with specific, actionable recommendations.

---

[PASTE RFP HERE]
```
