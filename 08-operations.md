# Operations: AI-Assisted Operations Management

> **Module 8 of 8** | Cross-Functional AI Training Program
> Target audience: Operations Managers, Project Managers, Procurement Specialists, Business Operations Analysts

---

## Section 1: Why AI Matters for Operations

Operations is the engine room of any organization — the team that keeps processes running, vendors managed, projects tracked, and information flowing. It's also one of the functions where AI delivers the most immediate, tangible time savings.

### The Adoption Landscape

- **65% of operations leaders** have implemented or are piloting AI tools for process improvement (McKinsey Operations Survey 2024)
- **72% of project managers** report using AI for status reporting and documentation (PMI Pulse of the Profession 2025)
- Organizations using AI in operations report **25-40% reduction** in administrative overhead

### Where AI Saves Time

| Task | Without AI | With AI | Savings |
|------|-----------|---------|---------|
| Process documentation (SOP) | 3-4 hours | 30-45 minutes | ~80% |
| Meeting summary + action items | 20-30 minutes | 2-3 minutes | ~90% |
| RFP first draft | 2-3 days | 3-4 hours | ~75% |
| Weekly status report | 45-60 minutes | 10-15 minutes | ~75% |
| Vendor comparison matrix | 2-3 hours | 30-40 minutes | ~75% |

### What AI Can Do for Operations

- Draft process documentation and SOPs from verbal descriptions or rough notes
- Summarize meetings and extract action items with owners and deadlines
- Generate RFP templates and evaluation criteria
- Create consistent project status reports from raw updates
- Build vendor comparison frameworks and evaluation matrices
- Draft internal communications and cross-functional updates
- Organize and structure information from multiple sources

### What AI Cannot Do

- Manage vendor relationships (trust and rapport are human)
- Make procurement decisions (budget authority, strategic fit, risk tolerance)
- Understand organizational politics and stakeholder dynamics
- Replace project management judgment on priorities and trade-offs
- Handle physical logistics and real-time operational decisions
- Enforce accountability — only people can hold other people accountable

---

## Section 2: Core AI Tools

### General AI Assistants

**ChatGPT** — Your go-to for quick, structured outputs
- Meeting summaries from rough notes
- Checklist and template generation
- Quick process outlines
- Email drafts for vendor or cross-functional communication

**Claude** — Best for long, detailed documents
- Comprehensive RFP drafts (handles large context well)
- Detailed vendor evaluation analyses
- Full process documentation with decision trees
- Complex project charters and scope documents

**Gemini** — Best for research-backed outputs
- Vendor research and market rate analysis (web-connected)
- Industry benchmarking for operational metrics
- Best practice research for process improvement

### Microsoft Copilot for M365

Copilot is particularly powerful for Operations because ops teams live in M365.

**Word**
- Draft SOPs, process manuals, and runbooks
- Generate RFPs from requirements lists
- Create project charters and scope documents
- Write vendor contracts and service level agreements

**Excel**
- Analyze budget data and create spending summaries
- Build resource allocation models
- Generate vendor comparison matrices from raw data
- Create capacity planning worksheets with formulas

**PowerPoint**
- Generate project status decks from bullet points
- Create operations review presentations
- Build process improvement proposal slides
- Transform data into visual dashboards

**Outlook**
- Draft vendor communications and follow-ups
- Summarize long email threads (critical for ops — you're CC'd on everything)
- Create cross-functional coordination emails
- Generate meeting agenda drafts from previous notes

**Teams**
- **Meeting recaps** — this is a game-changer for ops. Copilot automatically generates structured summaries with decisions, action items, and open questions from any Teams meeting
- Project standup summaries
- Decision logs from channel discussions
- Shift handoff notes

---

## Section 3: Practical Applications

### Use Case 1: Process Documentation

**Scenario**: Your team has a procurement approval workflow that exists only in people's heads. Three people do it slightly differently. You need a standardized SOP.

