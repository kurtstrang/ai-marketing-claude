# Moss Proposal Generator for Spend Management

## Skill Purpose
Generate a professional, client-ready Moss spend management proposal. This skill produces a complete proposal document that positions Moss as the clear choice, frames pricing with anchoring and tiered options, and includes ROI projections to justify the investment.

## When to Use
- User wants to create a proposal for a prospective Moss customer
- User has completed a discovery call and needs to formalize the engagement
- User wants a template for Moss commercial proposals
- Triggered by `/market proposal` or `/market proposal <client name>`

## How to Execute

### Step 1: Gather Proposal Inputs
Collect these details from the user (ask if not provided):

**About the Client:**
1. Client name and company
2. Industry, business model, and whether they operate one entity or multiple entities
3. Current spend management situation (cards, invoices/AP, reimbursements, budgets, approvals, accounting exports, ERP/accounting stack)
4. Primary pain points or challenges
5. Goals (control, visibility, automation, faster close, policy compliance, reduced manual work, employee autonomy)
6. Budget range (if known)
7. Decision timeline
8. Key stakeholders and decision-makers

**Hardcoded Moss context to use by default:**
- Moss is a spend management platform built for finance teams that want visibility, control, and automation across company spend.
- Moss' core modules are corporate cards, invoice management / accounts payable, employee reimbursements, budget control, integrations, and accounting automation.
- Moss is strongest when the buyer needs one platform across cards, invoices, reimbursements, approvals, and accounting workflows rather than a patchwork of tools.
- Moss' typical best-fit customer is a European SME / medium-sized company with roughly 30-250 employees and meaningful indirect spend.
- Common strong-fit industries include agencies, software / SaaS, IT services, professional services, e-commerce operators, and multi-entity growth companies.
- Moss' core buying committee usually includes CFO, Head of Finance, Finance Manager, Controller, Accounting lead, and sometimes Operations or IT.
- Moss' default brand voice is clear, confident, practical, finance-literate, and low-fluff. Write like a trusted finance operator, not a generic marketer.

**About the Services:**
1. Which Moss modules are you proposing? (Corporate Cards, Invoice Management / Accounts Payable, Reimbursements, Budget Control, Integrations, Accounting Automation)
2. Commercial model (platform subscription, implementation fee, phased rollout, multi-entity expansion)
3. Proposed timeline
4. Relevant Moss case studies, customer stories, proof points, or public results

**If audit data exists:** Check for any previous `/market audit` results. If found, automatically incorporate the findings into the Situation Analysis section for a data-backed proposal.

### Step 2: Discovery Call Question Framework
If the user hasn't had the discovery call yet, provide these 10 essential questions:

**Business Understanding:**
1. "Walk me through your business model, entity structure, and how spend is managed today."
2. "Which teams spend company money most often, and what kinds of indirect spend are hardest to control?"
3. "What does your current process look like from request or purchase through approval, reconciliation, and export into accounting?"

**Current Marketing:**
4. "What tools are you using today for cards, invoice handling, reimbursements, approvals, and accounting?"
5. "What is the current cost of the status quo in time, delays, policy breaches, reconciliation effort, or missed visibility?"
6. "What ERP, accounting, HR, or finance tools need to stay in the stack?"

**Goals and Expectations:**
7. "If we're wildly successful, what does that look like in 6 months? 12 months?"
8. "What specific numbers are you trying to hit? (Hours saved, faster month-end close, more spend under policy, fewer reimbursement delays, fewer manual touches)"
9. "What is the size of the opportunity for this project? (Monthly spend, invoice volume, number of cardholders, reimbursement volume, entities, finance team size)"

**Decision and Process:**
10. "Who else is involved in this decision, and what's your timeline for choosing a partner?"

**Bonus Questions:**
- "What's your biggest frustration with spend control or finance ops right now?"
- "Have you used a spend management tool before? What went well or poorly?"
- "Is there anything that would make you say 'no' to working with Moss?"

### Step 3: Build the Proposal Document

