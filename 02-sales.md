# Sales: AI-Assisted Selling

## Section 1: Why AI Matters for Sales

The way top performers sell is changing. AI won't replace salespeople — but salespeople who use AI will outperform those who don't.

### The numbers tell the story

- **69% of sales professionals** say AI helps them personalize prospect outreach more effectively (Salesforce State of Sales, 2024)
- **Reps spend only 28% of their time actually selling.** The rest goes to admin work, CRM updates, internal emails, and meeting prep. AI can take a massive chunk of that non-selling time off your plate.
- **Companies using AI in sales** report higher win rates, shorter sales cycles, and more pipeline generated per rep.

### What AI CAN do for you

- **Draft outreach emails** — cold emails, follow-ups, breakup emails, re-engagement sequences
- **Research prospects** — pull together company context, recent news, funding rounds, tech stack, and likely pain points before a call
- **Prepare call briefs** — synthesize everything you know about an account into a one-page prep doc
- **Generate proposals and SOWs** — turn deal notes into polished documents in minutes, not hours
- **Handle objection scripts** — brainstorm multiple angles for common pushback so you're never caught flat-footed
- **Enrich CRM data** — summarize call notes, draft deal updates, clean up pipeline entries

### What AI CANNOT do

- **Build genuine relationships.** Deals close on trust, and trust is earned person-to-person.
- **Read the room on a live call.** AI can't pick up on tone shifts, hesitation, or the unspoken signals that tell you when to push and when to pull back.
- **Close deals through empathy.** Complex enterprise sales require understanding a buyer's internal politics, career risk, and personal motivations — that's human territory.
- **Handle nuanced negotiations.** Pricing discussions, contract redlines, and executive alignment require judgment that AI simply doesn't have.

**Bottom line:** AI handles the prep work and busy work. You handle the relationships and the close. Together, you sell more in less time.

---

## Section 2: Core AI Tools

### General AI Assistants

| Tool | Best For | Sales Sweet Spot |
|------|----------|------------------|
| **ChatGPT** | Quick drafts, brainstorming, role-play | Rapid-fire email drafts, generating objection responses, simulating prospect conversations to sharpen your pitch |
| **Claude** | Long-form content, complex analysis | Multi-page proposals, analyzing RFP requirements, processing large deal context with many stakeholders |
| **Gemini** | Web-connected research, synthesis | Prospect research with real-time web access, company news roundups, competitive landscape summaries |

**Use what's approved by your organization.** Don't paste prospect data into random AI chatbots or free-tier tools that haven't been vetted. If you're not sure whether a tool is approved, ask before you use it.

### Microsoft Copilot for M365

If your org runs Microsoft 365, Copilot is already built into the tools you use every day. No switching between apps, no copy-pasting — it works right where you work.

- **Word** — Draft proposals, SOWs, business cases, and executive summaries. Start from a blank page or ask Copilot to restructure an existing doc for a different audience.
- **Excel** — Pipeline analysis, commission calculations, territory planning, and quota attainment tracking. Ask questions about your data in plain language: *"Show me deals over $50K that haven't moved stages in 30 days."*
- **PowerPoint** — Generate sales decks, QBR presentations, and case study slides. Turn a Word doc or outline into a polished deck in minutes.
- **Outlook** — Write personalized outreach emails, draft follow-ups, and generate meeting prep summaries. Copilot can reference previous email threads to keep context.
- **Teams** — Get call recap summaries with action items after deal review meetings. Never miss a next step from a prospect call again.

**The advantage:** Copilot works within your company's security boundary, so it's typically safer for internal data than external AI tools. Always follow your company's data handling policy.

---

## Section 3: Practical Applications

### Use Case 1: Prospecting & Research

**Scenario:** You're an AE with a first call tomorrow with the VP of Engineering at a mid-market SaaS company. You have 20 minutes to prep. You need to understand their world, not just their company's Wikipedia page.

**Example prompt:**

