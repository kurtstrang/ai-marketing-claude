# Marketing Report Generator (Markdown Format)

## Skill Purpose
Generate a comprehensive, professionally formatted Moss marketing report in Markdown. This skill compiles data from all previous audit and analysis results into a single, leadership-ready document with scores, findings, recommendations, and a prioritized action plan tied to qualified pipeline, new ARR, and conversion impact for Moss.

## When to Use
- User wants a full marketing report for Moss
- User has completed one or more audit skills and wants a compiled Moss report
- User asks for a Moss marketing assessment, scorecard, or analysis document
- Triggered by `/market report` or `/market report <domain>`

## How to Execute

### Step 1: Collect All Available Data
Before generating the report, check for any existing audit data from previous skill runs. Look for these files in the project directory:

**Possible data sources:**
- `MARKETING-AUDIT.md` -- from `/market audit`
- `LANDING-CRO.md` -- from `/market landing`
- `SEO-AUDIT.md` -- from `/market seo`
- `BRAND-VOICE.md` -- from `/market brand`
- `COMPETITOR-ANALYSIS.md` -- from `/market competitors`
- `FUNNEL-ANALYSIS.md` -- from `/market funnel`
- `CONTENT-AUDIT.md` -- from content analysis
- `AD-AUDIT.md` -- from `/market ads`
- `SOCIAL-AUDIT.md` -- from `/market social`
- `EMAIL-AUDIT.md` -- from `/market emails`

If no previous data exists, do **not** ask the agent to discover who Moss is. Use Moss's hardcoded operating context as the default foundation of the report:

**Moss context to assume by default**
- Moss is a European spend management platform for growing SMBs and mid-market companies, with a strong fit for businesses roughly in the 30-250 employee range and meaningful indirect spend.
- Moss sells primarily to finance teams: CFOs, finance leads, finance managers, accountants, controllers, and operations/people leaders who influence spend workflows.
- Moss's core product areas are: corporate cards, accounts payable / invoice management, reimbursements, procurement / purchase controls, budget control / advanced controlling, advanced accounting / AI-powered pre-accounting, bank transfers / pay runs, and integrations.
- Moss's primary business outcomes are: tighter spend control, faster month-end, less manual admin, cleaner accounting data, and better visibility before and after spend happens.
- Moss's core regions and localisation considerations are Europe-first, especially Germany, the UK, the Netherlands, and adjacent EU markets. International SEO, localisation quality, and cross-locale consistency matter.
- Moss's primary conversion paths are demo / intro booking, free-start or product-tour style journeys where available, and high-intent content paths that move finance buyers toward a sales conversation.
- Moss's default comparison set is Payhawk, Pleo, and Spendesk. Bring in Airbase, Tipalti, Coupa, SAP Concur, Ramp, or other alternatives only when the use case, geography, or company size clearly makes them more relevant.
- Moss's default proof assets include customer stories, finance-team use cases, software integrations, security / trust content, regulatory credibility, and third-party review credibility (for example G2, Capterra, app ratings, and similar proof).
- Moss's primary owned demand channels are the website, SEO, lifecycle email, paid search, paid social, webinars / events, and thought-leadership distribution.
- Moss's primary social focus is LinkedIn. YouTube and webinar/event distribution are secondary. Instagram is supportive for employer brand and light brand distribution. Do not prioritise TikTok or consumer-style social plays for Moss unless the user explicitly requests them and gives a business case.

If no previous data exists, inform the user and offer to:
1. Generate a Moss report from the available live-site and user-provided information
2. Generate a Moss report from existing analytics / CRM / ad platform exports
3. Create a Moss reporting template they can fill in later

### Step 2: Calculate the Marketing Scorecard

Score across 6 categories, each worth up to 100 points. The overall score is the weighted average.

#### Category 1: Website & Conversion (Weight: 25%)
Evaluate Moss's core conversion experience across homepage, product overview, category pages, pricing, customer stories, integrations, campaign landing pages, and demo / product-tour flows.

