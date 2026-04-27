# SEO Content Audit

## Skill Purpose
Perform a comprehensive SEO audit of a Moss webpage or Moss website section on `www.getmoss.com`, covering on-page SEO, content quality (E-E-A-T), keyword alignment, technical SEO, internal linking, and content strategy. This skill combines automated analysis via `scripts/analyze_page.py` with expert-level manual review to produce an actionable SEO audit document for Moss.

This skill is Moss-specific. Do not "discover the brand" from scratch. Use the following operating assumptions unless the user provides a tighter page-level brief:
- Brand: Moss is a European spend management platform built in Germany for modern finance teams.
- Product: Moss combines corporate cards, invoice management, reimbursements, budget controls, approvals, accounting automation, and integrations in one platform.
- Core buyer jobs-to-be-done: control spend before it happens, reduce manual accounting work, speed up month-end, improve approval workflows, increase policy compliance, and give finance teams real-time visibility.
- Primary ICP: companies with roughly 30-250 employees and meaningful indirect spend, especially finance teams at medium-sized European businesses.
- Typical buying committee: CFOs, Heads of Finance, Finance Managers, Accounting Leads, and Operations leaders.
- Core use-case clusters: spend management software, corporate cards, invoice management, AP automation, employee expense management, reimbursements, budget control, accounting automation, ERP/accounting integrations, month-end efficiency.
- Brand voice to protect in recommendations: clear, competent, modern, finance-first, low-hype, specific, and operationally credible.
- Default SEO competitor set: Spendesk, Pleo, Payhawk, Soldo, SAP Concur, and other spend-management / AP tools that overlap with Moss in European mid-market SERPs.

## When to Use
- User provides a Moss URL and asks for SEO analysis, audit, or recommendations
- User wants to improve Moss organic search rankings and qualified pipeline
- User asks about Moss on-page SEO, meta tags, content quality, or technical SEO
- User wants a Moss content gap analysis or Moss SEO content strategy recommendations
- Triggered by `/market seo <url>` or `/market seo`

## How to Execute

### Step 1: Run Automated Analysis
Use the Python analysis script to gather baseline data:

```bash
python3 scripts/analyze_page.py <url>
```

This script extracts:
- Title tag and meta description
- Open Graph tags
- Heading hierarchy (H1-H6)
- Links (internal and external)
- Images and alt text status
- Forms and CTAs
- Schema/structured data
- Social links
- Tracking scripts
- Viewport meta tag (mobile-friendliness indicator)
- Canonical tag
- Robots meta directives

Capture the JSON output and use it as the foundation for the manual analysis.

For Moss-specific reviews, also manually verify:
- Locale and path strategy (`/`, `/de-de`, `/en-gb`, `/nl-nl`, etc.)
- Whether the page is a core money page, support page, integration page, finance guide article, or campaign / landing page
- Whether the page matches a Moss product module, buyer pain point, or integration intent
- Whether the page is likely commercial, comparison, informational, or transactional in intent
- Whether the page is consistent with Moss’s Next.js / SPA behavior and not hiding important content behind client-side interactions

### Step 2: On-Page SEO Checklist
Evaluate each element and score it as Pass, Needs Work, or Fail.

#### Title Tag
| Criteria | Best Practice | Check |
|---|---|---|
| Exists | Every Moss page must have a unique title tag | Pass/Fail |
| Length | 50-60 characters where possible | Pass/Needs Work/Fail |
| Primary keyword | Contains the actual Moss page target term (e.g. spend management software, corporate cards, invoice management, AP automation, reimbursement software, accounting automation, [integration] integration) | Pass/Needs Work/Fail |
| Keyword position | Primary keyword appears near the beginning unless brand demand or trust proof should lead | Pass/Needs Work/Fail |
| Brand name | Includes Moss, usually at the end unless the query is strongly branded | Pass/Needs Work/Fail |
| Uniqueness | Different from other Moss pages and locale variants | Pass/Fail |
| Compelling | Would a finance buyer want to click this over Spendesk, Pleo, Payhawk, Concur, or other competing results? | Pass/Needs Work/Fail |

