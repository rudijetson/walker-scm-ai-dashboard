# Rate Lookup Prompts

Use these prompts with the sample rate requests (04-sample-rate-requests.md)

---

## Master Rate Lookup Prompt (Adapt for Any Request)

```
ROLE:
You are a freight rate analyst at Walker Logistics helping the sales team respond to rate requests quickly and accurately.

CONTEXT:
Walker Logistics provides warehousing and transportation services. For transportation, we work with a network of carriers and can provide LTL, FTL, and expedited options.

Current fuel surcharge: approximately 28% on linehaul
General market conditions: Capacity is moderate, spot rates are stable

TASK:
Analyze this rate request and provide:
1. Summary of what the customer is asking for
2. Key shipment details (origin, destination, weight, class, requirements)
3. Any missing information we need to quote accurately
4. Recommended service type (LTL, FTL, expedited, etc.)
5. Estimated rate range (if you can search current market rates)
6. Transit time estimate
7. Any special considerations or flags
8. Draft response email to the customer

OUTPUT FORMAT:
Structured analysis first, then the draft email. Keep the email professional but friendly, under 150 words.

---

[PASTE RATE REQUEST EMAIL HERE]
```

---

## Rate Request #1: Simple LTL (Atlanta to Nashville)

```
ROLE:
You are a freight rate analyst at Walker Logistics.

CONTEXT:
Customer request: 2 pallets, 1,400 lbs total, Class 85, Atlanta (30301) to Nashville (37201), needs delivery by Friday (ships tomorrow or Wednesday).

Walker's LTL carrier partners and approximate rates for this lane:
- Estes Express: $285-320, 2-day transit, reliable
- ABF Freight: $265-295, 2-day transit, good for heavy freight
- XPO LTL: $310-350, 1-2 day transit, premium service

Standard fuel surcharge: 28%

TASK:
1. Confirm this is a straightforward LTL shipment
2. Calculate estimated all-in rates for each carrier option
3. Recommend the best option given their Friday deadline
4. Draft a quick response email with the quote

OUTPUT FORMAT:
Brief analysis (5-6 lines) followed by a short, professional email response with the rate quote. Include transit time and any assumptions.

---

FROM: Mike Davidson <mdavidson@acmemfg.com>
SUBJECT: Quick rate check - Atlanta to Nashville

Hey,

Need a quick rate for a customer shipment.

2 pallets, about 1,400 lbs total. Class 85. Standard stuff - no special handling.

Going from our Atlanta plant (30301) to a customer in Nashville (37201).

Customer needs it there by Friday - so probably needs to ship tomorrow or Wednesday at the latest.

What can you do?

Mike Davidson
Acme Manufacturing
```

---

## Rate Request #2: FTL Weekly Lane (Dallas to Phoenix)

```
ROLE:
You are a freight rate analyst at Walker Logistics quoting a recurring FTL lane.

CONTEXT:
Customer wants a weekly dedicated lane: Dallas to Phoenix, full truckload, dry van, every Tuesday.

Market reference rates for Dallas to Phoenix FTL:
- Spot market: $1,800-2,200
- Contract/dedicated rates: $1,650-1,900 (committed weekly volume)
- Transit: 2 days typical
- Current capacity: Moderate - Texas outbound is balanced

For committed weekly lanes, we typically offer 10-15% below spot rates.

TASK:
1. Analyze the request and confirm requirements
2. Calculate a competitive contract rate for weekly commitment
3. Note any capacity concerns or considerations
4. Address their question about Texas outbound capacity
5. Draft a professional response with the quote

OUTPUT FORMAT:
Analysis section, then a professional email response. Since this is a committed lane, emphasize the value of consistency and our reliability.

---

FROM: Sandra Lopez <s.lopez@sunrisefoods.com>
SUBJECT: FTL Quote Request - Dallas to Phoenix (weekly)

Hi Walker team,

We're looking for a carrier partner for a new weekly lane and wanted to get your rates.

Details:
- Origin: Dallas, TX 75201 (our DC - dock hours 6am-4pm)
- Destination: Phoenix, AZ 85001 (customer DC - appointment required)
- Frequency: Once per week, every Tuesday pickup
- Equipment: Dry van, 53'
- Weight: Approximately 38,000 lbs (full truck, palletized)
- Commodity: Packaged food products (not temp controlled)

We need delivery within 3 days of pickup. No weekend delivery needed.

This would be an ongoing weekly shipment. Can you provide your best rate for a committed lane?

Also - do you have any capacity concerns for Texas outbound right now? We've been hearing things are tight.

Thanks,

Sandra Lopez
Logistics Coordinator
Sunrise Foods Inc.
(469) 555-2847
```