#### Section 1: Cover Page
```
[Moss Logo]

Spend Management Proposal
Prepared for: [Client Name]
Prepared by: [Moss Team]
Date: [Date]
Valid until: [Date + 30 days]

CONFIDENTIAL
```

#### Section 2: Executive Summary (1 page max)
Write a concise summary that:
- Acknowledges the client's current finance operations and goals
- States the core spend-management problem Moss will solve
- Previews the recommended Moss module mix and rollout approach
- Hints at the expected business outcome
- Creates urgency to act

**Template:**
```
[Client Name] is at an inflection point. With [current situation -- e.g., disconnected cards, invoice processing, and reimbursements creating manual finance work and weak spend visibility], there's a significant opportunity to [desired outcome -- e.g., centralize company spend, enforce policy before money is spent, and reduce month-end effort].

Based on our analysis of [what you reviewed -- their workflows, current tools, approval structure, accounting setup, and competitive options], we've identified [X] key areas where strategic improvements could drive [specific result -- e.g., faster reconciliation, stronger spend control, and measurable time savings within 3-6 months].

This proposal outlines a [timeframe] engagement focused on [primary Moss modules], designed to [primary outcome]. Our approach is built on [Moss differentiator -- e.g., unified cards + AP + reimbursements + accounting automation, strong finance controls, proven rollout support, and best-in-class integrations].

We recommend beginning with [first phase] to establish baselines and quick wins, then scaling usage based on performance data and adoption.
```

#### Section 3: Situation Analysis (2-3 pages)
Present your analysis of the client's current spend management setup. This is where audit data from `/market audit` is invaluable.

**Structure:**
1. **Current State Overview** -- What they're doing now across cards, invoices, reimbursements, budgets, approvals, and accounting exports
2. **Opportunities Identified** -- Specific areas where control, visibility, automation, or speed can improve
3. **Competitive Landscape** -- How they compare to alternatives and the status quo. Default Moss comparison set: manual processes / spreadsheets + bank cards, Pleo, Spendesk, Payhawk, and SAP Concur. Emphasize where Moss wins: deeper control, stronger accounting automation, and one unified platform across cards, AP, reimbursements, and approvals.
4. **Key Challenges** -- Obstacles that need to be addressed (change management, integrations, approval design, rollout scope, multi-entity complexity)
5. **Market Context** -- Industry trends and benchmarks in spend management, finance automation, compliance, and efficiency for SMEs

**Important:** Frame everything as opportunities, not failures. The client should feel understood, not criticized.

Good: "Your finance team currently reconciles cards, invoices, and reimbursements across multiple tools. We see a clear path to reduce manual effort, increase policy compliance, and give the business real-time visibility with a phased Moss rollout."

Bad: "Your finance process is broken and needs to be replaced."

#### Section 4: Strategy and Approach (2-3 pages)
Present your recommended strategy. Be specific enough to demonstrate expertise but not so detailed that they could execute the rollout without Moss.

**Structure:**
1. **Strategic Framework** -- Your overall approach and methodology. Use a Moss-specific framework: control first, automate second, scale third.
2. **Phase 1: Foundation** (Month 1-2) -- Process mapping, module scoping, stakeholder alignment, integration review, approval policy design, quick wins
3. **Phase 2: Growth** (Month 3-4) -- Launch core modules, onboard users, optimize approval flows, improve finance adoption, reduce manual work
4. **Phase 3: Scale** (Month 5-6) -- Expand to more teams, entities, use cases, and higher-value automations; increase adoption of winning workflows
5. **Ongoing: Optimize** -- Continuous improvement, reporting, governance, and success planning

For each phase, include:
- Specific activities and deliverables
- Expected outcomes
- How success will be measured

#### Section 5: Scope of Work (1-2 pages)
Detail exactly what is included (and what is not).

**Include:**
- Specific deliverables with quantities (e.g., "1 solution design workshop, 1 rollout plan, 2 admin enablement sessions, 1 finance training session, integration scoping for [X] systems")
- Meeting cadence (e.g., "Weekly implementation working sessions during rollout, monthly business reviews post-launch")
- Response time commitments (e.g., "Commercial follow-up within 1 business day, agreed implementation cadence during onboarding")
- Moss modules, add-ons, and integrations included
- Reporting format and frequency