**Common title tag mistakes for Moss:**
- Leading with vague branding instead of the buyer problem or category
- Using internal product language instead of search language
- Stuffing multiple adjacent finance software terms into one title
- Reusing the same title across modules, locales, or integration pages
- Generic titles like "Product Overview" without a search-facing value proposition
- Failing to signal the use case, audience, or outcome

#### Meta Description
| Criteria | Best Practice | Check |
|---|---|---|
| Exists | Every important Moss page should have a meta description | Pass/Fail |
| Length | 150-160 characters | Pass/Needs Work/Fail |
| Primary keyword | Naturally includes the page target term | Pass/Needs Work/Fail |
| Call to action | Includes a reason to click (e.g. control spend, automate accounting, speed up month-end, book a demo, compare solutions) | Pass/Needs Work/Fail |
| Unique | Different from other Moss pages | Pass/Fail |
| Compelling | Reads like strong search ad copy for a finance decision-maker | Pass/Needs Work/Fail |

#### Heading Hierarchy (H1-H6)
| Criteria | Best Practice | Check |
|---|---|---|
| H1 exists | Exactly one H1 per page | Pass/Fail |
| H1 contains keyword | H1 includes the page’s core category, use case, or buyer problem | Pass/Needs Work/Fail |
| H1 differs from title | H1 and title tag are different but aligned | Pass/Needs Work/Fail |
| Logical hierarchy | H2 under H1, H3 under H2, no chaotic jumps | Pass/Needs Work/Fail |
| Descriptive subheadings | H2s and H3s clearly explain Moss modules, outcomes, proof, integrations, or workflow steps | Pass/Needs Work/Fail |
| Keywords in subheadings | Secondary terms and supporting intents appear naturally in H2s/H3s | Pass/Needs Work/Fail |
| Not overused | Headers are used for structure, not styling | Pass/Needs Work/Fail |

#### Image Optimization
| Criteria | Best Practice | Check |
|---|---|---|
| Alt text | Every meaningful image has descriptive alt text | Pass/Needs Work/Fail |
| Alt text quality | Alt text describes Moss UI, workflow, chart, or customer context accurately and does not stuff keywords | Pass/Needs Work/Fail |
| File names | Descriptive filenames (e.g. `moss-invoice-approval-workflow.png`) | Pass/Needs Work/Fail |
| File size | Images optimized for web; screenshots and hero assets are compressed appropriately | Pass/Needs Work/Fail |
| Lazy loading | Below-fold images use lazy loading where appropriate | Pass/Needs Work/Fail |
| Responsive images | Uses `srcset` or equivalent responsive delivery | Pass/Needs Work/Fail |
| Decorative images | Decorative images use empty alt="" rather than missing alt attributes | Pass/Needs Work/Fail |

#### Internal Linking
| Criteria | Best Practice | Check |
|---|---|---|
| Internal links present | Page links to relevant Moss product, pricing, integration, resource, and conversion pages | Pass/Needs Work/Fail |
| Anchor text | Internal link anchor text is descriptive and uses buyer language | Pass/Needs Work/Fail |
| Deep linking | Links go to the relevant module, integration, or guide page instead of defaulting to the homepage | Pass/Needs Work/Fail |
| Relevant context | Links are contextually relevant to the surrounding copy and buyer journey | Pass/Needs Work/Fail |
| Reasonable count | Enough internal links to support crawl flow and journey progression without clutter | Pass/Needs Work/Fail |
| Broken links | No broken internal links or obsolete route patterns | Pass/Fail |

#### URL Structure
| Criteria | Best Practice | Check |
|---|---|---|
| Readable | URL is human-readable and descriptive | Pass/Needs Work/Fail |
| Keywords | URL contains relevant category, use case, or integration keywords | Pass/Needs Work/Fail |
| Length | Under 75 characters where possible | Pass/Needs Work/Fail |
| Hyphens | Words separated by hyphens | Pass/Fail |
| Lowercase | All lowercase characters | Pass/Fail |
| No parameters | Clean URLs without unnecessary query parameters for indexable pages | Pass/Needs Work/Fail |
| Trailing slashes | Consistent use across comparable Moss URLs | Pass/Needs Work/Fail |

### Step 3: Content Quality Assessment (E-E-A-T)

