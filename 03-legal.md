# Legal: AI-Assisted Legal Work

## Section 1: Why AI Matters for Legal

The legal profession is at an inflection point. According to Thomson Reuters' 2024 Future of Professionals report, **79% of legal departments plan to adopt generative AI within 12 months**. This is not speculative — firms and in-house teams are already deploying these tools in production workflows.

The efficiency gains are measurable. Contract review tasks that historically require 2–3 hours of attorney time can be reduced to 20–30 minutes with AI assistance. For high-volume work like NDA review, lease abstraction, or regulatory compliance mapping, the compounding time savings are substantial.

### What AI CAN Do

- **Draft initial contract versions** from term sheets or deal summaries
- **Extract key clauses** from lengthy agreements (termination, indemnification, liability caps, IP assignment, data processing obligations)
- **Summarize regulations and statutes** into structured, actionable overviews
- **Generate policy templates** based on specified requirements and company context
- **Flag potential risks** in contracts — unusual terms, missing standard provisions, one-sided obligations
- **Research case law and precedent** — surface relevant authorities for a given legal question
- **Translate legalese** into plain-language summaries for business stakeholders

### What AI CANNOT Do

- **Provide legal advice.** AI generates text, not counsel. It has no understanding of your client's risk tolerance, strategic objectives, or business context.
- **Make judgment calls on risk.** Determining whether a liability cap is commercially acceptable requires human legal judgment that AI fundamentally lacks.
- **Understand jurisdictional nuances without guidance.** AI defaults to general (often US-centric) legal frameworks unless explicitly directed otherwise.
- **Replace attorney-client privilege.** Communications with AI tools are not privileged. Pasting privileged content into an AI tool may waive privilege entirely.
- **Guarantee accuracy of legal citations.** AI can and does fabricate case names, citation numbers, and holdings. Every citation must be verified against primary sources.

> **Bottom line:** AI is a drafting and research accelerator. It produces first drafts, not final work product. Every output requires qualified attorney review before it leaves your desk.

---

## Section 2: Core AI Tools

### General AI Assistants

| Tool | Best For | Key Strength |
|------|----------|--------------|
| **ChatGPT** | Quick legal research queries, plain-language explanations of complex regulations, brainstorming alternative clause language | Fast iteration on drafting; broad general legal knowledge |
| **Claude** | Long contract analysis (handles 100K+ token context windows), drafting detailed legal memos, comparing document versions side-by-side | Excels at processing lengthy documents in a single pass — ideal for full agreement review |
| **Gemini** | Recent regulatory changes (web-connected), jurisdiction-specific research, cross-referencing current enforcement actions | Access to current information; useful for fast-moving regulatory landscapes |

### Microsoft Copilot for M365

Copilot is integrated directly into the tools your team already uses daily:

- **Word** — Draft contracts, generate redline summaries, create policy documents and legal memoranda. Copilot can restructure existing drafts, suggest clause alternatives, and summarize tracked changes across document versions.
- **Excel** — Matter tracking and reporting, deadline management across active matters, outside counsel cost analysis, budget-to-actual comparisons for legal spend.
- **PowerPoint** — Board-ready presentations on legal risk posture, compliance training decks, regulatory update summaries for executive leadership.
- **Outlook** — Draft client communications, summarize lengthy email threads on active matters, prepare stakeholder update summaries from scattered correspondence.
- **Teams** — Generate meeting minutes from legal review sessions, extract action items with assigned owners, summarize key decisions from recorded calls.

### A Note on Legal-Specific Tools

Specialized legal AI platforms — such as Harvey, CoCounsel (Thomson Reuters), and Lexis+ AI — offer capabilities tailored to legal workflows, including verified citation linking and jurisdiction-aware research. These tools are **not covered in this module**. Check with your legal operations team for approved specialized tools and any firm-specific usage policies that apply.

> **Important:** Only use AI tools that have been approved by your organization. Legal data is among the most sensitive categories of information your company handles. There are no exceptions to this policy — do not use unapproved tools, browser extensions, or personal AI accounts for any work-related legal content.

---

## Section 3: Practical Applications

### Use Case 1: Contract Review & Clause Extraction

**Scenario:** You have received a 40-page vendor services agreement for review. The business team needs your analysis by end of day, focusing on key commercial and risk terms. Manually reviewing and abstracting this agreement would take 2–3 hours.

**Prompt:**