**Explicitly Exclude:**
- Items outside scope to prevent scope creep
- Custom product development, bespoke connectors, or unsupported integrations unless separately agreed
- Legal, security, procurement, or IT work that must be completed on the client's side
- Assumptions about client responsibilities

**Client Responsibilities Section:**
List what you need from the client to be successful:
- Timely feedback and approvals (specify SLA)
- Access to current tools, workflows, and relevant data
- Designated point of contact
- Timely review of security, legal, and procurement materials within X business days
- Internal rollout support for admins, approvers, finance, and end users

#### Section 6: Timeline (1 page)
Visual timeline showing phases, milestones, and deliverables.

```
Month 1    | Month 2    | Month 3    | Month 4    | Month 5    | Month 6
-----------|------------|------------|------------|------------|----------
FOUNDATION | FOUNDATION | GROWTH     | GROWTH     | SCALE      | SCALE
Discovery &| Quick wins | Launch     | Optimize   | Expand     | Full
Setup      | & baselines| core flows | & iterate  | winners    | rollout

Key Milestones:
- Week 2: Complete workflow discovery and recommended solution design
- Week 4: Confirm rollout scope, integrations, and approval policy setup
- Month 2: First module(s) live or pilot users onboarded
- Month 3: Adoption and optimization recommendations
- Month 6: Comprehensive review and expansion roadmap
```

#### Section 7: Investment (1-2 pages)
Present pricing using the Good-Better-Best tier structure.

**Three-Tier Pricing Model:**

| Component | Control | Automate | Unify |
|---|---|---|---|
| Corporate Cards | Core card program | Cards + policy controls | Full company-wide card rollout |
| Invoice Management / AP | -- | Included | Included + advanced workflows |
| Reimbursements | Basic | Included | Included |
| Budget Control | Team-level | Department-level | Multi-team / multi-entity |
| Accounting Automation | Standard exports | Enhanced automation | Advanced automation + deeper finance ops |
| Integrations | Standard accounting integration | Multiple integrations | Advanced integration scope |
| Onboarding | Standard onboarding | Guided rollout | Multi-phase rollout |
| Reporting / Reviews | Monthly review | Bi-weekly review | Strategic review cadence |
| **Monthly / Annual Investment** | **[Use approved Moss pricing]** | **[Use approved Moss pricing]** | **[Use approved Moss pricing]** |

**Pricing Psychology Tips:**
- Present three options; most clients choose the middle tier
- Name the tiers with outcome-driven labels (not Bronze/Silver/Gold)
- Anchor the most complete option first to make the middle tier feel reasonable
- Include a "Most Popular" or "Recommended" badge on the middle tier when justified
- Show the math: "At [estimated monthly finance time saved or spend reduction], you only need [X] efficiency gain to justify the investment"

**Pricing Models Reference:**

| Model | When to Use | Typical Range |
|---|---|---|
| Platform Subscription | Standard Moss commercial motion | Use current approved regional pricing only |
| Platform + Implementation | New rollouts with onboarding and setup complexity | Use approved quote only |
| Multi-Entity / Advanced Scope | Multi-entity, larger process complexity, advanced finance requirements | Use approved quote only |
| Phased Rollout | Lower-risk start or budget-constrained rollout | Use approved quote only |
| Partner / Referral Motion | Accountant, advisor, consultant, or channel-led opportunity | Use approved partner commercial terms only |

#### Section 8: ROI Projection
Show the client the expected return on their investment.