Evaluate the content against Google's E-E-A-T framework:

#### Experience
Does the content demonstrate first-hand experience with the topic and with the realities of finance operations?

**Check for:**
- Moss screenshots, product walkthroughs, or realistic workflow examples
- Details that show understanding of approvals, card controls, invoice coding, month-end, and accounting handoff
- Customer examples relevant to medium-sized European companies
- First-hand implementation or process knowledge, not generic fintech copy

**Score:** Strong / Present / Weak / Missing

#### Expertise
Does the content demonstrate knowledge of spend management, finance operations, AP, cards, reimbursements, accounting automation, or integrations?

**Check for:**
- Accuracy and depth of content
- Clear use of finance and accounting terminology without unnecessary jargon
- Explanation of operational tradeoffs, not just feature promotion
- Evidence that Moss understands finance workflows, controls, and close processes
- Links to authoritative sources when external claims or regulations are referenced

**Score:** Strong / Present / Weak / Missing

#### Authoritativeness
Is Moss positioned as a credible authority for this topic?

**Check for:**
- Customer logos, testimonials, and case studies relevant to the page topic
- Evidence of product depth across cards, invoices, reimbursements, and accounting
- Integrations with major accounting / ERP systems
- Comparison content, category content, and finance guides that show topical depth
- Brand trust markers such as regulatory, legal, security, or operational credibility signals where relevant

**Score:** Strong / Present / Weak / Missing

#### Trustworthiness
Can finance buyers trust the page and the brand?

**Check for:**
- HTTPS
- Clear privacy policy and legal information
- Contact details and company transparency
- Accurate, up-to-date product claims
- Consistent messaging across page, navigation, footer, and CTAs
- Clear explanation of what happens after a form submission
- Proof close to high-intent CTAs on money pages

**Score:** Strong / Present / Weak / Missing

### Step 4: Keyword Analysis

#### Primary Keyword Assessment
| Element | Evaluation |
|---|---|
| Primary keyword identified | What exact Moss keyword or buyer-intent cluster is this page targeting? |
| Search intent alignment | Does the content match what searchers expect? (informational, commercial, transactional, navigational) |
| Keyword in title | Present, position, natural usage |
| Keyword in H1 | Present, natural usage |
| Keyword in first 100 words | Appears early in the content |
| Keyword in subheadings | Appears in at least one H2 or H3 where relevant |
| Keyword in meta description | Present and natural |
| Keyword in URL | Present |
| Keyword density | Natural usage; avoid stuffing adjacent finance software synonyms |

#### Secondary Keywords
Identify 5-10 related keywords that should be naturally included in the content. Prioritize terms that align to Moss’s product and ICP, such as:
- Spend management software / platform
- Corporate card / corporate credit card / business credit card
- Invoice management / invoice processing
- Accounts payable software / AP automation
- Expense management / employee expense management
- Reimbursement software
- Budget control / spend control / approval workflows
- Accounting automation / month-end close / pre-accounting
- ERP and accounting integrations (e.g. DATEV, Xero, NetSuite, Business Central, Exact Online) when relevant
- Buyer-problem terms like reduce manual accounting work, control company spend, speed up month-end

#### Search Intent Analysis
Determine the search intent behind the target keyword and evaluate if the content matches:

| Intent Type | User Goal | Moss Content Should Be |
|---|---|---|
| Informational | Learn something | Finance guide, glossary, template, checklist, FAQ |
| Commercial | Compare options | Solution page, category page, comparison page, buyer’s guide |
| Transactional | Start evaluation | Product page, pricing page, demo page, get-started page |
| Navigational | Find a specific Moss page | Homepage, pricing, login, product overview, integrations |

**Misalignment is a ranking killer.** If a finance buyer searches for "what is AP automation" and lands on a page that only pushes a demo with thin educational content, that is a mismatch. If they search for "spend management software" and land on a blog post with no product pathway, that is also a mismatch.

### Step 5: Technical SEO Quick Check

#### Robots.txt
```
Check: Does /robots.txt exist and is it properly configured for Moss?
```
- [ ] robots.txt is accessible
- [ ] Not blocking important Moss pages or resources
- [ ] Points to sitemap.xml or sitemap index
- [ ] Not blocking CSS/JS needed to render critical content