```
Review the attached vendor services agreement and extract the following provisions into a structured summary table:

1. Term and termination rights (including termination for convenience, cure periods)
2. Liability caps and limitations of liability (including carve-outs)
3. Indemnification obligations (scope, caps, procedures, mutual vs. one-way)
4. Intellectual property ownership and licensing (including work product, pre-existing IP)
5. Data processing and privacy obligations (including sub-processors, breach notification)
6. Insurance requirements
7. Non-compete and non-solicitation restrictions
8. Governing law and dispute resolution

For each provision, include:
- Section reference number
- Summary of the term
- Whether the term is mutual or one-sided
- Any notable deviations from market standard

Flag any provisions that are missing but would typically be expected in an agreement of this type.
```

**What the output looks like:** A structured table covering each provision category with section references, plain-language summaries, and flagged items. The AI will typically identify missing provisions (e.g., force majeure, assignment restrictions) and note asymmetric obligations.

**Tips for better results:**
- Paste the full agreement text rather than summarizing it yourself — AI works best with the source document
- Specify your company's position (buyer/seller, licensor/licensee) so the AI can flag terms that are unfavorable to your side
- If you have a clause library or preferred positions, include key requirements in the prompt for comparison
- Always verify section references against the actual document — AI occasionally miscounts or cross-references incorrectly

---

### Use Case 2: Regulatory Research

**Scenario:** A new EU regulation affecting your company's data practices has been published. Your CISO and DPO need a briefing on what it requires and what operational changes may be necessary. You need to deliver a preliminary assessment quickly.

**Prompt:**

```
Summarize the key requirements of [specific regulation name and number] that took effect on [date]. Structure the summary as follows:

1. Scope: Who does this regulation apply to? (entity types, revenue thresholds, geographic applicability)
2. Key obligations: List each material obligation with a one-paragraph explanation
3. Timeline: Compliance deadlines and any phased implementation
4. Penalties: Maximum fines and enforcement mechanisms
5. Action items: Based on these requirements, identify 8-10 specific steps a [company size/type] company should take to achieve compliance
6. Interaction with existing law: How does this regulation interact with GDPR, existing national laws, and sector-specific regulations?

Focus on practical compliance requirements, not legislative history. Our company is [brief description — industry, size, data processing activities, operating jurisdictions].
```

**What the output looks like:** A structured regulatory briefing covering scope, obligations, deadlines, and recommended action items. The AI provides a solid starting framework for your compliance assessment.

**Tips for better results:**
- Include the full regulation text if available — do not rely on AI's training data for recent regulations, as it may be outdated or incomplete
- Specify your jurisdiction and entity type explicitly — "a German-headquartered SaaS company with US and UK subsidiaries processing health data" is far more useful than "our company"
- Always verify the AI's characterization of penalties and deadlines against the official published text
- Use this as a research accelerator, not a substitute for reading the regulation yourself

---

### Use Case 3: Policy Drafting

**Scenario:** HR has requested an updated remote work policy that addresses new regulatory requirements and company practices. You need to draft a policy that is legally sound, clear for employees, and consistent with existing company policies.

**Prompt:**

```
Draft a remote work policy for [Company Name] with the following parameters:

Company context:
- Industry: [industry]
- Employees: [number] across [jurisdictions]
- Existing policies to align with: [list relevant policies — data protection, BYOD, expense reimbursement]

The policy must address:
1. Eligibility criteria and approval process
2. Work location requirements and restrictions (including cross-border/cross-state work limitations)
3. Equipment and expense reimbursement (aligned with [applicable state/country] requirements)
4. Data security obligations for remote workers (referencing our existing Information Security Policy)
5. Working hours, availability expectations, and time zone considerations
6. Health and safety obligations (home workspace requirements)
7. Tax and benefits implications notice (not advice — direct employees to HR/Tax)
8. Termination of remote work arrangement (conditions, notice period)
9. Governing policy hierarchy (this policy subordinate to employment agreement and local law)

Tone: Professional, clear, directive. Use "must" for mandatory requirements and "should" for recommendations. Include section numbering. Draft for [primary jurisdiction] but flag provisions that may need jurisdiction-specific adjustments.
```

**What the output looks like:** A structured policy document with numbered sections, clear mandatory and permissive language, and placeholder notes where jurisdiction-specific customization is needed. Typically 4–6 pages.

**Tips for better results:**
- Provide existing company policies as context so the AI maintains consistent terminology and cross-references
- Specify the primary jurisdiction — employment law varies dramatically between states and countries
- Ask the AI to flag areas requiring local counsel review rather than attempting to address all jurisdictions
- Review carefully for overly broad commitments the company may not intend to make

---

### Use Case 4: Risk Assessment

