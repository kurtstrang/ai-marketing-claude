# Brand Voice Analysis and Guidelines Generation

## Skill Purpose
Analyze, validate, and operationalize **Moss's** voice, tone, and messaging across Moss-owned channels and generate a comprehensive brand voice guidelines document. This skill does **not** need to discover who the brand is. Moss is already defined here. Use this skill to document how Moss communicates, spot drift from the approved voice, and produce actionable guidelines that any Moss writer, marketer, freelancer, or agency partner can follow to maintain consistency.

## When to Use
- User wants to understand or document **Moss's** voice
- User needs brand voice guidelines for Moss's internal team, freelancers, or agencies
- User wants to ensure consistency across Moss marketing channels
- User is refining Moss messaging, positioning, or editorial standards
- User wants to compare Moss's voice to Moss's default competitive set
- Triggered by `/market brand <url>` or `/market brand`

## How to Execute

### Step 1: Gather Source Material
For this skill, **do not discover the brand from scratch**. The brand is **Moss**.

**Moss core context (source of truth for this skill):**
- **Brand:** Moss
- **Category:** All-in-one spend management platform
- **Primary audience:** Finance teams and finance decision-makers at small and mid-sized companies, especially companies with roughly **30-250 employees** and meaningful indirect spend
- **Primary buyer roles:** CFO, VP Finance, Finance Director, Head of Finance, Finance Manager
- **Primary user roles:** Controller, Accountant, AP Manager, Finance Ops, Office/Operations managers, team leads with budget responsibility
- **Geographic focus:** Germany first, broader Europe and the UK
- **Core promise:** Moss helps finance teams gain **visibility, control, and speed** across cards, invoices, reimbursements, approvals, accounting, and spend workflows
- **Product scope:** Corporate cards, accounts payable / invoice management, reimbursements, approval workflows, purchase controls / procurement, advanced accounting / pre-accounting, advanced controlling / budgets, bank transfers, integrations, and finance automation powered by AI
- **Brand-level messaging anchors:** "Spend smarter.", "free up finance", "The Moss Effect", "Payments, expense claims & invoices, in one powerful platform."
- **Core differentiators to keep in mind:** one integrated platform, strong spend controls before money is spent, faster month-end, AI-supported finance workflows, strong accounting/ERP integrations, privacy/security credibility, Germany/Europe finance credibility
- **Default competitive set for this skill:** **Payhawk, Pleo, Spendesk**
- **Secondary competitor context (only if relevant to the user's request):** Airbase, SAP Concur, Tipalti, Soldo, Coupa

To analyze Moss's voice, examine content from Moss-owned channels in this order:

**Primary Sources (must analyze):**
1. **Homepage** -- The clearest public expression of Moss's positioning and voice
2. **About page** -- How Moss describes its vision, values, and company identity
3. **Product/service pages** -- How Moss presents cards, accounts payable, reimbursements, accounting, controls, and integrations

**Secondary Sources (analyze if available):**
4. **Finance Guide / blog posts** (at least 3-5 recent pieces)
5. **Customer stories / case studies**
6. **LinkedIn content** (company posts, profile copy, campaign language)
7. **Email newsletters / lifecycle emails** (welcome, nurture, activation, sales-assist)
8. **Customer-facing copy** (help docs, onboarding flows, microcopy, error states)

**Tertiary Sources:**
9. **Product announcements**
10. **Press / newsroom pages**
11. **Ad copy / paid landing pages**
12. **Video scripts, webinars, event pages, or podcast transcripts**
13. **Careers pages** -- Useful for tone, but lower priority than product and buyer-facing messaging

Use browser tools or the analyze_page.py script to access web content. If a URL is provided and it is a Moss-owned domain or subdomain, use it to validate current execution of the Moss voice. If the URL is not Moss-owned, treat it as comparison material only; do **not** switch the skill's primary brand away from Moss.

For channel prioritization, default to what actually matters for Moss:
- **Prioritize:** website, product pages, pricing, customer stories, Finance Guide, lifecycle email, LinkedIn, webinars/events, help content
- **De-prioritize by default:** TikTok, Instagram-first creator formats, meme-led consumer channels, and other platforms that are not central to Moss's B2B finance GTM unless the user explicitly provides them

### Step 2: Voice Dimension Analysis
Start from the **Moss baseline below**. Do not "guess" the brand from scratch. Use current Moss source material only to validate or refine these defaults.

#### Dimension 1: Formal <-----> Casual
Where does Moss fall on the formality spectrum?

| Signal | Formal | Casual |
|---|---|---|
| Contractions | Avoids them ("do not", "cannot") | Uses them freely ("don't", "can't") |
| Sentence structure | Complex, longer sentences | Short, punchy sentences |
| Vocabulary | Professional, industry-standard | Conversational, everyday words |
| Greetings | "Dear valued customer" | "Hey there!" |
| Pronouns | Third person ("the company", "one") | First/second person ("we", "you") |
| Humor | Rare or absent | Frequent, natural |
| Slang/colloquialisms | Never | Occasionally or frequently |

**Default Moss score: 4/10**
- Moss is professional and credibility-driven, but it is not stiff, academic, or corporate-jargon heavy.
- Moss usually writes with clarity and confidence, using "you" and "your" naturally.
- Moss should feel **businesslike, modern, and direct**, not bureaucratic or overly chatty.

**Evidence required:** Quote 3-5 specific Moss examples from the source material that support or challenge the baseline.

#### Dimension 2: Serious <-----> Playful
How much levity does Moss inject into its communication?

| Signal | Serious | Playful |
|---|---|---|
| Tone | Authoritative, measured | Light-hearted, fun |
| Metaphors | Rare, conservative | Creative, unexpected |
| Exclamation marks | Rare | Frequent |
| Emoji use | Never | Sometimes or often |
| Wordplay/puns | Never | Enjoys them |
| Error messages | "An error has occurred" | "Oops! Something went sideways" |
| Self-deprecation | Never | Occasionally |

**Default Moss score: 2/10**
- Moss is predominantly serious, operational, and finance-trust oriented.
- Lightness is acceptable in human contexts (customer stories, employer brand, event copy), but the default should stay grounded and controlled.
- Moss should avoid gimmicks, meme language, and overt playfulness in core product or conversion messaging.

#### Dimension 3: Technical <-----> Simple
How much domain expertise does Moss assume in its audience?

| Signal | Technical | Simple |
|---|---|---|
| Jargon | Uses industry terms freely | Avoids or explains all jargon |
| Acronyms | Uses without definition | Spells out on first use |
| Detail level | In-depth explanations | High-level overviews |
| Audience assumption | Expert audience | General audience |
| Data/statistics | Frequent, detailed | Occasional, simplified |
| Examples | Complex, domain-specific | Simple, relatable analogies |

**Default Moss score: 6/10**
- Moss speaks to finance professionals, so some technical vocabulary is natural and credible.
- However, Moss's best-performing external communication makes complex finance operations feel understandable and manageable.
- The voice should be **finance-native but accessible**: precise without becoming dense.

#### Dimension 4: Reserved <-----> Bold
How much personality and confidence does Moss project?

| Signal | Reserved | Bold |
|---|---|---|
| Claims | Hedged ("we believe", "may help") | Direct ("we guarantee", "the best") |
| Opinions | Neutral, balanced | Strong, opinionated |
| Competitive references | Avoids mentioning competitors | Directly compares |
| Personality | Professional, understated | Distinctive, memorable |
| Promises | Conservative | Ambitious |
| Controversy | Avoids | Embraces when aligned with values |

**Default Moss score: 6/10**
- Moss is more confident than cautious, but it is not loud, cocky, or combative.
- Moss should sound certain about product value, operational outcomes, and category point of view.
- Moss should avoid chest-beating language like "revolutionary", "game-changing", or "the world's best" unless it is a verified award or proof point.

### Step 3: Tone Spectrum Mapping

Beyond the four dimensions, map how Moss's tone shifts across different contexts:

| Context | Typical Tone | Example |
|---|---|---|
| Homepage | Confident, outcome-led, clear | Use a quote from the current homepage |
| Product description | Practical, benefit-first, finance-native | Use a quote from the current product pages |
| Finance Guide / blog post | Educational, useful, trustworthy | Use a quote |
| Customer story | Credible, specific, results-led, human | Use a quote |
| LinkedIn / social media | More conversational, still B2B and composed | Use a quote |
| Error/404 page | Helpful, calm, concise | Use a quote if available |
| Email subject lines | Clear, relevant, low-hype | Use a quote |
| CTA buttons | Action-oriented, friction-aware, direct | Use a quote |
| Customer support / help center | Reassuring, practical, low-friction | Use a quote |

Default interpretation for Moss:
- **Homepage:** Confident, benefits-first, modern finance clarity
- **Product pages:** More explicit, operational, use-case oriented
- **Finance Guide:** Educational and trusted, not overly salesy
- **Customer stories:** Proof-rich and outcome-driven
- **LinkedIn:** Slightly more human and current, but still never casual-consumer
- **Lifecycle email:** Clear, helpful, action-led, not overdesigned in tone

### Step 4: Brand Personality Framework

Map Moss to one of five core personality archetypes (brands may blend 1-2):

#### The 5 Archetypes

**1. The Authority**
- Characteristics: Expert, trustworthy, data-driven, established
- Voice: Confident but not arrogant, educational, precise
- Industries: Finance, healthcare, B2B enterprise, legal, consulting
- Example brands: McKinsey, IBM, Mayo Clinic
- Key phrases: "Research shows...", "Our experts...", "Industry-leading..."

**2. The Innovator**
- Characteristics: Forward-thinking, disruptive, visionary, tech-savvy
- Voice: Exciting, future-focused, sometimes provocative
- Industries: Tech, SaaS, startups, renewable energy
- Example brands: Tesla, Stripe, Notion
- Key phrases: "Reimagine...", "The future of...", "We're building..."

**3. The Friend**
- Characteristics: Warm, approachable, helpful, relatable
- Voice: Conversational, empathetic, inclusive, encouraging
- Industries: Consumer products, education, community platforms
- Example brands: Mailchimp, Slack, Duolingo
- Key phrases: "We get it...", "You've got this...", "Here to help..."

**4. The Rebel**
- Characteristics: Bold, challenging conventions, irreverent, passionate
- Voice: Direct, opinionated, sometimes confrontational, memorable
- Industries: Lifestyle, fitness, creative industries, direct-to-consumer
- Example brands: Nike, Oatly, Cards Against Humanity
- Key phrases: "Stop settling for...", "The truth is...", "We're done with..."

**5. The Guide**
- Characteristics: Wise, patient, methodical, trustworthy
- Voice: Clear, instructional, supportive, knowledgeable
- Industries: Education, professional development, tools, platforms
- Example brands: HubSpot, Khan Academy, Ahrefs
- Key phrases: "Here's how to...", "Step by step...", "The complete guide to..."

**Assessment:**
- Primary archetype: **The Authority**
- Secondary archetype: **The Guide**
- Archetype fit: **Strong**
- Why this is Moss:
  - Moss sells into finance, where trust, control, and competence matter
  - Moss simplifies operational complexity, which gives it a strong Guide quality
  - Moss should feel credible first, useful second, innovative third
  - Moss is **not** a Rebel brand, and it is **not** a Friend-first brand

### Step 5: Vocabulary Analysis

Use the Moss vocabulary baseline below. Validate it with current source material and add/remove only where the evidence is strong.

#### Words They Use Frequently
Analyze Moss source material and identify the 15-20 most characteristic words or phrases. Organize by category:

**Action words:** (verbs Moss favors)
- automate
- control
- approve
- reconcile
- simplify
- manage
- issue
- integrate
- capture
- reduce
- customise
- streamline
- sync
- track
- optimise

**Descriptive words:** (adjectives Moss uses)
- smart / smarter
- powerful
- automated
- real-time
- intuitive
- fast / faster
- built-in
- direct
- seamless
- integrated
- efficient
- secure
- scalable

**Value words:** (words that reflect Moss's values)
- visibility
- control
- speed
- efficiency
- clarity
- accuracy
- compliance
- reliability
- impact
- oversight
- trust
- privacy

**Industry-specific terms:**
- spend management
- accounts payable
- reimbursements
- corporate cards
- approvals
- month-end
- accounting
- ERP
- invoice coding
- pre-accounting
- cost centres
- VAT
- budgets
- workflows
- policy controls

#### Words They Avoid
Identify words that are notably absent or that would feel out of character for Moss:

- Overly casual consumer language: "awesome", "super fun", "OMG", "viral", "hustle"
- Empty hype words: "revolutionary", "game-changing", "magic", "best ever", "unicorn"
- Startup chest-thumping: "move fast and break things", "growth hack", "10x everything"
- Finance language that feels intimidating when a simpler alternative exists
- Slang-heavy or meme-heavy internet language
- Cute, jokey phrasing in core conversion copy
- Overblown confrontation against competitors

#### Signature Phrases
Does Moss have any recurring phrases, taglines, or linguistic patterns?

- Tagline: **Spend smarter.**
- Recurring phrases:
  - **free up finance**
  - **The Moss Effect**
  - **Payments, expense claims & invoices, in one powerful platform**
  - **Get started for free**
  - **Book an intro**
- Linguistic patterns:
  - short, clear benefit-led headlines
  - product copy that pairs outcomes with operational detail
  - preference for concrete workflow language over abstract brand flourish
  - compressed, punchy CTA language
  - frequent use of parallel structures in feature/value lists

### Step 6: Competitor Voice Comparison

Compare Moss's voice to 2-3 key competitors using the default Moss competitive set:

**Default competitors for this skill:**
1. **Payhawk**
2. **Pleo**
3. **Spendesk**

Only replace these if the user explicitly asks for a different comparison set or if the page/subcategory clearly requires a more specific competitive frame.

**Voice Comparison Matrix:**
| Dimension | Moss | Payhawk | Pleo | Spendesk |
|---|---|---|---|---|
| Formal <> Casual | 4/10 | Score and assess | Score and assess | Score and assess |
| Serious <> Playful | 2/10 | Score and assess | Score and assess | Score and assess |
| Technical <> Simple | 6/10 | Score and assess | Score and assess | Score and assess |
| Reserved <> Bold | 6/10 | Score and assess | Score and assess | Score and assess |
| Primary Archetype | Authority / Guide | [type] | [type] | [type] |

**Differentiation Assessment:**
- Assess how distinct Moss's voice is from competitors
- Identify where Moss overlaps with peers in the spend-management category
- Identify where Moss can be more ownable
- Default lens for Moss differentiation:
  - Moss should own **finance-native clarity**
  - Moss should sound more **operationally credible** than playful challengers
  - Moss should sound more **modern and useful** than legacy enterprise tools
  - Moss should differentiate on **control + speed + accounting readiness**, not on noise

### Step 7: Consistency Audit

Assess voice consistency across Moss's analyzed channels:

| Channel | Voice Consistency | Notes |
|---|---|---|
| Homepage | Consistent/Mostly/Inconsistent | [specific observations] |
| About page | Consistent/Mostly/Inconsistent | [notes] |
| Product pages | Consistent/Mostly/Inconsistent | [notes] |
| Finance Guide / blog | Consistent/Mostly/Inconsistent | [notes] |
| Customer stories | Consistent/Mostly/Inconsistent | [notes] |
| LinkedIn | Consistent/Mostly/Inconsistent | [notes] |
| Email | Consistent/Mostly/Inconsistent | [notes] |
| Help center / onboarding | Consistent/Mostly/Inconsistent | [notes] |

**Common Consistency Issues to watch for at Moss:**
- Product pages are crisp and confident, but thought-leadership content drifts into generic finance SEO language
- LinkedIn becomes too generic, too soft, or too startup-polished compared to the product truth
- Performance copy becomes too feature-heavy and loses the emotional or operational payoff
- Brand pages become more abstract than conversion pages
- Localised pages drift in tone or precision
- Customer stories become overly polished and lose specificity
- Microcopy or lifecycle messaging feels more mechanical than the site

**Overall Consistency Score:** X/10

### Step 8: Brand Messaging Hierarchy

Document Moss's messaging from most distilled to most expanded:

#### Level 1: Tagline (under 10 words)
The most compressed form of the brand message.
- Current: **"Spend smarter."**
- Assessment: It captures the category promise cleanly, but should always be supported by clearer operational value nearby.

#### Level 2: Value Propositions (1 sentence each)
3-5 core value propositions that support the brand promise.
1. Moss gives finance teams one place to control cards, invoices, reimbursements, approvals, and accounting workflows.
2. Moss prevents out-of-policy spending with built-in controls, approvals, and real-time visibility before money is spent.
3. Moss helps finance teams close the books faster with AI-supported pre-accounting and strong accounting / ERP integrations.
4. Moss reduces admin and gives finance teams time back for higher-value work.
5. Moss combines finance-grade control with a user experience employees and finance teams can actually use.

#### Level 3: Elevator Pitch (30 seconds / 75 words)
A conversational explanation of what Moss does and why it matters.
"Moss is an all-in-one spend management platform built for modern finance teams. It brings cards, invoices, reimbursements, approvals, accounting automation, and integrations into one system, so businesses get more control, better visibility, and a faster month-end. Instead of chasing receipts, fixing manual errors, and stitching together disconnected tools, finance teams can automate the work, stay compliant, and focus on making better decisions."

#### Level 4: Boilerplate (100-150 words)
The standard "about us" paragraph used in press releases, email signatures, and speaker bios.
"Moss is a European spend management platform that helps finance teams gain visibility and control across company spending. Built for small and mid-sized businesses, Moss combines corporate cards, accounts payable, reimbursements, approvals, accounting automation, and integrations in one powerful platform. By reducing manual work and giving teams real-time oversight, Moss helps businesses move faster, stay compliant, and close the books with less effort. Moss is used by thousands of businesses across Europe and is built to make modern finance operations simpler, smarter, and more impactful."

#### Level 5: Full Brand Story (300-500 words)
The complete narrative of who Moss is, what it stands for, and why it exists.
- Current status: **Exists**
- Recommendations for improvement:
  - Keep the story anchored in finance-team pain, not startup mythmaking
  - Connect brand narrative to real operational outcomes
  - Reinforce the "free up finance" idea through concrete examples
  - Use the story to bridge from admin reduction to strategic finance impact

### Step 9: Generate Brand Voice Documentation

Create the comprehensive Do's and Don'ts guide:

#### Voice Chart

```
OUR VOICE IS:                    OUR VOICE IS NOT:
--------------------------------------------------
Confident                        Arrogant

Clear                            Vague

Finance-native                   Needlessly technical

Modern                           Trendy for the sake of it

Helpful                          Hand-holding or fluffy

Direct                           Abrupt

Credible                         Overhyped
```

#### Writing Do's and Don'ts

**DO:**
- Lead with the business outcome or finance problem solved
- Write for finance buyers and users who value clarity, control, and speed
- Use concrete operational language instead of generic SaaS abstractions
- Explain complex processes in simple, precise language
- Use "you" and "your" to keep the copy buyer-relevant
- Connect product features to workflow or reporting outcomes
- Use proof, specifics, and examples whenever possible
- Make CTAs clear, low-friction, and expectation-setting
- Sound like a modern finance operator, not a lifestyle brand
- Keep headlines tight and benefit-led

**DON'T:**
- Don't write like Moss needs to discover its category or audience
- Don't use empty startup hype, buzzwords, or inflated promises
- Don't become overly casual, jokey, or meme-driven
- Don't bury the outcome behind product terminology
- Don't make Moss sound like a generic accounting blog
- Don't overcomplicate copy to sound more "enterprise"
- Don't overuse exclamation marks, superlatives, or dramatic claims
- Don't turn customer proof into vague praise; keep it specific
- Don't make the buyer do interpretive work to understand the value
- Don't write product copy that sounds detached from real finance workflows

### Step 10: Copy Samples in Identified Voice

Provide 5-8 sample copy pieces written in the identified Moss voice so the team has concrete examples to reference:

**1. Homepage Headline:**
"Control every company expense from one platform."

**2. Product Description Paragraph:**
"Moss brings cards, invoices, reimbursements, approvals, and accounting automation together, so finance teams can spend less time fixing manual work and more time moving the business forward."

**3. Finance Guide / Blog Post Opening:**
"Month-end doesn't have to mean chasing receipts, matching invoices by hand, and untangling spreadsheet logic. Here's how finance teams can build a spend process that is faster, cleaner, and easier to control."

**4. Social Media Post:**
"Still managing cards, invoices, and reimbursements in separate systems? That's where visibility gets lost. Moss brings every spend workflow into one place, so finance teams get more control before month-end even starts."

**5. Email Subject Line:**
"Close the books faster with smarter spend controls"

**6. CTA Button Text:**
"Get started for free"

**7. Error Message:**
"We couldn't load this view right now. Please try again in a moment."

**8. Customer Thank You Message:**
"You're all set. Moss is now ready to help your team manage spend with more visibility, control, and less admin."

## Output Format

Generate a file called `BRAND-VOICE.md` with:

```markdown
# Brand Voice Guidelines
## [Brand Name]
### Analysis Date: [Date]

---

## Voice Summary
[2-3 sentence summary of the brand voice, personality, and key characteristics]

---

## Voice Dimensions

### Formal <-----> Casual: [X/10]
[Evidence and explanation]

### Serious <-----> Playful: [X/10]
[Evidence and explanation]

### Technical <-----> Simple: [X/10]
[Evidence and explanation]

### Reserved <-----> Bold: [X/10]
[Evidence and explanation]

### Visual Voice Map
```
Formal                                    Casual
|----[X]----------------------------------|
Serious                                   Playful
|--------[X]------------------------------|
Technical                                 Simple
|------------------[X]--------------------|
Reserved                                  Bold
|------------[X]--------------------------|
```

---

## Brand Personality
- Primary Archetype: [Archetype]
- Secondary Archetype: [Archetype]
- [Explanation and evidence]

---

## Tone by Context
| Context | Tone | Example |
|---|---|---|
| [context] | [tone] | "[example]" |

---

## Vocabulary

### Words We Use
[Organized word lists]

### Words We Avoid
[Words that don't fit the brand]

### Signature Phrases
[Recurring patterns and phrases]

---

## Voice Chart
| Our Voice IS | Our Voice IS NOT |
|---|---|
| [trait] | [anti-trait] |

---

## Writing Guidelines

### Do's
- [specific guidelines]

### Don'ts
- [specific anti-patterns]

---

## Brand Messaging Hierarchy

### Tagline
[tagline]

### Value Propositions
1. [value prop]

### Elevator Pitch
[pitch]

### Boilerplate
[boilerplate]

---

## Copy Samples
[8 examples of copy in the brand voice]

---

## Competitor Voice Comparison
[Comparison matrix and differentiation analysis]

---

## Consistency Audit
[Channel-by-channel assessment]
- Overall Consistency Score: [X/10]

---

## Recommendations
### Immediate Actions
1. [recommendation]

### Voice Evolution Opportunities
1. [recommendation]

### Consistency Improvements
1. [recommendation]
```

## Key Principles
- This is a **Moss-specific** skill. Do not spend time "discovering" who the brand is. Start from the Moss context above and validate against current Moss-approved source material.
- Brand voice analysis still requires reading like a detective. Every word choice, punctuation decision, and sentence structure reveals whether Moss is executing its intended voice or drifting from it.
- Always provide EVIDENCE for every assessment. Don't just say "Moss is clear and confident" -- quote specific examples that prove it.
- The brand voice guide should be usable by someone who has never worked with Moss before. A new copywriter should be able to read this document and write on-brand content.
- Copy samples are the most valuable part of the deliverable. People learn voice by example, not by description. Make the samples diverse (headlines, body copy, social, email, error messages) so writers have references for every context.
- Voice and tone are different. Moss's **voice** should stay consistent; the **tone** can shift depending on whether the context is homepage copy, a Finance Guide article, a product page, or customer support.
- If Moss's voice is inconsistent across channels, frame it as an opportunity to strengthen the brand, not as a failure.
- If the user has run `/market competitors` previously, use that data for the competitor voice comparison section -- but default back to **Payhawk, Pleo, and Spendesk** if nothing else is available.
- The voice dimensions should be plotted visually (text-based spectrum) so stakeholders can quickly understand the positioning at a glance.
- Moss should generally sound like: **a trusted finance operator who knows the work, simplifies the complexity, and helps businesses move faster with more control.**