| Factor | Points Available | Criteria |
|---|---|---|
| ICP and value proposition clarity | 20 | Immediately clear to finance buyers = 20, Mostly clear = 13, Generic SaaS messaging = 7, Unclear = 0 |
| Product architecture and use-case clarity | 15 | Clear path from cards/AP/reimbursements/accounting/integrations to fit = 15, Mostly clear = 10, Fragmented = 5, Confusing = 0 |
| CTA strategy and funnel fit | 20 | Strong CTA hierarchy for book intro / get started / product tour = 20, Present but inconsistent = 12, Weak = 5, Missing = 0 |
| Trust, proof, and risk reduction | 15 | Strong proof mix and finance trust signals = 15, Adequate = 10, Thin = 5, Weak = 0 |
| Form and lead-capture friction | 15 | Low friction and role-appropriate = 15, Acceptable = 10, Friction-heavy = 5, Broken = 0 |
| UX, performance, and localisation consistency | 15 | Fast, polished, and consistent across devices/locales = 15, Mostly solid = 10, Noticeable issues = 5, Severe issues = 0 |

#### Category 2: SEO & Organic (Weight: 20%)
Evaluate Moss's ability to win and convert high-intent organic demand across brand, category, comparison, integration, and finance-education search themes.

| Factor | Points Available | Criteria |
|---|---|---|
| Category and solution-page coverage | 20 | Strong coverage for high-intent spend-management use cases = 20, Good = 13, Patchy = 7, Weak = 0 |
| International SEO and localisation | 15 | Strong hreflang / locale mapping / local relevance = 15, Mostly correct = 10, Needs work = 5, Weak = 0 |
| Content quality and finance credibility (E-E-A-T) | 20 | Strong finance credibility and practical depth = 20, Good = 13, Generic = 7, Weak = 0 |
| Internal linking to money pages | 15 | Finance Guide / integrations / stories support product conversion well = 15, Adequate = 10, Minimal = 5, None = 0 |
| Technical SEO and crawl health | 15 | No major issues = 15, Minor issues = 10, Major issues = 5, Critical = 0 |
| Organic conversion path quality | 15 | Organic visitors are moved clearly to demo / product intent = 15, Reasonable = 10, Weak = 5, Poor = 0 |

#### Category 3: Content & Messaging (Weight: 15%)
Evaluate how well Moss communicates differentiation, finance outcomes, and market authority.

| Factor | Points Available | Criteria |
|---|---|---|
| Brand voice consistency | 15 | Clear, credible, practical, finance-literate throughout = 15, Mostly consistent = 10, Mixed = 5, Weak = 0 |
| Persona targeting | 20 | Speaks directly to CFO / finance lead / accountant / controller needs = 20, Good = 13, Broad = 7, Off-target = 0 |
| Differentiation vs alternatives | 20 | Clear why Moss over Payhawk / Pleo / Spendesk / status quo = 20, Somewhat clear = 13, Weak = 7, Missing = 0 |
| Outcome-focused copy quality | 20 | Strong link from pain to control / automation / faster close = 20, Good = 13, Generic = 7, Weak = 0 |
| Proof density and specificity | 15 | Strong claims supported by evidence, examples, and customer proof = 15, Adequate = 10, Light = 5, Weak = 0 |
| Content mix across funnel stages | 10 | Good mix of product, proof, education, events, and comparisons = 10, Some mix = 6, Limited = 3, Thin = 0 |

#### Category 4: Social Media & Community (Weight: 15%)
Evaluate Moss's social presence based on channels that actually matter for B2B finance demand generation and thought leadership.

| Factor | Points Available | Criteria |
|---|---|---|
| Platform focus and fit | 20 | Strong emphasis on LinkedIn and relevant supporting channels = 20, Mostly right = 13, Too scattered = 7, Poor fit = 0 |
| Content quality and thought leadership | 25 | Strong finance / spend-management content and clear expertise = 25, Good = 17, Adequate = 10, Weak = 0 |
| CTA and website alignment | 15 | Social content supports clear next steps into Moss offers = 15, Mostly aligned = 10, Loose = 5, Poor = 0 |
| Repurposing and posting consistency | 15 | Consistent cadence with reusable content system = 15, Some consistency = 10, Sporadic = 5, Weak = 0 |
| Engagement relevance | 15 | Engagement from the right audience and discussions = 15, Adequate = 10, Low-value engagement = 5, Weak = 0 |
| Community and event leverage | 10 | Good use of webinars, events, ambassadors, and customer voices = 10, Some use = 6, Minimal = 3, None = 0 |

#### Category 5: Email & Automation (Weight: 15%)
Evaluate Moss's lead nurture, lifecycle education, and conversion assistance for finance buyers.