**ROI Calculation Framework:**
```
Current State:
- Monthly company spend: [X]
- Monthly invoice volume: [X]
- Number of cardholders / spenders: [X]
- Current finance admin hours/month: [X]
- Current month-end close time: [X]
- Current reimbursement turnaround time: [X]
- Current monthly cost of manual finance operations / leakage: [X]

Projected State (6 months):
- Projected reduction in manual processing time: [X%] -> [new hours/month]
- Projected increase in spend under policy: [X%]
- Projected faster close or reconciliation cycle: [X days/hours]
- Projected savings from reduced leakage / duplicate / uncontrolled spend: [X]/month
- Projected capacity freed for finance team: [X hours or FTE equivalent]
- 6-month projected ROI: [X]x

Investment: [total 6-month or 12-month cost]
Projected Return: [projected savings + efficiency value]
ROI: [X]x return
```

**Important:** Be conservative with projections. Under-promise and over-deliver. Use ranges rather than specific numbers. Add disclaimers that results depend on rollout quality, adoption, stakeholder engagement, and the client's starting point. Never invent Moss pricing or promise unsupported outcomes.

#### Section 9: Team (0.5-1 page)
Introduce the team members who will work on this account.

For each team member:
- Name and title
- Relevant experience and expertise
- Role on this engagement
- Brief bio (2-3 sentences max)

Default Moss team structure to use unless the user provides a different one:
- Account Executive / Commercial Lead
- Solutions Engineer or Product Specialist
- Implementation / Onboarding Manager
- Customer Success Manager or Account Manager

#### Section 10: Case Studies (1-2 pages)
Include 2-3 relevant case studies that demonstrate results similar to what you're promising.

Prioritize public Moss customer stories that match the client's industry, size, and pain points. Strong default use cases include:
- Agencies / services firms with distributed spend and project-based purchasing
- SaaS / tech companies with subscriptions, travel, and employee card needs
- Finance teams managing reimbursements, approvals, and reconciliation across multiple departments
- Multi-entity or scaling teams that need visibility and control without adding headcount

Use only approved/public proof. If exact figures are unavailable or unapproved, anonymize and use directional outcomes.

**Case Study Format:**
```
Client: [Industry and company type -- anonymize if needed]
Challenge: [1-2 sentences about their situation]
Solution: [1-2 sentences about the Moss modules and rollout approach]
Results:
- [Specific metric 1: e.g., "Reduced transaction processing time by 30%"]
- [Specific metric 2: e.g., "Saved approximately one week per month in reconciliation effort"]
- [Specific metric 3: e.g., "Improved visibility, policy compliance, or reimbursement turnaround"]
```

#### Section 11: Next Steps (0.5 page)
Make it crystal clear what happens next. Reduce friction.

```
Ready to move forward? Here's what happens next:

1. Sign this proposal or confirm your preferred option
2. We'll schedule a kickoff / solution alignment call within 48 hours
3. You'll receive the onboarding checklist, access requests, and implementation plan
4. We begin the Foundation phase immediately

Questions? Contact [Name] at [email] or [phone].

This proposal is valid until [date -- 30 days from now].
```

### Step 4: Proposal Design and Formatting

**Best Practices:**
- Keep total proposal under 15 pages (excluding appendix)
- Use consistent headers, fonts, and Moss brand styling throughout
- Include the client's logo alongside the Moss logo on the cover page
- Use charts, workflows, screenshots, and visuals instead of dense text wherever possible
- Bold key numbers and outcomes
- Use whitespace generously -- don't cram content
- Include page numbers and a table of contents for longer proposals
- Save as PDF for professional presentation

**Formatting in Markdown:**
- Use H1 for the proposal title
- Use H2 for major sections
- Use H3 for subsections
- Use tables for pricing, timelines, and comparisons
- Use bold for emphasis on key points
- Use blockquotes for client testimonials

### Step 5: Follow-Up Sequence After Sending

**Day 0 (Send Day):**
Send proposal via email with a brief cover note. Subject: "Your Moss Spend Management Proposal -- [Client Name]"

**Day 2:**
Follow-up email: "I wanted to make sure you received the proposal. Happy to hop on a quick call to walk through it if that would be helpful."

**Day 5:**
Value-add follow-up: Share a relevant Moss customer story, product tour, integration page, or finance insight related to their use case. Softly reference the proposal.

**Day 7:**
Direct follow-up: "I'd love to hear your thoughts on the proposal. Do you have any questions I can address? I'm available [specific times] this week for a call."

