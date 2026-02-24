# Finance: AI-Assisted Financial Operations

## Section 1: Why AI Matters for Finance

The finance function is undergoing a significant shift. According to the Deloitte CFO Survey 2024, **58% of finance teams** now use AI or machine learning tools in some capacity — from automating close narratives to accelerating variance analysis. This isn't a future trend; it's the current operating environment.

The efficiency gains are measurable:

- **Monthly close narratives**: reduced from ~4 hours to ~45 minutes of drafting and review time
- **Variance analysis preparation**: reduced from ~2 hours to ~20 minutes for standard budget-vs-actual explanations
- **Audit documentation**: first drafts of control descriptions and process narratives generated in minutes rather than hours

### What AI CAN Do

- Draft financial narratives (MD&A sections, board memos, close commentary)
- Generate variance explanations from structured data points you provide
- Prepare audit documentation — control descriptions, process narratives, testing plan frameworks
- Build and iterate on forecasting model structures and assumption narratives
- Summarize lengthy financial reports, earnings calls, and regulatory filings
- Assist with vendor due diligence by structuring evaluation criteria and comparison frameworks

### What AI CANNOT Do

- **Replace professional judgment** on accounting treatments, revenue recognition, or classification decisions
- **Make investment decisions** — AI has no fiduciary duty and no understanding of your risk appetite
- **Guarantee regulatory compliance** — SOX, IFRS, and GAAP requirements demand human accountability
- **Audit itself** — AI cannot validate its own output; independent verification is always required
- **Understand company-specific context** without explicit guidance — your chart of accounts, intercompany structures, and materiality thresholds are unknown to it

The bottom line: AI is a drafting and preparation tool. It accelerates the work that precedes professional judgment — it does not replace it.

---

## Section 2: Core AI Tools

### General AI Assistants

| Tool | Best For | Key Strength |
|------|----------|-------------|
| **ChatGPT** | Quick variance explanations, memo drafts, brainstorming financial model structures | Fast iteration, good at structured output formats |
| **Claude** | Long-form financial analysis (annual reports, audit prep documents), detailed memo drafting, complex data interpretation | Handles large documents well, strong at nuanced writing and maintaining consistency across lengthy outputs |
| **Gemini** | Market research with web access, industry benchmarking, regulatory update summaries | Real-time web access for current market data and regulatory changes |

### Microsoft Copilot for M365

Copilot is embedded directly in your existing Microsoft tools, which makes it the most accessible option for day-to-day finance work.

- **Word**: Draft financial narratives, board memos, audit reports, and policy documents. Copilot can restructure existing content, adjust tone for different audiences (board vs. management vs. external auditors), and generate first drafts from bullet-point inputs.

- **Excel**: Formula assistance, pivot table suggestions, data analysis, and financial modeling support. **Important caveat**: Copilot in Excel works best for analysis, formatting, and suggesting approaches. **Always verify calculations independently.** Do not rely on Copilot-generated formulas without tracing the logic yourself — an incorrect SUMIF or misaligned range can cascade through an entire model.

- **PowerPoint**: Board presentations, investor decks, budget review slides. Copilot can generate slide structures from Word documents or outlines, apply consistent formatting, and suggest data visualizations.

- **Outlook**: Draft vendor communications, manage audit request responses, and compose stakeholder updates. Useful for maintaining professional tone across high-volume correspondence during close or audit periods.

- **Teams**: Finance meeting recaps, budget review summaries, and action item tracking. Meeting transcription and summary features reduce the documentation burden on the finance team during review cycles.

---

## Section 3: Practical Applications

### Use Case 1: Financial Report Narratives

**Scenario**: You're preparing the Management Discussion & Analysis (MD&A) section for Q3 results. You have the numbers — revenue, EBITDA, key line items — but need to draft the narrative that explains performance to stakeholders.

**Example Prompt**:

```
Draft the revenue and profitability section of our Q3 Management Discussion & Analysis.
Use a professional, conservative tone appropriate for board-level reporting.

Key metrics:
- Q3 Revenue: $42.3M (vs Q3 prior year: $38.1M, vs budget: $43.0M)
- Gross margin: 62.4% (vs prior year: 64.1%, vs budget: 63.5%)
- EBITDA: $8.7M (vs prior year: $7.9M, vs budget: $9.2M)
- Operating expenses: $17.6M (vs prior year: $16.5M, vs budget: $17.0M)

Business context:
- New enterprise product launched in August — contributed $1.8M in revenue but carried
  higher implementation costs that compressed margins
- Two large client renewals slipped to Q4 (combined $1.2M ARR)
- Headcount increased by 12 FTEs in engineering (planned)

Structure: start with a revenue overview, then profitability, then forward-looking context.
Do not fabricate any numbers beyond what I've provided.
```