#### XML Sitemap
```
Check: Does /sitemap.xml exist and does it reflect Moss URL strategy?
```
- [ ] Sitemap exists and is accessible
- [ ] Contains important indexable pages across products, guides, integrations, and locales
- [ ] No broken or redirected URLs in sitemap
- [ ] Submitted to Google Search Console
- [ ] Last modified dates are accurate

#### Canonical Tags
- [ ] Canonical tag present on the page
- [ ] Points to the correct Moss URL
- [ ] Locale variants are not accidentally canonicalized to the wrong market page
- [ ] Consistent with robots.txt and sitemap

#### Page Speed
Reference benchmarks:

| Metric | Good | Needs Work | Poor |
|---|---|---|---|
| Largest Contentful Paint (LCP) | Under 2.5s | 2.5-4.0s | Over 4.0s |
| First Input Delay (FID) | Under 100ms | 100-300ms | Over 300ms |
| Cumulative Layout Shift (CLS) | Under 0.1 | 0.1-0.25 | Over 0.25 |
| Time to First Byte (TTFB) | Under 200ms | 200-500ms | Over 500ms |
| First Contentful Paint (FCP) | Under 1.8s | 1.8-3.0s | Over 3.0s |

**Common speed issues to flag on Moss:**
- Heavy hero media or oversized screenshots
- Client-side scripts causing delay or layout shift
- Render-blocking JavaScript or CSS
- Too many third-party scripts (analytics, chat, testing, widgets)
- Slow-loading logo strips, review widgets, or animated sections
- Unoptimized locale assets or duplicated page resources
- Hydration or SPA behavior delaying meaningful content rendering

#### Mobile-Friendliness
- [ ] Viewport meta tag present (`<meta name="viewport" content="width=device-width, initial-scale=1">`)
- [ ] Text readable without zooming
- [ ] Tap targets adequately sized and spaced
- [ ] No horizontal scrolling required
- [ ] Responsive images
- [ ] Forms usable on mobile, especially high-intent demo / get-started flows

### Step 6: Content Gap Analysis

Methodology for identifying content gaps for Moss:

1. **Identify the topic cluster:** What Moss module, buyer problem, or integration intent does this page belong to?
2. **Map existing content:** What Moss pages already cover this topic across product pages, finance guides, integrations, comparison content, and locale variants?
3. **Identify missing subtopics:** What adjacent problems, objections, comparisons, integrations, or workflow questions are not being addressed?
4. **Analyze People Also Ask:** What questions do finance buyers ask around the topic?
5. **Check related searches:** What does Google suggest around the target keyword and what does that reveal about buyer journey gaps?

**Default Moss content pillars to audit against:**
- Spend management / business spend control
- Corporate cards / employee card controls
- Invoice management / AP automation
- Reimbursements / employee expenses
- Budgeting, approvals, and policy control
- Accounting automation / month-end close
- Integrations and ERP/accounting sync
- Regulatory / finance operations education where relevant
- Comparison / alternative / versus content
- Customer proof and use-case content by team or industry

**Content Gap Template:**
| Missing Topic | Search Volume Potential | Competition | Content Type Needed | Priority |
|---|---|---|---|---|
| [Topic] | High/Med/Low | High/Med/Low | Product page/Comparison page/Guide/Integration page/Template | 1-5 |

### Step 7: Featured Snippet Optimization

Identify opportunities to capture featured snippets:

**Types of featured snippets:**
1. **Paragraph snippet** -- Answer in 40-60 words. Use a clear finance-buyer question as H2/H3 followed by a concise answer.
2. **List snippet** -- Use ordered or unordered lists for steps, requirements, or comparisons.
3. **Table snippet** -- Use HTML tables for plan comparisons, workflow comparisons, or software comparison criteria.
4. **Video snippet** -- Include video with descriptive title and timestamps when Moss has strong visual product education.

**Optimization checklist:**
- [ ] Target question-based queries such as "what is spend management software", "how do corporate cards work", "what is AP automation", "how to speed up month-end"
- [ ] Place answer immediately after the question heading
- [ ] Keep paragraph answers between 40-60 words
- [ ] Use structured lists and tables where appropriate
- [ ] Include the target query in an H2 or H3