**Day 14:**
Final follow-up: "I wanted to check in one more time about the proposal. I understand timing may not be right -- if that's the case, I'm happy to reconnect when it makes sense. Otherwise, I'd love to discuss next steps."

**Day 21:**
Breakup email: "I haven't heard back, so I'll assume the timing isn't right. I'll close out this proposal on [expiration date]. If things change, my door is always open. Wishing you and [Company] the best."

### Step 6: Objection Handling

Prepare responses for common client pushbacks:

| Objection | Response Framework |
|---|---|
| "Too expensive" | Reframe as investment, show ROI math tied to finance time saved, control gained, and cost of poor spend visibility, offer phased rollout where appropriate |
| "We can do this in-house" | Highlight opportunity cost, complexity of stitching together cards + AP + reimbursements + approvals, speed to value, and the hidden cost of manual finance ops |
| "We tried this before and it didn't work" | Ask what specifically didn't work, differentiate Moss on unified workflows, finance controls, accounting automation, and structured rollout support |
| "We need to think about it" | Set a specific follow-up date, offer to address specific concerns, provide relevant proof points or customer stories |
| "Can you guarantee results?" | Explain why guarantees are unrealistic because results depend on rollout and adoption, but share historical/public proof and provide conservative ROI ranges |
| "We're talking to other vendors" | Welcome it, differentiate on methodology and platform depth rather than price alone, emphasize finance control, accounting automation, and fit for their process complexity |
| "The timeline is too long" | Explain why shortcuts create adoption and data-quality problems, offer a quick-wins phase, and show the phased approach with early value |
| "We don't have the budget right now" | Offer a smaller starting module mix, phased rollout, or delayed expansion, and show the cost of waiting |

### Step 7: Terms and Conditions Essentials

Include these in the proposal appendix or as a separate document:

1. **Payment Terms:** Net terms, payment methods, billing cadence, late payment policies
2. **Contract Duration:** Minimum commitment period, renewal terms, rollout period
3. **Cancellation Policy:** Required notice period, exit process
4. **Scope Changes:** Process for handling additional modules, entities, integrations, or services
5. **Intellectual Property:** Platform ownership, usage rights, implementation materials, license terms
6. **Confidentiality:** NDA terms, data handling, DPA/security documentation references
7. **Liability Limitations:** Caps on liability, force majeure
8. **Reporting and Communication:** Agreed cadence and format
9. **Third-Party Costs:** Client responsibility for any third-party systems, payment costs, or implementation dependencies outside Moss scope
10. **Results Disclaimer:** Outcomes are not guaranteed; projections depend on adoption, rollout, process maturity, and other factors

## Output Format

Generate a file called `CLIENT-PROPOSAL.md` with:

```markdown
# Marketing Services Proposal

## Prepared for: [Client Name]
## Prepared by: [Agency Name]
## Date: [Date]

---

## Table of Contents
1. Executive Summary
2. Situation Analysis
3. Strategy & Approach
4. Scope of Work
5. Timeline
6. Investment
7. ROI Projection
8. Our Team
9. Case Studies
10. Next Steps

---

[Full proposal content with all sections populated based on client details]

---

## Appendix
- Terms & Conditions
- Detailed Deliverable Descriptions
- Tool Stack
```

## Key Principles
- The proposal is a sales document, not a statement of work. It should SELL, not just describe.
- Lead with the client's finance and spend-control problems and goals, not your product features. Make them feel understood before presenting solutions.
- Every price should be anchored to the ROI it will generate. Never present cost without context.
- Use the client's own language from the discovery call. Mirror their words back to them.
- If audit data is available from previous skills, use it extensively -- data-backed proposals close at a much higher rate than generic proposals.
- Keep it concise. Finance leaders skim. Use bold, headers, and tables to make key information scannable.
- Always include a specific, time-bound next step. Ambiguity kills deals.
- Never invent Moss pricing, packaging, timelines, integrations, security claims, or case-study results. Use approved materials or clearly marked placeholders.