| Factor | Points Available | Criteria |
|---|---|---|
| Lead capture mechanisms | 15 | Strong mix of guides, events, product interest capture, and demo follow-up = 15, Good = 10, Limited = 5, Weak = 0 |
| Segmentation by role, stage, and market | 20 | Strong segmentation = 20, Good = 13, Basic = 7, Weak = 0 |
| Nurture sequence quality | 25 | Clear journeys from interest to demo / product understanding = 25, Good = 17, Basic = 10, Weak = 0 |
| Product education and proof in email | 15 | Strong use of proof, objections, and workflow education = 15, Adequate = 10, Light = 5, Weak = 0 |
| Lifecycle and expansion support | 15 | Good onboarding / activation / cross-sell / retention logic = 15, Some support = 10, Limited = 5, None = 0 |
| Deliverability and operational hygiene | 10 | Strong = 10, Adequate = 7, Concerning = 3, Weak = 0 |

#### Category 6: Paid Advertising (Weight: 10%)
Evaluate paid demand generation for Moss with an emphasis on channel fit and revenue contribution.

| Factor | Points Available | Criteria |
|---|---|---|
| Channel strategy fit | 20 | Strong use of search and B2B social with clear purpose by channel = 20, Good = 13, Mixed = 7, Weak = 0 |
| Campaign structure and intent capture | 20 | Well-structured by use case / market / funnel stage = 20, Good = 13, Messy = 7, Weak = 0 |
| Targeting quality | 20 | Strong audience, keyword, and company-fit logic = 20, Good = 13, Broad = 7, Wasteful = 0 |
| Creative and offer quality | 20 | Strong message match and offers for demos, tours, guides, or events = 20, Adequate = 13, Weak = 7, Poor = 0 |
| Tracking and CRM attribution | 20 | Strong end-to-end attribution into pipeline / ARR = 20, Good = 13, Partial = 7, Weak = 0 |

#### Overall Score Calculation
```
Overall Score = (Website * 0.25) + (SEO * 0.20) + (Content * 0.15) + (Social * 0.15) + (Email * 0.15) + (Paid * 0.10)
```

**Score Interpretation:**
| Score Range | Rating | Meaning |
|---|---|---|
| 85-100 | Excellent | Moss marketing is a competitive advantage. Optimise, replicate, and scale. |
| 70-84 | Good | Moss has a strong foundation with clear commercial upside in specific gaps. |
| 55-69 | Average | Moss marketing works, but too much demand or trust is being left on the table. |
| 40-54 | Below Average | Multiple growth surfaces need attention. Opportunity cost is meaningful. |
| 0-39 | Critical | Moss marketing is underperforming against the market. Immediate prioritisation required. |

### Step 3: Write Category Deep-Dives

For each of the 6 categories, provide:

1. **Score and Rating** -- X/100 with interpretation
2. **Key Findings** -- 3-5 specific observations with evidence
3. **What's Working** -- Positive elements to preserve and build on
4. **Gaps and Issues** -- Problems identified with severity ratings
5. **Recommendations** -- Specific, actionable improvements ranked by impact
6. **Revenue Impact Estimate** -- Estimated financial impact of implementing recommendations

**Revenue Impact Estimation Framework:**
For Moss, prefer a qualified-demand and ARR model over a simple ecommerce revenue model.

```
Impact = (Estimated additional qualified visits or lead volume * Demo/primary conversion rate change * Opportunity creation rate * Win rate * Average ARR or first-year deal value) * Confidence factor

Example:
- Current monthly high-intent sessions: 20,000
- Recommended SEO/CRO improvements could add 3,000 qualified visits
- Current demo / primary conversion rate: 2.0%
- Improved rate after changes: 2.5%
- Additional demo-equivalent conversions: +135/month
- Opportunity creation rate: 35%
- Win rate: 25%
- Average ARR or first-year revenue: €12,000
- Estimated steady-state revenue impact: €141,750 in additional new ARR / first-year revenue generated per month of performance
- Confidence factor (conservative): 0.5
- Conservative estimate: €70,875/month equivalent in additional new ARR / first-year revenue
```

If Moss-specific sales metrics are available, always use actual Moss benchmarks instead of generic assumptions.

### Step 4: Competitor Comparison Summary
If competitor data is available from `/market competitors`, include:

**Competitive Positioning Matrix:**
Use Moss as the reference brand. Default competitors are:
- Payhawk
- Pleo
- Spendesk

If the market context clearly requires a different set, explain the swap.