```
I have a discovery call tomorrow with [Name], VP of Engineering at [Company].

Here's what I know:
- Series B SaaS company, ~200 employees
- They sell [product category] to [target market]
- Based in [city]

Help me prepare by giving me:
1. Three likely pain points a VP of Engineering at this stage/size company faces
2. Recent company news or trends in their space I should reference
3. Smart discovery questions that show I've done my homework
4. Potential ways our solution ([brief description]) maps to their likely challenges
5. One insight or perspective I can share to add value on the call

Keep it concise — I need a one-page call prep, not a novel.
```

**What the AI output looks like:** A structured call prep doc with specific pain points (e.g., scaling engineering velocity, managing technical debt post-Series B, hiring challenges), 3–4 tailored discovery questions, and a "value hook" — an insight you can share to establish credibility before you even start pitching.

**Tips for better results:**
- Include your product's value prop in the prompt so the AI can map pain points to your solution
- Add any context from LinkedIn, mutual connections, or previous CRM notes — the more you give, the better the output
- Run this through Gemini if you want real-time company news pulled in automatically

---

### Use Case 2: Email Personalization at Scale

**Scenario:** You're an SDR who needs to send 50 personalized cold emails this week across three different personas (VP Sales, VP Marketing, CRO) in the fintech space. Writing each one from scratch would take hours. Copy-pasting the same template gets you ignored.

**Example prompt:**

```
I need to write personalized cold outreach emails for three personas in fintech.

Our product: [one-sentence value prop]
Key differentiator: [what makes us different]

Persona 1: VP of Sales — cares about pipeline velocity, rep productivity, forecast accuracy
Persona 2: VP of Marketing — cares about lead quality, attribution, campaign ROI
Persona 3: CRO — cares about revenue growth, alignment between sales and marketing, board metrics

For each persona, write:
- A subject line (under 8 words, no clickbait)
- A 4-sentence cold email: hook (reference their likely pain), bridge (how we help), proof point (one stat or customer example), CTA (low-friction ask)
- Two variations of the hook sentence so I can A/B test

Tone: direct, peer-to-peer, zero fluff. Write like a top-performing SDR, not a marketing team.
```

**What the AI output looks like:** Three persona-specific email templates, each with a sharp subject line, a concise body that speaks directly to that persona's priorities, and two hook variations for testing. You get 50 emails' worth of raw material in under two minutes.

**Tips for better results:**
- Always personalize further before sending — swap in the prospect's name, company, and one specific detail (recent funding round, job posting, LinkedIn post) so it doesn't read as templated
- Test which hook variations get better open and reply rates, then feed that data back into future prompts
- Never send an AI-generated email without reading it yourself. One wrong detail or tone-deaf line can tank your credibility

---

### Use Case 3: Proposal Generation

**Scenario:** You just got a verbal "yes" on a deal. The prospect wants a proposal by end of day. Normally this takes you 2–3 hours of pulling together pricing, timelines, and scope. You have 30 minutes before your next call.

**Example prompt:**

```
Help me draft a proposal for [prospect company]. Here's the deal context:

- Prospect: [Company], [industry], ~[size] employees
- Champion: [Name], [Title]
- Problem: [2-3 sentences on what they're trying to solve]
- Solution: [Which of our products/packages they need]
- Pricing: [Package name] at [$X/month or $X/year], [number] seats
- Implementation timeline: [X weeks]
- Key success metrics they care about: [e.g., 30% reduction in X, Y% improvement in Z]
- Competitive context: They also evaluated [competitor] — our edge is [differentiator]

Write a 2-page proposal with these sections:
1. Executive Summary — tie our solution to their specific problem (not generic)
2. Proposed Solution — what they get, how it works, why it fits
3. Investment & Timeline — pricing table, implementation phases, go-live date
4. Expected Outcomes — quantified where possible
5. Next Steps — clear action items with dates

Tone: confident, professional, client-focused. No jargon, no filler paragraphs.
```