**Prompt**:
```
I need to create a Standard Operating Procedure (SOP) for our procurement approval workflow. Here's what I know from interviews with the team:

- Requests under $5,000: manager approval only
- Requests $5,000-$25,000: manager + department head approval
- Requests over $25,000: manager + department head + VP Finance approval
- All requests need a purchase order number from the finance system
- Preferred vendors can skip the RFQ step
- New vendors need 3 quotes for anything over $10,000
- Average turnaround: 2 days for small, 5 days for medium, 10 days for large
- Common issues: missing budget codes, incomplete vendor info

Create a detailed SOP with:
1. Purpose and scope
2. Roles and responsibilities (RACI format)
3. Step-by-step process with decision points
4. Required forms/information at each step
5. Exception handling procedures
6. SLA targets
```

**What AI produces**: A structured SOP document with clear decision trees, role assignments, and exception handling — typically 80-90% complete. You'll need to verify specific system names, form numbers, and approval thresholds with stakeholders.

**Tips for better results**:
- Include real examples of exceptions and edge cases — AI handles these well when given context
- Specify your company's documentation format/template if you have one
- Ask AI to generate a process flow diagram description that you can convert to a visual

---

### Use Case 2: Meeting Summaries & Action Items

**Scenario**: You just finished a 45-minute cross-functional meeting with 12 people about a new office relocation project. You need a structured summary.

**Prompt**:
```
Summarize this meeting transcript into a structured format:

[Paste meeting notes or transcript]

Format the summary as:
1. **Meeting Overview** (2-3 sentences: purpose, attendees, date)
2. **Key Decisions Made** (numbered list with decision owner)
3. **Action Items** (table format: Action | Owner | Deadline | Priority)
4. **Open Questions / Parking Lot** (items that need follow-up)
5. **Next Steps** (what happens next and when)

Rules:
- If no deadline was explicitly stated, flag it as "TBD — needs deadline"
- If ownership is unclear, mark as "Unassigned — needs owner"
- Prioritize action items as High/Medium/Low based on project timeline impact
```

**What AI produces**: A clean, structured summary that you can paste directly into your project management tool or email to stakeholders. The action item table is particularly useful.

**Tips for better results**:
- If using Teams with Copilot, it generates meeting recaps automatically — start there
- For rough notes, include speaker names so AI can assign action items correctly
- Ask AI to flag any conflicting statements or unclear commitments

---

### Use Case 3: RFP Drafting

**Scenario**: You need an RFP for a new facilities management vendor. You have a list of requirements but no time to write a formal document.

**Prompt**:
```
Draft a Request for Proposal (RFP) for facilities management services for our company. Here are the details:

Company: Mid-size tech company, 3 office locations (HQ: 50,000 sq ft, Branch 1: 15,000 sq ft, Branch 2: 10,000 sq ft)
Current contract expires: June 30, 2026
Budget range: $500K-$750K annually
Key services needed:
- Janitorial (daily cleaning, deep cleaning monthly)
- HVAC maintenance (quarterly inspections, emergency repair)
- Security (24/7 access control, visitor management)
- Landscaping (weekly maintenance, seasonal updates)
- Minor repairs and maintenance

Must-haves:
- 24/7 emergency response (< 2 hour SLA)
- Dedicated account manager
- Monthly reporting dashboard
- Green/sustainable cleaning products
- Background checks for all on-site staff

Evaluation criteria: Cost (30%), Service quality (25%), Experience (20%), Sustainability (15%), Technology/reporting (10%)

Timeline:
- RFP issued: March 15
- Questions due: March 25
- Proposals due: April 15
- Vendor presentations: April 21-25
- Decision: May 1

Include standard RFP sections: introduction, scope, requirements, evaluation criteria, submission instructions, timeline, terms and conditions.
```

**What AI produces**: A professional, 8-12 page RFP document with all standard sections, formatted evaluation criteria, and submission requirements. You'll need to add company-specific legal terms and verify budget/timeline details.