| Factor | Moss | Competitor 1 | Competitor 2 | Competitor 3 |
|---|---|---|---|---|
| Website Quality | X/10 | X/10 | X/10 | X/10 |
| Positioning Clarity | X/10 | X/10 | X/10 | X/10 |
| Product Breadth | X/10 | X/10 | X/10 | X/10 |
| Proof & Trust | X/10 | X/10 | X/10 | X/10 |
| Overall Position | Xth/4 | Xth/4 | Xth/4 | Xth/4 |

**Competitive Advantages:** Where Moss is stronger
**Competitive Gaps:** Where competitors outperform Moss
**Opportunities:** White space Moss can own in positioning, proof, content, or conversion paths

### Step 5: Content Quality Assessment
Summarize content findings across all channels:

- **Website copy** -- Clarity, differentiation, persuasive strength, finance-buyer fit
- **Finance Guide / editorial content** -- Depth, expertise, SEO alignment, conversion support
- **Social media content** -- LinkedIn-first thought leadership quality, YouTube/event support, platform fit
- **Email content** -- Nurture quality, proof usage, CTA strength, role/stage relevance
- **Ad creative** -- Message match, offer quality, ICP fit, visual clarity

### Step 6: Conversion Optimization Summary
Compile all conversion-related findings:

- **Primary conversion paths** -- How finance buyers become leads, demos, or product-tour starts
- **Funnel leaks** -- Where Moss loses intent across homepage, product pages, pricing, content, and forms
- **CRO quick wins** -- Changes that can be implemented immediately
- **Testing opportunities** -- A/B tests recommended with hypotheses
- **Benchmark comparison** -- Current rates vs appropriate B2B SaaS / fintech / spend-management standards

### Step 7: SEO Snapshot
Summarize SEO health in a scannable format:

```
SEO Health Snapshot:
- Title Tags: [Optimized / Needs Work / Missing]
- Meta Descriptions: [Optimized / Needs Work / Missing]
- H1 Tags: [Proper / Issues / Missing]
- Image Alt Text: [Complete / Partial / Missing]
- Page Speed: [Fast / Moderate / Slow]
- Mobile-Friendly: [Yes / Partially / No]
- Schema Markup: [Present / Partial / Missing]
- Hreflang / Localisation: [Strong / Issues / Missing]
- Sitemap: [Present / Issues / Missing]
- HTTPS: [Yes / No]
- Core Web Vitals: [Pass / Needs Work / Fail]
```

### Step 8: Build the Prioritized Action Plan

Organize all recommendations into three tiers:

#### Quick Wins (Implement This Week)
High impact, low effort changes. These should be implementable within 1-5 business days.

Format each item as:
```
- [ ] [Action item]: [Specific description]
  - Impact: [HIGH/MEDIUM/LOW]
  - Effort: [1-5 hours]
  - Expected Result: [Specific outcome for Moss, e.g. more qualified demos, better message match, stronger proof]
  - Revenue Impact: [€X/month estimated]
```

#### Medium-Term (Implement This Month)
Moderate impact, moderate effort. These require 1-4 weeks.

#### Strategic (Implement This Quarter)
High impact, high effort. These are foundational changes that require planning and sustained effort.

### Step 9: Build the 30-60-90 Day Roadmap

**Days 1-30: Foundation & Quick Wins**
- Week 1: Implement the highest-confidence Moss CRO and messaging fixes on key money pages
- Week 2: Validate tracking and establish baseline KPIs across traffic, conversion, pipeline, and ARR
- Week 3: Launch priority medium-term improvements in content, paid, or lifecycle
- Week 4: Review performance, tighten hypotheses, and reprioritize

**Days 31-60: Growth & Optimization**
- Week 5-6: Launch core page, offer, or paid-demand improvements
- Week 7: Begin A/B testing on Moss's highest-leverage pages and flows
- Week 8: Deploy content and nurture improvements tied to high-intent demand

**Days 61-90: Scale & Expand**
- Week 9-10: Scale what is working across product lines, offers, or locales
- Week 11: Expand to new comparison, integration, or demand-capture opportunities
- Week 12: Run a full review and update the next-quarter Moss growth roadmap

### Step 10: Appendix

Include methodology notes so the reader understands how scores were derived:

**Scoring Methodology:**
- How each category was evaluated for Moss's B2B fintech / spend-management context
- Data sources used
- Benchmarks referenced
- Limitations and assumptions
- Date of analysis