**What the AI output looks like:** A clean, structured proposal that reads like you spent hours on it. The executive summary directly references the prospect's pain, the solution section maps features to their use case, and the pricing/timeline section is clear and specific.

**Tips for better results:**
- The more deal context you provide, the less generic the output — include specific things the prospect said during calls
- Always double-check pricing, dates, and any commitment language before sending. AI can hallucinate numbers.
- Save your best AI-generated proposals as templates for future deals in that segment
- **Never include confidential pricing from other customers or competitive deal intelligence in your prompts**

---

### Use Case 4: Objection Handling

**Scenario:** You're mid-cycle with a strong prospect, but they just hit you with: *"We already have a solution for this."* You need to respond thoughtfully without being pushy. Instead of winging it, you brainstorm with AI first.

**Example prompt:**

```
A prospect in my pipeline just said: "We already have a solution for this — we're using [competitor product]."

Context:
- They agreed to a demo, so there was initial interest
- Their current tool is [competitor] which is strong at [X] but weak at [Y, Z]
- Our differentiators: [list 2-3 key advantages]
- The champion is a [title] who cares about [priority]

Give me 5 different response approaches:
1. The "curiosity" approach — ask what's working and what's not
2. The "ROI challenge" — quantify what they might be leaving on the table
3. The "future state" approach — align with where they're headed, not where they are
4. The "social proof" play — reference a similar company that switched
5. The "low-risk" offer — suggest a side-by-side comparison or pilot

For each, write a 2-3 sentence email response and a verbal version I could use on a call.
Keep the tone consultative, not combative. I want to reopen the conversation, not win an argument.
```

**What the AI output looks like:** Five distinct approaches, each with both an email version and a talk-track version. The "curiosity" approach might ask what triggered their original evaluation; the "ROI challenge" might reference industry benchmarks. You pick the one that fits this prospect's personality and situation.

**Tips for better results:**
- Include what you know about the prospect's personality and communication style — some buyers respond to data, others to stories
- Use AI-generated objection scripts as *starting points* — your delivery and timing matter more than the exact words
- Build a personal objection-handling library over time by saving the best AI responses that actually worked

---

### Use Case 5: Call Prep & Follow-Up

**Scenario:** You just finished a 45-minute demo with three stakeholders. It went well — they asked great questions, flagged two concerns, and want next steps. You need to send a follow-up email within the hour while everything is fresh. You also need to prep for the next call with their CFO next week.

**Example prompt:**

```
I just finished a demo with [Company]. Help me write a follow-up email.

Attendees: [Name/Title], [Name/Title], [Name/Title]
Key points discussed:
- They're currently doing [process] manually, costing them ~[X] hours/week
- [Name] was excited about [specific feature] and asked how it integrates with [their tool]
- [Name] raised a concern about [specific concern — e.g., data migration timeline]
- They want to see a pricing proposal and involve their CFO in the next meeting

Write a follow-up email that:
1. Thanks them and references one specific moment from the call (not generic)
2. Recaps the 3 key takeaways (what they need, what we showed, what resonated)
3. Addresses the concern [Name] raised with a brief, reassuring answer
4. Proposes a clear next step: meeting with CFO next [day], with a pricing overview attached
5. Keeps it under 200 words — busy executives don't read essays

Tone: warm but professional. I want them to feel heard, not sold to.
```

**What the AI output looks like:** A polished follow-up email that references specific discussion points (not just "great meeting!"), acknowledges the concern that was raised, and drives clearly toward the next step. It reads like you spent 20 minutes crafting it, not 2.

**Tips for better results:**
- Write your call notes immediately after hanging up — even bullet points. The fresher your notes, the better the AI output.
- Include direct quotes from the prospect when possible ("When you mentioned that...") — this level of specificity builds trust
- Always review the AI's recap against your actual notes. If it fabricates a discussion point that didn't happen, you'll look careless.
- Use the same prompt structure to generate your CFO meeting prep doc, adding what you learned from this call

---

## Section 4: Responsible AI Use