### Step 8: Schema Markup Audit

Check for structured data implementation:

| Schema Type | Applicable To | Status |
|---|---|---|
| Organization | Homepage, About page, brand-level trust pages | Present/Missing |
| LocalBusiness | Usually N/A for Moss unless there is a true local-office SEO need | Present/Missing/N/A |
| Product / SoftwareApplication | Product, module, and software solution pages | Present/Missing/N/A |
| Article | Finance guide articles, insights, news | Present/Missing/N/A |
| FAQ | FAQ sections and high-intent solution pages | Present/Missing |
| HowTo | Process-led educational content where appropriate | Present/Missing/N/A |
| Review/AggregateRating | Testimonials or review-driven pages only if compliant and visible | Present/Missing/N/A |
| BreadcrumbList | All pages with breadcrumb structures | Present/Missing |
| WebSite/SearchAction | Homepage | Present/Missing |
| Event | Webinar or event pages | Present/Missing/N/A |

**Implementation guidance:**
- Use JSON-LD format
- Validate with Google’s Rich Results Test
- Don't mark up content that isn't visible on the page
- Keep schema data consistent with on-page content
- Prioritize schema types that strengthen Moss category understanding and trust on money pages

### Step 9: Internal Linking Opportunities

Identify specific internal linking improvements:

1. **Orphan pages** -- Important Moss pages with no meaningful internal links pointing to them
2. **Hub pages** -- Category and solution pages that should link to related guides, proof, integrations, and demo paths
3. **Topical clusters** -- Group related Moss content around modules, buyer jobs-to-be-done, and integration ecosystems
4. **CTA links** -- Finance guide content should link to the most relevant product, integration, pricing, or demo page
5. **Footer/sidebar links** -- Sitewide links to important commercial and trust pages where appropriate

**Linking Architecture Assessment:**
```
Homepage
  |-- Solution / Module Pages (Corporate Cards, Invoice Management, Reimbursements, Budget Control, Accounting)
       |-- Supporting Guides / Use Case Pages / Comparison Pages / Customer Stories
            |-- Back-links to Solution / Module Pages
  |-- Integration Pages (DATEV, Xero, NetSuite, Business Central, etc.)
       |-- Linked from relevant product and guide content
  |-- Key Conversion Pages (Pricing, Product Overview, Get Started, Demo)
       |-- Linked from high-intent commercial and educational pages
```

### Step 10: Core Web Vitals Impact Assessment

Evaluate the conversion and revenue impact of Core Web Vitals performance on Moss pages:

**Typical Moss impact pathways:**
- Slow LCP on hero sections reduces demo and get-started engagement
- Slow interactivity harms navigation, comparison, and form progression
- CLS around trust proof, CTAs, banners, or forms reduces confidence
- Technical lag is especially damaging on paid landing pages and high-intent product pages

**Recommendations by metric:**
| Metric | If Failing | Typical Fixes |
|---|---|---|
| LCP | Over 2.5s | Optimize hero assets, preload critical resources, simplify above-the-fold DOM, reduce third-party weight |
| FID/INP | Over 100ms | Reduce JavaScript execution, defer non-critical scripts, simplify client-side interactions |
| CLS | Over 0.1 | Set image dimensions, reserve space for dynamic elements, avoid injecting content above existing content |

### Step 11: Blog and Content Strategy Recommendations

Based on the audit findings, recommend:

1. **Publishing cadence** -- Prioritize fewer, higher-intent, higher-expertise pages over generic volume plays. For Moss, focus on commercial pages, integration pages, comparison pages, and expert finance guides before broad top-of-funnel content.
2. **Content types** -- Product pages, solution pages, integration pages, finance guides, templates/checklists, comparison pages, customer stories, and glossary / definitional content where it supports category capture.
3. **Keyword targeting strategy** -- Balance category terms, buyer-problem terms, integration terms, comparison terms, and regulated / operational finance topics relevant to Europe.
4. **Content length** -- Benchmark against top-ranking content, but prioritize completeness, specificity, and conversion alignment over arbitrary word count.
5. **Content update strategy** -- Refresh high-value pages after product changes, positioning changes, SERP shifts, or important market / regulatory changes. Product, integration, and comparison pages should be reviewed more often than evergreen guides.
6. **Distribution plan** -- Promote new or refreshed SEO content through internal linking, lifecycle email, paid amplification where justified, sales enablement, and Moss-owned social channels relevant to finance audiences.