---

## Rate Request #3: LTL with Special Requirements (Liftgate)

```
ROLE:
You are a freight rate analyst handling a shipment with accessorial requirements.

CONTEXT:
Customer needs LTL from Los Angeles to Seattle with liftgate delivery. Location has no dock.

Base LTL rates LA to Seattle (before accessorials):
- 6 pallets, 4,800 lbs, Class 92.5: approximately $850-1,100

Accessorial charges (typical):
- Liftgate delivery: $75-95
- Limited access delivery: $65-85
- Notify/appointment: $15-25

Transit time: 3-4 business days typically

TASK:
1. Confirm shipment details and accessorial needs
2. Calculate all-in rate including accessorials
3. Note that "commercial but no dock" may trigger limited access fees
4. Provide transit time estimate for Monday ship date
5. Draft response email with complete quote

OUTPUT FORMAT:
Break down the quote showing base rate + each accessorial so customer understands the components. Professional email format.

---

FROM: Tom Bradley <tbradley@eliteretail.com>
SUBJECT: LTL rate needed - liftgate + residential

Hi,

I need a rate for a delivery to one of our franchise locations. It's a strip mall location with no dock, so we'll need liftgate service.

Shipment info:
- 6 pallets, 4,800 lbs total
- 48x40 pallets, about 48" high each
- Class 92.5
- Picking up from: Los Angeles, CA 90001
- Delivering to: Seattle, WA 98101

The delivery address is technically commercial (it's a retail store) but there's no dock and limited space. Driver will need to set pallets at the back door.

Customer is asking when they can expect delivery if we ship this Monday.

Let me know,

Tom Bradley
Elite Retail Solutions
```

---

## Rate Request #4: Expedited / Hot Shipment

```
ROLE:
You are a freight rate analyst handling an urgent, time-critical shipment with high-value cargo.

CONTEXT:
Emergency shipment: Customer production line down, needs parts ASAP. Atlanta to Chicago, 1 pallet, 850 lbs, $45,000 value.

Expedited options Atlanta to Chicago:
- Next-day air freight: $1,200-1,500 (delivery by noon next day)
- Expedited ground (team drivers): $950-1,100 (delivery in 14-16 hours)
- Hot shot/sprinter van: $800-950 (delivery in 12-14 hours)
- Standard LTL expedited: $450-550 (next day by EOD, not guaranteed)

For high-value cargo ($45K), recommend:
- Declared value coverage at $0.50 per $100 = $225
- Or customer's cargo insurance

TASK:
1. Acknowledge urgency immediately
2. Present multiple options with clear trade-offs
3. Include transit times AND delivery windows
4. Address the high-value nature and insurance
5. Give a clear recommendation
6. Respond FAST - they said within the hour

OUTPUT FORMAT:
Options table format for easy comparison, followed by your recommendation. Keep email concise but complete - they need to make a quick decision.

---

FROM: Rachel Kim <rkim@techparts.com>
SUBJECT: URGENT - need expedited rate ASAP

We have an emergency shipment and need options fast.

Customer production line is down waiting for these parts. They're in Chicago and we're in Atlanta.

What we're shipping:
- 1 pallet
- 850 lbs
- Dims: 48x40x36
- High value electronics components (about $45,000 value)

Need to know:
1. Fastest option and cost (even if it's expensive)
2. Next-day air freight option?
3. Expedited ground - what's the transit?
4. Do you have a truck heading that way we could get space on?

Customer will pay premium for speed. What are our options and costs for each?

Need an answer within the hour if possible.

Rachel Kim
TechParts Distribution
Cell: (404) 555-9182
```

---

## Rate Request #5: Multi-Stop FTL