**Tools Used:**
- List any tools or scripts used in the analysis
- Reference to scripts/analyze_page.py if used
- Include relevant Moss tools where applicable (e.g. GA4, GSC, CRM, ad platforms, Convert, Hotjar, session replay, SEO tools)

**Glossary:**
- Define terms a non-marketing or cross-functional Moss stakeholder may not know
- Keep it relevant to terms used in the report (for example: spend management, AP automation, product-qualified lead, opportunity rate, ARR, message match)

## Output Format

Generate a file called `MARKETING-REPORT.md` with:

```markdown
# Marketing Report
## Moss (getmoss.com)
### Prepared by: Moss AI Marketing Assistant
### Date: [Date]

---

## Executive Summary

### Overall Marketing Score: [X/100] -- [Rating]

[2-3 paragraph summary covering: current state assessment, top 3 findings, estimated revenue or pipeline impact of implementing recommendations, and recommended first steps for Moss]

### Score Breakdown
| Category | Score | Rating |
|---|---|---|
| Website & Conversion | X/100 | [Rating] |
| SEO & Organic | X/100 | [Rating] |
| Content & Messaging | X/100 | [Rating] |
| Social Media | X/100 | [Rating] |
| Email & Automation | X/100 | [Rating] |
| Paid Advertising | X/100 | [Rating] |
| **Overall** | **X/100** | **[Rating]** |

### Top 3 Priority Actions
1. [Most impactful Moss recommendation with revenue / pipeline estimate]
2. [Second most impactful recommendation]
3. [Third most impactful recommendation]

---

## Detailed Findings

### 1. Website & Conversion [X/100]
[Deep-dive analysis with findings, what's working, gaps, recommendations]

### 2. SEO & Organic [X/100]
[Deep-dive analysis]

### 3. Content & Messaging [X/100]
[Deep-dive analysis]

### 4. Social Media [X/100]
[Deep-dive analysis]

### 5. Email & Automation [X/100]
[Deep-dive analysis]

### 6. Paid Advertising [X/100]
[Deep-dive analysis]

---

## Competitor Comparison
[Matrix and analysis]

---

## SEO Snapshot
[Health checklist]

---

## Conversion Optimization Summary
[Funnel analysis and CRO recommendations]

---

## Revenue Impact Summary
| Recommendation | Estimated Monthly Impact | Confidence | Priority |
|---|---|---|---|
| [Rec 1] | €X,XXX | High/Medium/Low | 1 |
| [Rec 2] | €X,XXX | High/Medium/Low | 2 |
| ... | ... | ... | ... |
| **Total Estimated Impact** | **€XX,XXX/month** | | |

---

## Prioritized Action Plan

### Quick Wins (This Week)
- [ ] [Action items with impact and effort]

### Medium-Term (This Month)
- [ ] [Action items]

### Strategic (This Quarter)
- [ ] [Action items]

---

## 30-60-90 Day Roadmap
[Week-by-week plan]

---

## Appendix
### Methodology
### Tools Used
### Glossary
### Data Sources
```

## Key Principles
- This report should be strong enough to use in Moss leadership reviews, planning, experimentation prioritization, and agency / freelancer briefing. It should not read like a generic agency teardown.
- Always lead with commercial insight and growth opportunity, not vague criticism. Frame findings around qualified demand, conversion quality, pipeline, and new ARR.
- Quantify everything possible. For Moss, "more qualified demos" or "€75,000/month in missed pipeline or ARR opportunity" is more useful than soft commentary.
- Make the action plan specific enough that a growth marketer, content lead, performance marketer, or CRO engineer at Moss could execute it.
- Use professional formatting: consistent headers, tables for data, checkboxes for action items, clear visual hierarchy.
- If data from previous skills is available, reference specific findings. If not, be transparent about what is based on direct evidence vs estimation.
- Benchmark Moss against relevant B2B spend-management and finance-software competitors, not generic B2C brands or irrelevant social tactics.
- Default to Moss-relevant channels and plays: website CRO, SEO, paid search, LinkedIn, lifecycle, webinars/events, integrations, customer proof, and finance-led thought leadership.
- Do not recommend TikTok-first, consumer-influencer, or broad brand-awareness tactics unless the user explicitly asks for them and the business case is strong.
- The report should tell a story: Here's where Moss is strong, here's where friction or leakage lives, here's the most valuable path forward, and here's what it is worth.