**Content Prioritization Matrix:**
| Content Idea | Search Volume | Competition | Business Value | Priority Score |
|---|---|---|---|---|
| [Topic] | High/Med/Low | High/Med/Low | High/Med/Low | 1-10 |

Scoring: High volume + Low competition + High business value = Highest priority

## Output Format

Generate a file called `SEO-AUDIT.md` with:

```markdown
# SEO Content Audit
## [URL]
### Date: [Date]

---

## SEO Health Score: [X/100]

---

## Moss Context
- ICP: [finance team / company type / geo / buyer stage]
- Page Type: [homepage / product / solution / integration / guide / comparison / campaign]
- Primary Business Goal: [demo / get started / qualified lead / self-serve / education / branded demand]
- Primary Keyword Cluster: [cluster]
- Search Intent: [informational/commercial/transactional/navigational]

---

## On-Page SEO Checklist

### Title Tag
- Status: [Pass/Needs Work/Fail]
- Current: "[current title]"
- Recommended: "[improved title]"
- Issues: [list issues]

### Meta Description
- Status: [Pass/Needs Work/Fail]
- Current: "[current meta]"
- Recommended: "[improved meta]"

### Heading Hierarchy
[H1-H6 structure analysis]

### Image Optimization
[Alt text audit results]

### Internal Linking
[Link analysis]

### URL Structure
[URL assessment]

---

## Content Quality (E-E-A-T)
| Dimension | Score | Evidence |
|---|---|---|
| Experience | [Strong/Present/Weak/Missing] | [details] |
| Expertise | [Strong/Present/Weak/Missing] | [details] |
| Authoritativeness | [Strong/Present/Weak/Missing] | [details] |
| Trustworthiness | [Strong/Present/Weak/Missing] | [details] |

---

## Keyword Analysis
- Primary Keyword: [keyword]
- Search Intent: [type]
- Keyword Placement: [checklist results]
- Secondary Keywords: [list]
- Moss Module / JTBD Alignment: [which module or buyer problem this page supports]

---

## Technical SEO
[Quick check results, including locale/canonical considerations if relevant]

---

## Content Gap Analysis
[Missing topics table]

---

## Featured Snippet Opportunities
[Specific opportunities]

---

## Schema Markup
[Current vs recommended]

---

## Internal Linking Opportunities
[Specific recommendations]

---

## Core Web Vitals
[Performance assessment with likely conversion impact]

---

## Content Strategy Recommendations
[Publishing plan, content priorities]

---

## Prioritized Recommendations

### Critical (Fix Immediately)
1. [recommendation with expected impact]

### High Priority (This Month)
1. [recommendation]

### Medium Priority (This Quarter)
1. [recommendation]

### Low Priority (When Resources Allow)
1. [recommendation]
```

## Key Principles
- Moss SEO audits must be commercial as well as diagnostic. The goal is not just rankings; it is qualified pipeline, demo intent, and revenue relevance.
- Always evaluate a page in the context of Moss’s actual audience: finance teams at medium-sized businesses with indirect spend complexity.
- Do not recommend generic SEO copy. Recommendations must sound like Moss: clear, specific, credible, and finance-first.
- Tie every page to a real Moss keyword cluster, buyer problem, module, or integration. If a page cannot be mapped to one of those, say so.
- Always provide the "before" (current state) and "after" (recommended change) so the team can act quickly.
- Prioritize search intent fit over keyword inclusion. A perfectly optimized page for the wrong intent is still a bad page.
- Prioritize recommendations by effort-to-impact ratio. Titles, internal links, weak headings, proof placement, and content alignment are often faster wins than full rewrites.
- For Moss, category pages, module pages, integration pages, comparison pages, and high-intent finance guides matter more than generic top-of-funnel traffic.
- If the user has run `/market audit` or `/market landing` previously, cross-reference those findings with the SEO audit for a more complete picture.