```
ROLE:
You are a freight rate analyst quoting a complex multi-stop truckload shipment.

CONTEXT:
Multi-stop FTL from Chicago with 4 delivery stops: Indianapolis, Louisville, Nashville, Atlanta.

Pricing approach for multi-stop:
- Base linehaul (Chicago to Atlanta through route): ~$1,400-1,600
- Stop charges: $75-100 per stop
- Waiting time risk: Each stop adds potential detention
- Total mileage: approximately 720 miles

Alternative: Break into separate LTL shipments
- Indianapolis (8 pallets): ~$320-380
- Louisville (10 pallets): ~$380-450
- Nashville (6 pallets): ~$350-420
- Atlanta (8 pallets): ~$480-560
- Total LTL: ~$1,530-1,810

TASK:
1. Analyze the routing and stop sequence
2. Quote the multi-stop FTL option
3. Calculate the LTL alternative for comparison
4. Make a recommendation based on cost and complexity
5. Note delivery timeline for each approach
6. Address their question about which makes more sense

OUTPUT FORMAT:
Side-by-side comparison of the two approaches, then a clear recommendation with reasoning. Professional email format.

---

FROM: James Wright <jwright@nationwide.com>
SUBJECT: Multi-stop FTL quote - 4 drops

Hi,

Looking for a rate on a multi-stop full truckload.

Route:
- Pickup: Chicago, IL 60601 (our main DC)
- Stop 1: Indianapolis, IN 46201 - drop 8 pallets
- Stop 2: Louisville, KY 40201 - drop 10 pallets
- Stop 3: Nashville, TN 37201 - drop 6 pallets
- Stop 4: Atlanta, GA 30301 - drop 8 pallets (final)

Details:
- Total: 32 pallets, approximately 28,000 lbs
- Dry van
- All stops are commercial with docks
- Would ship Monday, need all deliveries completed by Thursday EOD

What's the rate? Also, is it cheaper to do this as one multi-stop or break it into separate LTL shipments? I'm open to whatever makes more sense cost-wise.

Thanks,

James Wright
Distribution Manager
Nationwide Supply Co.
```

---

## Rate Request #6: Vague/Incomplete Request

```
ROLE:
You are a freight rate analyst who needs to gather more information before quoting.

CONTEXT:
This request is missing critical details needed to provide an accurate quote. We need to ask clarifying questions professionally without making the customer feel bad.

Missing information typically needed:
- Exact addresses (origin and destination)
- Accurate weight and dimensions
- Freight class or commodity description
- Delivery timeline/urgency
- Any special requirements

TASK:
1. Identify what information is missing
2. Make reasonable assumptions where possible (but note them)
3. Provide a ballpark range with heavy caveats
4. Draft a friendly response asking for the details needed
5. Make it easy for them to respond (specific questions, not open-ended)

OUTPUT FORMAT:
List of missing info first, then a friendly email that acknowledges their request, provides a rough estimate if possible, and asks specific questions to finalize the quote.

---

FROM: Chris Taylor <ctaylor@smallbiz.com>
SUBJECT: shipping quote

Hi,

I need to ship some stuff from our warehouse to a customer.

It's about 10 boxes, maybe 500 pounds total? Not really sure on the exact dims but they're not huge. Regular cardboard boxes.

Going from somewhere in Texas to somewhere in Florida. I can get you the exact addresses if you need them.

How much would that cost and how long does it take?

Chris
```

---

## Rate Request #7: International / Cross-Border

```
ROLE:
You are a freight rate analyst handling a cross-border Mexico to US shipment.

CONTEXT:
Cross-border freight from Monterrey, Mexico to Chicago. This involves:
- Mexican domestic transport to border
- Border crossing and customs clearance
- US domestic transport to destination

Typical costs Monterrey to Chicago (door-to-door):
- Freight: $2,200-2,800 (depending on carrier and service)
- Customs brokerage: $150-250
- Border crossing fees: $75-125
- Total: $2,425-3,175

Transit time: 4-6 business days typically
Documents needed: Commercial invoice, packing list, USMCA certificate (if claiming duty-free), bill of lading

TASK:
1. Confirm this is within our service capability
2. Provide door-to-door rate estimate
3. Explain what's included (and what's not)
4. Answer their questions about customs brokerage
5. List required documents
6. Mention the monthly volume opportunity for contract pricing

OUTPUT FORMAT:
Comprehensive response covering all their questions. Professional tone appropriate for a potential ongoing customer.

---

FROM: Maria Santos <msantos@globalimports.com>
SUBJECT: Cross-border rate - Mexico to Chicago

Hello,

We need a rate for cross-border freight from Mexico.

Details:
- Origin: Monterrey, Mexico (supplier's facility)
- Destination: Chicago, IL 60601 (our warehouse)
- Freight: 12 pallets, 16,000 lbs
- Commodity: Auto parts (HS code 8708.99)
- Value: $85,000 USD

Questions:
1. What's your door-to-door rate including customs clearance?
2. Do you handle the customs brokerage or do we need our own broker?
3. What's typical transit time?
4. What documents do we need to provide?

We do this shipment monthly and would consider a contract rate if the pricing is competitive.

Thanks,

Maria Santos
Global Imports LLC
```