**Tips for better results**:
- Include your company's standard terms or reference them
- Specify the response format you want from vendors (makes evaluation easier)
- Ask AI to generate an evaluation scorecard template alongside the RFP

---

### Use Case 4: Project Status Reports

**Scenario**: You manage 5 projects and need to send a weekly status update to leadership. You have raw updates from each project lead.

**Prompt**:
```
Create a weekly project status report from these raw updates. Use RAG status (Red/Amber/Green) for each project.

Project 1 - Office Relocation:
"Construction is 2 weeks behind schedule due to permit delays. Budget is on track. Movers are confirmed for the new date. IT infrastructure work hasn't started yet."

Project 2 - ERP Implementation:
"Phase 2 testing completed on time. 3 critical bugs found, 2 fixed, 1 being worked on. Go-live still targeted for April 1. Training materials are 80% complete."

Project 3 - Vendor Consolidation:
"Completed evaluation of 12 vendors. Shortlisted to 4. Negotiations starting next week. Expected savings of 18% vs current spend. Legal review of contracts pending."

Project 4 - Process Automation:
"Pilot completed successfully. 40% time reduction confirmed. Full rollout plan being drafted. Need additional budget approval for 2 more licenses ($15K)."

Project 5 - Compliance Audit Prep:
"All documentation gathered. Mock audit scheduled for March 10. Two gaps identified: data retention policy needs update, access control logs incomplete for Q3."

Format as:
| Project | Status | Progress | Key Update | Risks/Blockers | Next Week |
Use RAG indicators: 🟢 Green (on track), 🟡 Amber (at risk), 🔴 Red (off track)

Then add a 3-sentence executive summary highlighting the most important items leadership needs to know.
```

**What AI produces**: A formatted status table with appropriate RAG ratings and a concise executive summary. The RAG assignments are usually accurate when you provide enough context about timelines and impacts.

**Tips for better results**:
- Be consistent with the format each week — AI can match a template you provide
- Include previous week's status so AI can highlight changes
- Ask AI to flag items that need leadership decision or escalation

---

### Use Case 5: Vendor Evaluation

**Scenario**: You received proposals from 3 vendors for a cloud migration project and need to create a structured comparison for the steering committee.

**Prompt**:
```
Create a vendor evaluation matrix for these 3 cloud migration proposals. Use the following weighted criteria:

Criteria and weights:
- Technical capability (25%)
- Cost (25%)
- Implementation timeline (20%)
- Support & SLA (15%)
- References & experience (15%)

Vendor A - CloudFirst:
- Proposed cost: $280K over 18 months
- Timeline: 12 months
- Team: 8 people, 3 AWS-certified architects
- SLA: 99.95% uptime, 1-hour response for critical issues
- References: 5 similar-size migrations, all in tech sector
- Approach: Lift-and-shift first, then optimize

Vendor B - MigrateNow:
- Proposed cost: $220K over 12 months
- Timeline: 8 months (aggressive)
- Team: 5 people, 2 AWS-certified
- SLA: 99.9% uptime, 4-hour response for critical issues
- References: 15 migrations total, 3 similar size, mixed industries
- Approach: Re-architect during migration

Vendor C - SkyBridge:
- Proposed cost: $310K over 24 months
- Timeline: 14 months
- Team: 10 people, 4 AWS-certified, 1 dedicated PM
- SLA: 99.99% uptime, 30-minute response for critical issues
- References: 8 similar-size migrations, 2 in our industry
- Approach: Phased migration with parallel running

Create:
1. Scoring matrix (1-5 scale for each criterion, with weighted totals)
2. Pros/cons summary for each vendor
3. Risk assessment for each vendor
4. Recommendation with rationale
```

**What AI produces**: A detailed evaluation matrix with scoring, risk analysis, and a reasoned recommendation. The structure is immediately presentation-ready for a steering committee.