**Scenario:** The business development team has shared a draft partnership agreement with a technology vendor. Before the deal moves forward, you need to identify key risk areas and recommend mitigations for the negotiation team.

**Prompt:**

```
Analyze this draft partnership agreement and prepare a risk assessment. For each risk identified:

1. Risk description: What is the specific concern?
2. Severity: High / Medium / Low
3. Likelihood: How likely is this risk to materialize?
4. Relevant provision: Reference the specific section
5. Recommended mitigation: What changes should we negotiate?
6. Fallback position: If the counterparty rejects our preferred position, what is our minimum acceptable term?

Pay particular attention to:
- Uncapped liability or indemnification provisions
- One-sided termination rights
- Broad IP assignment or licensing provisions
- Non-compete restrictions that could limit our business operations
- Data sharing obligations and restrictions on data use
- Ambiguous performance standards or SLAs without remedies
- Auto-renewal terms with limited termination windows
- Most-favored-nation clauses
- Change of control provisions

Our company is the [buyer/seller/licensee/partner]. Our priority is [state key business objective — e.g., protecting our proprietary data, maintaining flexibility to terminate, limiting financial exposure].
```

**What the output looks like:** A structured risk register with 10–15 identified risks, severity ratings, section references, and specific recommended redline positions. The AI typically identifies both obvious risks (uncapped indemnification) and subtler issues (ambiguous definitions, missing provisions).

**Tips for better results:**
- State your company's position and priorities clearly — the same clause can be favorable or unfavorable depending on which side you represent
- Include any deal-specific context (e.g., "this is a $2M annual commitment" or "the vendor will have access to our customer data") to help the AI assess severity appropriately
- Use the output as a starting framework and apply your own judgment on severity and commercial acceptability
- Cross-reference flagged risks against your organization's standard risk matrix and approval thresholds

---

### Use Case 5: Plain-Language Summaries

**Scenario:** The finance team needs to understand the payment terms, penalty provisions, and termination costs in a licensing agreement, but the 25-page contract is dense with legal terminology. You need to produce a business-friendly summary they can act on.

**Prompt:**

```
Create a plain-language executive summary of the attached licensing agreement for a non-legal audience (finance and business operations). The summary should:

1. Use clear, non-technical language — avoid legal jargon
2. Explain what each provision means in practical business terms
3. Highlight financial obligations: payment terms, fee escalation, penalties, termination costs
4. Call out key dates and deadlines in a simple timeline format
5. Identify decisions or actions the business team needs to take, with deadlines
6. Include a "What This Means For Us" section that translates legal obligations into operational impact

Format the summary in three parts:
- **One-paragraph overview** (suitable for an executive who will read nothing else)
- **Key terms table** (term, what it means, what we need to do, deadline)
- **Detailed summary** (2-3 pages maximum, organized by topic not by contract section)

Audience: Finance Director and VP of Operations. They are commercially sophisticated but not legally trained.
```

**What the output looks like:** A structured, jargon-free summary with a concise executive overview, a scannable key terms table, and a readable narrative that translates legal obligations into business actions.

**Tips for better results:**
- Specify the audience and their concerns — a CFO cares about different provisions than a CTO
- Ask the AI to flag terms it has simplified so you can verify the simplification is accurate and does not misrepresent the legal position
- Review the summary against the source agreement to ensure no material terms were omitted or mischaracterized
- Consider including a brief disclaimer noting the summary is for informational purposes and does not constitute legal advice

---

## Section 4: Responsible AI Use

### Confidentiality — The Non-Negotiable Rule

**Never paste privileged communications, client confidential information, or opposing party documents into AI tools.**

This is the single most important rule for legal professionals using AI. Consider:

- **Attorney-client privilege may be waived** if privileged content is disclosed to a third-party AI service. Once waived, privilege cannot be restored.
- **Work product protection** may be compromised by sharing litigation strategy, mental impressions, or case analysis with an AI tool.
- **Opposing party documents** received under confidentiality provisions or protective orders must not be processed through external AI services.
- **Client confidential information** — including deal terms, settlement amounts, investigation findings, and personally identifiable information — must never be entered into unapproved tools.

**Practical guidance:** Before pasting any content into an AI tool, ask yourself: *"Would I be comfortable if this text appeared in a data breach disclosure?"* If the answer is no, do not paste it.

### Hallucination Risk — AI Fabricates Citations

This risk cannot be overstated. AI models routinely generate:

- **Fabricated case names** that sound plausible but do not exist
- **Incorrect citation numbers** for real cases
- **Inaccurate holdings** — attributing the wrong ruling to a real case
- **Non-existent statutes or regulations** with convincing section numbers