**What the AI output looks like**: A 3–4 paragraph narrative covering revenue growth (11% YoY), the budget shortfall driven by renewal timing, margin compression from the product launch, EBITDA improvement despite cost pressures, and a forward-looking note on the Q4 pipeline. The tone is measured and factual.

**Tips for better results**:
- Always provide the specific numbers — AI cannot look up your actuals
- Include business context for variances; without it, the narrative will be generic
- Specify the audience (board, investors, internal management) to calibrate the tone
- State explicitly: "Do not fabricate numbers" — this prevents the model from inventing supporting figures

---

### Use Case 2: Variance Analysis

**Scenario**: You're preparing budget-vs-actual variance explanations for the monthly board package. You have 8 line items with material variances that need clear, concise commentary.

**Example Prompt**:

```
Generate variance explanations for the following budget-vs-actual results (October 2025).
Format each as 2-3 sentences suitable for a board-level variance report.
Use a professional tone. Classify each variance as favorable or unfavorable.

Line items with material variances (>5% or >$50K):

1. Professional Services Revenue: Actual $3.2M vs Budget $3.8M (-$600K, -15.8%)
   Context: Two SOWs delayed due to client procurement process; expected to close in November.

2. SaaS Revenue: Actual $5.1M vs Budget $4.9M (+$200K, +4.1%)
   Context: Early renewal of 3 mid-market accounts with price increases.

3. Personnel Costs: Actual $4.8M vs Budget $4.3M (+$500K, +11.6%)
   Context: Hired 6 unbudgeted contractors for SOX remediation project.

4. Travel & Entertainment: Actual $180K vs Budget $95K (+$85K, +89.5%)
   Context: Unbudgeted travel for new client implementations in APAC region.

5. Cloud Infrastructure: Actual $620K vs Budget $550K (+$70K, +12.7%)
   Context: Data migration costs for platform upgrade; one-time in nature.

For each, state: the variance amount, whether favorable or unfavorable,
the root cause, and whether it is recurring or one-time.
```

**What the AI output looks like**: A structured set of variance explanations, each 2–3 sentences, with clear favorable/unfavorable classification, root cause, and recurrence assessment. Ready to drop into a board package with minimal editing.

**Tips for better results**:
- Provide the "why" behind each variance — AI can format and articulate, but only you know the business reasons
- Specify your materiality thresholds so the AI understands what qualifies as significant
- Request a consistent format (favorable/unfavorable, root cause, one-time vs. recurring) to ensure uniformity across the report
- Review every variance explanation against what actually happened — the AI is rephrasing your inputs, not conducting analysis

---

### Use Case 3: Audit Preparation

**Scenario**: External audit fieldwork begins in three weeks. You need to prepare control descriptions and process narratives for the revenue recognition cycle, and your documentation from last year needs updating.

**Example Prompt**:

```
Help me draft audit documentation for our revenue recognition process (ASC 606).
I need three outputs:

1. A process narrative (1-2 pages) describing our order-to-cash cycle:
   - Sales team enters contracts in Salesforce
   - Finance reviews for multi-element arrangements and variable consideration
   - Revenue is recognized at a point in time for product sales, over time for
     professional services (input method based on hours delivered)
   - Monthly reconciliation between Salesforce, billing system (Zuora), and GL (NetSuite)
   - Journal entries prepared by Senior Accountant, reviewed by Controller

2. Control descriptions for 3 key controls:
   - Contract review and approval (threshold: >$100K requires Controller sign-off)
   - Revenue recognition journal entry review (preparer/reviewer segregation)
   - Monthly revenue reconciliation (Salesforce → Zuora → NetSuite)

3. A testing plan outline for each control: what to test, sample size considerations,
   and what constitutes an exception.

Use language consistent with SOX documentation standards.
Do not include any actual revenue figures.
```

**What the AI output looks like**: A structured process narrative covering the order-to-cash flow, three formatted control descriptions with objective/frequency/responsible party/evidence sections, and a testing framework. The output uses standard audit documentation language and SOX-appropriate structure.

**Tips for better results**:
- Describe your actual process accurately — the AI will structure and formalize it, but garbage in means garbage out
- Reference the specific accounting standard (ASC 606, IFRS 15) so the AI frames the narrative correctly
- Explicitly state "Do not include actual revenue figures" to prevent the model from inserting placeholder numbers that could be confused for real data
- Use this as a first draft — your external auditors will have specific formatting and content requirements