AI can make you faster, but one careless mistake can cost you the deal — or worse. Here's what every sales professional needs to know.

### Never share with AI tools

- **Customer pricing and contract terms.** Your negotiated rates with Customer A are confidential. Pasting them into an AI tool to "help draft a similar proposal" risks exposing sensitive commercial data.
- **Competitive deal intelligence.** What you know about a competitor's pricing, weaknesses, or strategy from confidential sources doesn't belong in an AI prompt.
- **Customer PII.** Contact details, org charts, personal phone numbers, home addresses — keep all personally identifiable information out of AI tools.
- **Full CRM exports.** Don't dump raw CRM data into an AI chatbot. If you need AI to analyze pipeline data, use approved internal tools like Copilot within your M365 environment.

### Review everything before it goes out

Every AI-generated email, proposal, or document must be reviewed before you send it. No exceptions.

- **Wrong details kill deals.** AI might get a company name wrong, fabricate a statistic, or misstate your pricing. A prospect who catches an error loses confidence in you.
- **Tone matters.** AI defaults to generic. If your prospect is casual, the email shouldn't read like a legal brief. If they're a C-suite executive, it shouldn't read like a text message.
- **Your name is on it.** When you hit send, it's your reputation — not the AI's.

### Keep it authentic

Prospects can smell generic AI content. The whole point of using AI is to be *more* personalized, not less.

- **Always add a human touch.** Reference something specific: a LinkedIn post they wrote, a comment from your last call, a recent company announcement. AI gives you the structure — you add the substance.
- **Don't automate relationship-building.** AI can help you prepare, but the actual human connection happens in the conversation. Use the time AI saves you to be more present on calls, not to send more volume.
- **Match your voice.** If an AI draft doesn't sound like you, rewrite it until it does. Your prospects know how you write. A sudden shift to robotic prose raises red flags.

### Use approved tools only

- Only use AI tools that your company has approved and vetted. No pasting prospect data into random free AI chatbots you found online.
- If you're unsure whether a tool is approved, check with your IT or security team before using it.
- **Shadow AI is a risk.** Using unapproved tools might feel faster, but it creates security, compliance, and legal exposure that can come back to hurt you and your company.

**The golden rule: AI is a draft, never the final product.** Treat every AI output like a first attempt from a junior rep — good starting material, but it always needs your experience and judgment before it's ready for a prospect.

---

## Quiz

Test your knowledge. Choose the best answer for each question.

---

**Q1: Which of the following is something AI CANNOT do effectively in sales?**

- A) Draft personalized cold outreach emails
- B) Generate objection-handling scripts for common pushback
- C) Read a prospect's emotional state during a live negotiation call ✓
- D) Summarize company research before a discovery call

---

**Q2: An SDR needs to quickly draft 30 personalized cold emails for a new outbound campaign. Which tool is the best starting point?**

- A) Microsoft Copilot in Excel
- B) ChatGPT for rapid email drafts and variations ✓
- C) Copilot in PowerPoint
- D) Gemini for creating slide decks

---

**Q3: You use AI to generate a prospecting email. Before sending, you notice the email references the prospect's "recent Series C funding round." You're not sure this actually happened. What should you do?**

- A) Send it anyway — the prospect will correct you if it's wrong
- B) Remove the reference entirely and send a generic email instead
- C) Verify the information before sending — AI can fabricate details ✓
- D) Add "I believe" before the claim to hedge your bets

---

**Q4: Which of the following should you NEVER include in a prompt to an AI tool?**

- A) Your product's public value proposition
- B) A prospect's job title from LinkedIn
- C) Another customer's negotiated contract pricing ✓
- D) General industry pain points for a target persona

---

**Q5: You've used AI to draft a proposal after a verbal commitment. What's the most important step before sending it to the prospect?**

- A) Run it through a grammar checker
- B) Add your company logo and formatting
- C) Review all pricing, dates, commitments, and deal-specific details for accuracy ✓
- D) Send it immediately to maintain momentum — speed wins deals