In 2023, multiple attorneys faced sanctions for submitting AI-generated briefs containing fabricated citations. This is not a theoretical risk — it is an active, documented problem.

**Rule: Every legal citation generated by AI must be verified against a primary source (Westlaw, LexisNexis, official government databases) before use. No exceptions.**

### Jurisdiction Matters

AI tools default to general legal principles, often US-centric. If you are working in or advising on a matter involving a specific jurisdiction:

- **Always specify the jurisdiction** in your prompt — "under German law," "pursuant to California Civil Code," "under English contract law"
- **State the applicable governing law** if the matter involves a contract
- **Identify relevant regulatory bodies** if the question involves compliance
- Do not assume the AI's response accounts for local statutory requirements, court rules, or regulatory guidance

### Review Requirements

**Every AI-generated legal document must be reviewed by a qualified attorney before use.** This applies to:

- Contracts and contract amendments
- Legal memoranda and research summaries
- Policy documents
- Regulatory assessments
- Client communications
- Board and committee materials

AI output is a first draft — treat it accordingly. Review for legal accuracy, completeness, consistency with your client's or company's position, and compliance with applicable law.

### Regulatory Compliance

Legal professionals operate under jurisdiction-specific ethical obligations. Be aware of:

- **Bar association guidance** on AI use — several state bars and law societies have issued formal opinions or guidance
- **Court rules** requiring disclosure of AI use in filings (an increasing number of courts now require this)
- **Continuing competence obligations** — understanding AI's capabilities and limitations is increasingly part of a lawyer's duty of competence
- **Supervisory obligations** — senior attorneys remain responsible for the accuracy of work product, regardless of whether AI assisted in its preparation

Check your jurisdiction's rules. When in doubt, disclose AI use and verify everything.

### Company Policy

Use only approved AI tools for any work-related legal content. Legal data is among the most sensitive categories your organization handles:

- No personal AI accounts for work content
- No unapproved browser extensions or plugins that process text through AI
- No copying of work content into free-tier or consumer AI products
- Follow your organization's data classification policies — if content is classified as confidential or above, confirm your AI tool is approved for that classification level

---

## Quiz

**Q1: You use an AI tool to research case law for a brief. The AI provides three case citations that appear directly on point. What is the correct next step?**

- A) Include the citations in your brief — AI tools are trained on legal databases and the citations are reliable
- B) Verify each citation against a primary legal research platform (Westlaw, LexisNexis) before including them ✓
- C) Include the citations but add a footnote noting they were AI-generated
- D) Ask the AI to confirm the citations are accurate by re-prompting

**Q2: A colleague asks you to paste the opposing party's settlement demand letter into an AI tool to help draft a response strategy. What should you do?**

- A) Proceed — the AI tool will keep the content confidential
- B) Proceed only if the AI tool has enterprise-grade security
- C) Decline — opposing party documents and litigation strategy should not be entered into AI tools ✓
- D) Proceed but redact the party names first

**Q3: An AI tool drafts a limitation of liability clause for a vendor agreement. The clause states: "Vendor's total aggregate liability shall not exceed the fees paid in the twelve (12) months preceding the claim." What should you do before accepting this clause?**

- A) Accept it — this is a standard market limitation
- B) Review whether the liability cap amount is appropriate for this deal, check for necessary carve-outs (IP indemnification, confidentiality breach, willful misconduct), and verify it aligns with your company's risk position ✓
- C) Reject it and draft the clause manually — AI cannot draft reliable contract language
- D) Accept it but increase the look-back period to twenty-four months

**Q4: You are researching employment law requirements for your company's new office in Ontario, Canada. What is the most important instruction to include in your AI prompt?**

- A) Ask the AI to provide the most recent case law on the topic
- B) Specify that the analysis should be under Ontario provincial and Canadian federal employment law, not US law ✓
- C) Request that the AI cite only Supreme Court of Canada decisions
- D) Ask the AI to compare Ontario law with your home jurisdiction

**Q5: Your company has approved an enterprise AI tool for general business use. A partner asks you to use it to summarize a privileged legal memo about a pending regulatory investigation. What is the correct approach?**

- A) Proceed — the tool is enterprise-approved and therefore safe for all content
- B) Proceed but remove the client's name from the memo first
- C) Do not enter privileged content into the AI tool — enterprise approval for general use does not authorize processing of privileged legal communications; confirm with legal ops whether the tool is approved for privileged content ✓
- D) Proceed only if the regulatory investigation is not yet public knowledge