**Tips for better results**:
- Include your organization's specific priorities (e.g., "we value reliability over speed")
- Ask AI to highlight hidden costs or risks in each proposal
- Request a "questions to ask each vendor" list for the presentation round

---

## Section 4: Responsible AI Use

### What NOT to Share with AI

Operations teams handle a wide range of sensitive information. Be mindful of what goes into AI prompts:

| Never Share | Why |
|------------|-----|
| Full vendor contracts with pricing | Commercial confidentiality; vendor terms are proprietary |
| Internal budget figures and cost breakdowns | Financial data is confidential |
| Employee performance data from ops reviews | Employee PII and performance data are protected |
| Security procedures and access controls | Security-sensitive operational details |
| Proprietary process IP | Trade secrets and competitive advantages |
| Vendor negotiations in progress | Could compromise negotiating position |

**Safe to share** (anonymized/generalized):
- Generic process descriptions without system names
- Publicly available vendor information
- General project timelines and milestones
- Industry-standard frameworks and templates

### Review Requirements

Operations documents affect how work gets done across the organization. Before distributing any AI-generated content:

1. **SOPs**: Verify every step against actual practice. AI doesn't know your systems, tools, or exceptions.
2. **RFPs**: Have procurement and legal review before issuing. AI may miss required clauses or compliance requirements.
3. **Status reports**: Confirm RAG ratings and metrics against actual data. AI can't verify project status — only you can.
4. **Vendor evaluations**: Validate scoring against actual proposal content. AI may misinterpret vendor claims.

### Accuracy in Reporting

This is critical: **AI-generated status reports must reflect actual project state**. Don't let AI invent progress, smooth over risks, or create a rosier picture than reality. Your credibility depends on accuracy.

- Always verify numbers and dates against source data
- Check that action items are assigned to real people who agreed to own them
- Ensure risk assessments reflect actual conditions, not AI's optimistic defaults

### Company Policy Reminders

- **Approved tools only**: ChatGPT, Claude, Gemini, Microsoft Copilot
- **No shadow AI**: Don't use unapproved tools, browser extensions, or plugins for work data
- **You own the output**: AI is a drafting assistant — every document that goes out has your name on it
- **When in doubt, leave it out**: If you're unsure whether data is sensitive, don't include it in a prompt

---

## Quiz

**Q1: A colleague says "AI can write our SOPs so we don't need to interview process owners anymore." What's the best response?**
- A) They're right — AI can generate processes from industry best practices
- B) AI can draft SOPs, but you still need process owner input to capture how things actually work here ✓
- C) AI can't write SOPs at all — they're too complex
- D) Just use Microsoft Copilot — it already knows your company's processes

**Q2: Which Microsoft Copilot feature is most valuable for operations teams managing multiple meetings per day?**
- A) PowerPoint slide generation
- B) Excel formula assistance
- C) Teams meeting recaps with action items ✓
- D) Word document formatting

**Q3: You're drafting an RFP using AI and the output includes a section on vendor insurance requirements. What should you do?**
- A) Keep it — AI knows standard RFP requirements
- B) Remove it — insurance requirements are unnecessary
- C) Have your procurement and legal teams review it to ensure it matches your company's actual requirements ✓
- D) Replace it with a simpler version to save vendors time

**Q4: Which of the following is safe to include in an AI prompt when evaluating vendors?**
- A) The exact pricing from each vendor's confidential proposal
- B) Your company's maximum budget for the project
- C) Publicly available information about vendor capabilities and services ✓
- D) Internal emails about your negotiation strategy

**Q5: Your AI-generated weekly status report shows all projects as "Green" but you know one project missed its deadline last week. What should you do?**
- A) Send it as-is — the AI probably assessed it correctly based on the data you provided
- B) Correct the status to reflect reality before sending — you own the accuracy of the report ✓
- C) Add a footnote saying "AI-generated, accuracy not guaranteed"
- D) Don't use AI for status reports anymore