---

### Use Case 4: Forecasting Narratives

**Scenario**: It's annual budget season. You've built the financial model, but now you need to write the assumptions and methodology narrative that accompanies the forecast to the board and executive team.

**Example Prompt**:

```
Draft the assumptions and methodology section for our FY2026 annual budget submission.
Tone: professional, suitable for board review. Length: 2-3 pages.

Key forecast drivers and assumptions:
- Revenue growth: 18% YoY, driven by:
  - Existing customer expansion (net revenue retention assumed at 112%)
  - New logo acquisition: 45 new enterprise accounts (vs 38 in FY2025)
  - Price increase of 5% on renewals effective July 2026
- Gross margin: 63% (vs 62.4% in FY2025), improvement from scale efficiencies
  in cloud infrastructure
- Headcount: 285 FTEs by year-end (vs 248 current), 70% of hires in H1
- OpEx growth: 14% YoY, below revenue growth (operating leverage)
- CapEx: $2.1M (platform migration, data center consolidation)
- Working capital: DSO assumed at 52 days (vs 48 current, reflecting enterprise mix shift)

Methodology:
- Bottom-up by business unit for revenue, top-down allocation for shared services
- Monthly phasing based on historical seasonality (Q4 heaviest at ~30% of annual)
- Sensitivity scenarios: base, upside (+3% revenue), downside (-5% revenue, +2% churn)

Structure the narrative with clear sections: Revenue, Profitability, Headcount & OpEx,
Capital Expenditure, Working Capital, and Risk Factors/Sensitivities.
```

**What the AI output looks like**: A well-organized 2–3 page narrative covering each section, articulating the rationale behind key assumptions, connecting forecast drivers to business strategy, and presenting sensitivities in a board-ready format.

**Tips for better results**:
- Be specific about the drivers — "18% growth" is less useful than "18% growth from NRR of 112%, 45 new logos, and a 5% price increase"
- Include the methodology (bottom-up, top-down, hybrid) so the narrative accurately reflects how the budget was built
- Always review the final output to ensure the narrative is consistent with the model — any disconnect between the narrative and the numbers will erode credibility with the board
- AI drafts the words; you own the assumptions. Every number in the forecast narrative should trace back to your model.

---

### Use Case 5: Vendor Evaluation

**Scenario**: You're evaluating three SaaS vendors for a new accounts payable automation tool. You need a structured comparison to present to the CFO and procurement.

**Example Prompt**:

```
Create a vendor evaluation framework for comparing 3 AP automation tools.
Format as a scoring matrix suitable for a CFO presentation.

Vendors under consideration:
1. Tipalti — cloud-native, strong international payments, mid-market focus
2. Coupa — full procure-to-pay suite, enterprise-grade, higher price point
3. Bill.com — SMB/mid-market, simple interface, limited ERP integrations

Our requirements (prioritized):
- Must integrate with NetSuite (our ERP)
- Must support 3-way matching (PO, receipt, invoice)
- Must handle multi-currency (we operate in USD, EUR, GBP)
- Must support approval workflows with configurable thresholds
- SOC 2 Type II compliance required
- Budget: $50K-$120K annually

Evaluation criteria to include:
- Functionality fit (weight: 30%)
- Integration depth with NetSuite (weight: 25%)
- Total cost of ownership over 3 years (weight: 20%)
- Implementation timeline and effort (weight: 15%)
- Vendor stability and support (weight: 10%)

Generate:
1. A weighted scoring matrix (1-5 scale per criterion)
2. A summary recommendation with rationale
3. A list of questions to ask each vendor during demos

Note: Leave actual scores blank for me to fill in — I only want the framework,
not assumptions about vendor capabilities.
```

**What the AI output looks like**: A formatted scoring matrix with weighted criteria, a template for recording vendor responses, a draft recommendation structure, and 10–12 targeted demo questions. Scores are left blank for the team to populate after vendor demos.

**Tips for better results**:
- Be explicit about your non-negotiable requirements vs. nice-to-haves
- Ask the AI for the framework, not the scores — you need to evaluate vendors based on actual demos and reference calls, not AI assumptions
- Include your budget range so the framework can address total cost of ownership appropriately
- Use this as a starting point and customize for your organization's procurement process

---

## Section 4: Responsible AI Use

### Financial Data Is Off-Limits

**This is non-negotiable.** Never paste actual financial statements, revenue figures, margin data, forward-looking projections, or any material non-public information into AI tools. This includes:

- Income statements, balance sheets, or cash flow statements (even partial)
- Revenue by customer, product line, or geography
- EBITDA, net income, or margin figures (actual or projected)
- Guidance, forecasts, or budget numbers
- M&A targets, deal terms, or valuation models
- Compensation data, bonus pools, or equity information

Instead, use **sanitized or illustrative data** when you need AI assistance with financial content. Replace real figures with representative examples, or describe the pattern you need without the actual numbers.

### Accuracy Is Paramount

AI-generated financial figures and calculations must **always** be independently verified. Every number, formula reference, and percentage in AI output should be traced back to source data. This is not optional — errors in financial reporting carry legal consequences under SOX, securities regulations, and professional standards.

Specific verification practices:
- **Cross-check every calculation** the AI produces against your source data
- **Verify formula logic** in any Excel/Copilot suggestions before deploying them in a model
- **Never present AI-generated numbers as audited or verified** without completing your review
- **Flag AI-assisted work** in your workpapers if your organization's audit methodology requires it

### Regulatory Compliance

SOX, IFRS, GAAP, and other regulatory requirements are not negotiable, and AI does not understand your specific compliance obligations. The AI has no knowledge of:

- Your entity structure and consolidation requirements
- Your specific revenue recognition policies and elections
- Control environment requirements and remediation status
- Regulatory filings, deadlines, or disclosure obligations
- Related party relationships and transactions

AI can help draft documentation, but **you** are responsible for ensuring compliance. "The AI generated it" is not a defense in an audit finding or regulatory inquiry.

### Audit Trail

Using AI does not eliminate the need for documentation. Maintain your standard workpaper practices:

- Document when and how AI was used in preparing financial deliverables
- Retain the original AI output alongside your reviewed and finalized version
- Ensure the review and approval chain is clear — someone with appropriate authority must sign off
- If your organization has specific policies on AI use in financial reporting, follow them

### Materiality and Professional Judgment

AI does not understand materiality thresholds, and it cannot make the judgment calls that define financial reporting. Decisions about:

- Whether a variance is material and requires disclosure
- How to classify unusual transactions
- When to escalate accounting treatment questions
- What level of estimation uncertainty to communicate

These remain squarely within the domain of professional judgment. AI can prepare the analysis that informs these decisions — it cannot make them.

### Company Policy

Only use approved AI tools for finance work. Financial data is among the most sensitive information in any organization. No exceptions, no workarounds, no "quick checks" in unapproved tools. If you're unsure whether a tool is approved, check with your manager or IT before using it.

---

## Quiz

**Q1: Which of the following tasks is AI well-suited to assist with in a finance context?**
- A) Making final judgment on revenue recognition treatment for a complex multi-element arrangement
- B) Determining whether a variance is material enough to require board disclosure
- C) Drafting the first version of a quarterly MD&A narrative based on metrics you provide ✓
- D) Independently auditing a set of financial controls for SOX compliance

**Q2: You need to draft variance commentary for a board package. What is the safest approach for using AI?**
- A) Paste the full P&L into ChatGPT and ask it to explain the variances
- B) Provide sanitized or illustrative data points with business context, and draft explanations using AI ✓
- C) Upload the board package to an AI tool for a comprehensive review
- D) Use AI to generate the variance numbers and explanations together to save time

**Q3: AI generates a variance analysis that states: "SaaS revenue was $5.1M, exceeding budget by 4.1%, driven by early renewals." You provided these data points in your prompt. What should you do before including this in your board package?**
- A) Include it as-is since the numbers match what you provided
- B) Verify the numbers match your source data, confirm the percentage calculation is correct, and validate that the explanation accurately reflects the business reason ✓
- C) Run it through a second AI tool for cross-validation
- D) Add a disclaimer that the analysis was AI-generated

**Q4: A colleague uses Copilot in Excel to build a formula that allocates shared service costs across business units. What is the appropriate next step?**
- A) Trust the formula since Copilot understands Excel natively
- B) Verify the formula logic, check cell references, and test with known values before relying on the output ✓
- C) Only verify if the allocation amounts look unreasonable
- D) Accept the formula but add a note that it was AI-generated

**Q5: During external audit preparation, you use AI to draft control descriptions and process narratives. Which of the following is true?**
- A) AI-drafted documentation satisfies SOX requirements as long as it is accurate
- B) The AI output must go through your standard review and approval process, and the audit trail must reflect who reviewed and approved the final documentation ✓
- C) AI-generated audit documentation does not require additional review since it follows standard templates
- D) External auditors will not accept any documentation that was AI-assisted
