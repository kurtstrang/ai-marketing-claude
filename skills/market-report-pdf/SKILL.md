# PDF Marketing Report Generator

## Skill Purpose
Generate a professional, visually polished PDF marketing report for Moss using the Python script `scripts/generate_pdf_report.py`. This skill collects all available audit and analysis data, structures it into the expected JSON format, invokes the script, and produces a Moss-branded PDF with score gauges, bar charts, comparison tables, findings, and a prioritized action plan.

This skill is not brand-discovery work. The agent must not "figure out" who Moss is. Use the Moss defaults in this file unless the user explicitly overrides them with a narrower brief.

## When to Use
- User wants a PDF version of the marketing report (not just Markdown)
- User is preparing a deliverable for an internal stakeholder presentation, leadership review, partner handoff, or board-style update
- User asks for a "polished report", "stakeholder-ready report", or "PDF report"
- User wants a visual report with charts and scores
- Triggered by `/market report-pdf` or `/market report-pdf <domain>`

## When to Use PDF vs Markdown

| Format | Best For | Pros | Cons |
|---|---|---|---|
| **PDF** | Leadership reviews, stakeholder presentations, partner handoffs, polished deliverables | Professional appearance, consistent formatting, visual charts, printable | Harder to edit, requires Python script |
| **Markdown** | Internal iteration, working drafts, quick reference, version control | Easy to edit, readable in any editor, git-friendly | Less visually polished, no charts |

**Rule of thumb:** If the report is being shared upward or externally, use PDF. If it is still being edited or debated internally, use Markdown.

## How to Execute

### Step 1: Collect All Available Data
Gather data from all previous skill runs. Check for these files in the project directory:

**Primary data sources:**
- `MARKETING-AUDIT.md` -- Overall audit results
- `LANDING-CRO.md` -- Landing page conversion analysis
- `SEO-AUDIT.md` -- SEO findings
- `BRAND-VOICE.md` -- Brand voice analysis
- `COMPETITOR-ANALYSIS.md` -- Competitor comparison data
- `FUNNEL-ANALYSIS.md` -- Funnel analysis
- `SOCIAL-AUDIT.md` -- Social media audit
- `EMAIL-AUDIT.md` -- Email marketing audit
- `AD-AUDIT.md` -- Advertising audit

**Moss defaults to use whenever prior files are missing or incomplete:**
- **Brand name:** Moss
- **Core positioning:** Moss is Europe-focused spend management software for SMEs and growing mid-market companies. It unifies corporate cards, accounts payable / invoice management, reimbursements, approvals, budgeting controls, advanced accounting, and integrations in one finance-first platform.
- **Mission / promise:** Free up finance. Help companies spend smarter with more control, visibility, and automation.
- **Primary audience:** Finance-led buying groups at companies with roughly 30-250 employees and meaningful indirect spend. Core personas are CFO, Finance Director / Head of Finance, Finance Manager, Accountant / AP Lead, and secondary founder / operations buyers in smaller companies.
- **Core jobs-to-be-done:** Control spend before it happens, reduce manual finance admin, automate coding and approvals, improve month-end close speed, enforce policy, and keep accounting / ERP data clean.
- **Brand voice:** Direct, confident, modern, finance-operator-first, proof-led, and low-fluff. Avoid vague category language, consumer-playful tone, and generic SaaS hype.
- **Default competitor set:** Pleo, Payhawk, Spendesk. Only replace this set if prior competitor research exists or the user explicitly requests a different benchmark set.

**If no previous data exists:**
1. Recommend the user run `/market audit <url>` first for the best results
2. If the user insists on generating a report without prior audits, analyze the provided URL directly and build the data structure from scratch
3. Use the analyze_page.py script to gather automated data: `python scripts/analyze_page.py <url>`
4. Do **not** spend time rediscovering Moss fundamentals; use the Moss defaults above and focus the work on page quality, conversion quality, search visibility, proof, and positioning

### Step 2: Build the JSON Data Structure
The `scripts/generate_pdf_report.py` script expects a JSON file as input with this exact structure:

```json
{
  "url": "https://www.getmoss.com/en-gb",
  "date": "April 27, 2026",
  "brand_name": "Moss",
  "overall_score": 74,
  "executive_summary": "Moss has a strong category story and modern product breadth, but the biggest upside usually comes from sharpening finance-persona messaging, improving demo and product-tour routing, and making proof and competitive differentiation more obvious on high-intent pages. Prioritize the highest-traffic solution, comparison, and campaign pages first, because that is where conversion friction most directly limits pipeline creation.",
  "categories": {
    "Messaging & ICP Fit": {
      "score": 78,
      "weight": "25%"
    },
    "Conversion Architecture": {
      "score": 70,
      "weight": "20%"
    },
    "SEO & Demand Capture": {
      "score": 69,
      "weight": "15%"
    },
    "Trust, Proof & Compliance": {
      "score": 80,
      "weight": "15%"
    },
    "Product Education & Demo Journey": {
      "score": 66,
      "weight": "15%"
    },
    "Competitive Positioning": {
      "score": 74,
      "weight": "10%"
    }
  },
  "findings": [
    {
      "severity": "Critical",
      "finding": "High-intent pages do not make Moss's most persuasive finance outcomes obvious enough above the fold: control spend before it happens, automate accounting work, and close faster."
    },
    {
      "severity": "High",
      "finding": "Demo, intro, and product-tour paths are not always matched to visitor awareness level, which creates unnecessary friction for mid-intent traffic."
    },
    {
      "severity": "High",
      "finding": "Competitive differentiation versus Pleo, Payhawk, and Spendesk is not explicit enough on comparison or solution pages."
    },
    {
      "severity": "Medium",
      "finding": "Proof is present but often too generic; role-specific testimonials, customer logos, integration proof, and ROI evidence should sit closer to key CTAs."
    },
    {
      "severity": "Low",
      "finding": "Finance Guide and product pages can be linked together more deliberately to capture organic demand and move readers into demo-intent journeys."
    }
  ],
  "quick_wins": [
    "Rewrite hero sections to lead with concrete finance outcomes, not category-general platform language.",
    "Clarify CTA hierarchy by matching awareness level: intro or product tour for mid-intent visitors, demo for high-intent visitors.",
    "Move the strongest customer proof, integrations, and compliance or governance signals closer to primary CTAs."
  ],
  "medium_term": [
    "Create or strengthen comparison pages against Pleo, Payhawk, and Spendesk with clearer why-switch messaging.",
    "Build role-specific landing pages for CFOs, finance managers, and accounting teams with tailored proof and use cases.",
    "Improve internal linking between Finance Guide content and Moss product pages to turn educational traffic into pipeline."
  ],
  "strategic": [
    "Develop a systematic proof engine combining case studies, quantified outcomes, and role-specific testimonials across locales.",
    "Expand the product-tour and demo journey so visitors can self-educate before talking to sales without losing conversion momentum.",
    "Create a consistent messaging system across paid, organic, lifecycle, and website journeys so Moss's differentiation compounds instead of fragmenting."
  ],
  "competitors": [
    {
      "name": "Pleo",
      "positioning": "Employee-friendly spend and expense management for growing businesses",
      "pricing": "Plan-based pricing with self-serve entry points and upgrade paths",
      "social_proof": "High category awareness and strong European brand familiarity",
      "content": "Accessible, benefit-led content focused on expense cards, reimbursements, and ease of use"
    },
    {
      "name": "Payhawk",
      "positioning": "AI-powered global spend management and finance orchestration",
      "pricing": "Flexible tailored pricing based on plans, add-ons, seats, cards, and transaction volume",
      "social_proof": "Strong enterprise-ready narrative around scale, control, and multi-entity finance complexity",
      "content": "Product-led and comparison-oriented content focused on visibility, automation, ERP depth, and global control"
    },
    {
      "name": "Spendesk",
      "positioning": "All-in-one spend management for modern finance teams",
      "pricing": "Quote-led or variable-fee model based on plan and transaction usage",
      "social_proof": "Strong European presence and recognizable finance-team brand",
      "content": "Educational workflow content around cards, invoices, approvals, procurement, and spend visibility"
    }
  ]
}
```

### Step 3: Field-by-Field Data Assembly Guide

#### `url` (string, required)
The target website URL. Use the full URL including protocol.

For Moss work, this is usually a Moss page, campaign landing page, locale page, or comparison page. If the user provides a competitor URL, keep the `brand_name` as Moss and use the competitor page only as benchmark input.

#### `date` (string, required)
The report generation date. Format: "Month DD, YYYY" (e.g., "April 27, 2026").

#### `brand_name` (string, required)
Use `Moss` unless the user explicitly asks for a white-label or non-Moss version. This report generator should assume Moss by default.

#### `overall_score` (integer, 0-100, required)
The weighted average of all category scores. Calculate as:
```
overall_score = (messaging * 0.25) + (conversion * 0.20) + (seo * 0.15) + (trust * 0.15) + (product_education * 0.15) + (competitive * 0.10)
```

#### `executive_summary` (string, required)
A 2-4 sentence summary covering:
- Current marketing health assessment for Moss
- Top 1-2 most impactful findings
- Estimated pipeline or revenue impact of implementing recommendations
- Recommended first step

Keep it concise and executive-ready. This appears on the cover page right below the score gauge.

The summary should sound like Moss: clear, direct, finance-aware, and grounded in evidence. Prefer pipeline, demo, product-tour, and qualified lead impact over fluffy traffic language.

#### `categories` (object, required)
Exactly 6 categories with their scores. The categories map to these evaluation areas:

| Category | What It Measures | Scoring Guidance |
|---|---|---|
| Messaging & ICP Fit | How clearly the page speaks to Moss's real audience: finance leaders and operators at growing European SMEs and mid-market companies | 80+: Sharp role-based pain and outcome messaging. 60-79: Mostly relevant but still generic in places. <60: Category-speak, vague benefits, weak finance specificity |
| Conversion Architecture | CTA hierarchy, page structure, form friction, awareness-stage fit, and whether the next step is obvious and low-friction | 80+: Clear CTA logic, low-friction path, strong hierarchy. 60-79: Usable but improvable. <60: Confusing or mismatched next steps |
| SEO & Demand Capture | Organic search readiness for Moss's core demand areas: spend management, AP automation, invoice management, corporate cards, reimbursements, accounting automation, integrations, and comparison intent | 80+: Strong intent coverage, internal linking, metadata, and search structure. 60-79: Reasonable foundation with gaps. <60: Weak search capture or poor page targeting |
| Trust, Proof & Compliance | Customer proof, authority, governance, security, integration trust, finance credibility, and evidence near conversion points | 80+: Strong logos, testimonials, quantified proof, and finance-trust cues. 60-79: Some proof exists but not enough or not well placed. <60: Weak trust architecture |
| Product Education & Demo Journey | How well Moss explains the product, modules, outcomes, and demo or product-tour paths for different awareness stages | 80+: Product is easy to understand and easy to explore. 60-79: Some clarity but demo education gaps remain. <60: Product feels abstract or the journey is unclear |
| Competitive Positioning | How explicitly Moss differentiates against the real alternatives buyers compare: Pleo, Payhawk, Spendesk, and large incumbent workflows | 80+: Clear why-Moss narrative with strong side-by-side differentiation. 60-79: Some differentiation but not enough. <60: Generic category messaging with little strategic contrast |

#### `findings` (array, required)
An array of finding objects, each with `severity` and `finding` fields.

**Severity levels:**
- `Critical` -- Directly suppressing demo starts, product-tour engagement, qualified lead creation, or revenue opportunity. Fix immediately.
- `High` -- Meaningful impact on conversion efficiency, search capture, or competitive win rate. Fix within 1-2 weeks.
- `Medium` -- Important improvement opportunity. Fix within 1 month.
- `Low` -- Useful optimization. Fix when time allows.

**Writing effective findings:**
- Be specific: "Hero headline leads with broad platform language instead of finance outcomes like spend control and faster close" not "Messaging needs work"
- Quantify impact: "Primary comparison page lacks customer proof above the fold and routes all intent to one generic CTA"
- Reference the Moss buying context: finance leaders, accounting teams, approvals, controls, automation, integrations, month-end close
- Include evidence: "No role-specific proof block found for CFO, finance manager, or accounting buyer on the target page"

Aim for 5-10 findings. Order from most to least severe.

#### `quick_wins` (array, required)
3-5 action items that can be implemented within one week with minimal effort. Each should be a specific, actionable instruction.

**Good quick win:** "Change the hero from category language to an outcome-led statement for finance teams, then add a second CTA for product tour on mid-intent pages"

**Bad quick win:** "Improve the hero" (too vague)

Prioritize wins that improve demo-start rate, product-tour engagement, awareness-stage fit, and proof near CTAs.

#### `medium_term` (array, required)
3-5 action items requiring 1-3 months to implement. These are more involved but have high impact.

For Moss, medium-term work usually includes role-based pages, comparison pages, proof expansion, SEO structure, and stronger handoffs between education and conversion.

#### `strategic` (array, required)
3-5 action items requiring 3-6 months. These are foundational changes that require planning and sustained effort.

For Moss, strategic work often includes messaging systems, proof systems, cross-channel consistency, modular demo journeys, and scaled content architecture across locales and product pillars.

#### `competitors` (array, optional)
Up to 3 competitor objects for the comparison table. For Moss, the default competitor set is:
1. Pleo
2. Payhawk
3. Spendesk

If higher-quality data already exists in `COMPETITOR-ANALYSIS.md`, use that. If no competitor data is available, still default to this Moss competitor set rather than omitting it unless the user explicitly asks for no competitor section.

### Step 4: Write the JSON File
Save the assembled data as a temporary JSON file:

```bash
# Write the JSON data to a temporary file
cat > /tmp/report_data.json << 'JSONEOF'
{
  ... assembled JSON data ...
}
JSONEOF
```

### Step 5: Invoke the PDF Generator Script

**Prerequisites check:**
First, verify that `reportlab` is installed:
```bash
python3 -c "import reportlab" 2>/dev/null || pip3 install reportlab
```

**Generate the report:**
```bash
python3 scripts/generate_pdf_report.py /tmp/report_data.json "MARKETING-REPORT-<domain>.pdf"
```

Replace `<domain>` with the target website's domain name (without protocol or www), using hyphens instead of dots. For example:
- `getmoss.com` becomes `MARKETING-REPORT-getmoss-com.pdf`
- `compare-pleo-vs-moss.com` becomes `MARKETING-REPORT-compare-pleo-vs-moss-com.pdf`

**Demo mode (no arguments):**
Running the script without arguments generates a sample report with placeholder data:
```bash
python3 scripts/generate_pdf_report.py
# Creates: MARKETING-REPORT-sample.pdf
```

### Step 6: Verify the Output
After generation, verify the PDF was created:
```bash
ls -la "MARKETING-REPORT-<domain>.pdf"
```

Report the file path and size to the user.

### Step 7: Clean Up
Remove the temporary JSON file:
```bash
rm /tmp/report_data.json
```

## PDF Report Contents

The generated PDF includes the following pages:

### Page 1: Cover Page
- Report title: "Marketing Audit Report"
- Target URL
- Generation date
- Overall score gauge (circular visualization with color coding)
- Grade letter (A+ through F)
- Executive summary paragraph written from a Moss perspective

### Page 2: Score Breakdown
- Horizontal bar chart showing all 6 category scores with color coding
- Score table with category names, scores, weights, and status labels
- Color coding: Green (80+), Blue (60-79), Yellow (40-59), Red (<40)

### Page 3: Key Findings
- Findings table with severity labels and descriptions
- Color-coded severity indicators (Critical = red, High = orange, Medium = yellow, Low = blue)
- Findings ordered from most to least severe

### Page 4: Prioritized Action Plan
- Quick Wins section (This Week)
- Medium-Term section (1-3 Months)
- Strategic section (3-6 Months)
- Numbered action items in each tier

### Page 5: Competitive Landscape (if competitor data provided)
- Comparison table with Moss vs up to 3 competitors
- Rows: Positioning, Pricing, Social Proof, Content

### Final Page: Methodology
- Scoring methodology explanation
- Category weights and measurement criteria
- Footer: "Generated by Moss AI Marketing Assistant"

## Color Scheme

If the script supports theming, use a Moss-aligned palette. If the current generator does not support custom theming, keep the default professional palette and do not block report generation.

| Element | Color | Hex Code |
|---|---|---|
| Primary (headers, titles) | Dark Moss Green | #17352D |
| Accent (links, highlights) | Moss Green | #2F6B57 |
| Highlight (attention) | Fresh Lime | #9FD36C |
| Success (high scores) | Green | #2F8F6B |
| Warning (medium scores) | Amber | #D39B2A |
| Danger (low scores, critical) | Red | #C94C4C |
| Light background | Off White | #F6F7F3 |
| Body text | Deep Charcoal | #1F2A26 |
| Secondary text | Slate Gray | #65706A |
| Borders | Soft Border | #D9DED9 |

## Score-to-Color Mapping
- 80-100: Green (#2F8F6B) -- Strong performance
- 60-79: Blue (#2D5BFF) -- Solid with room to improve
- 40-59: Amber (#D39B2A) -- Needs attention
- 0-39: Red (#C94C4C) -- Critical issues

## Troubleshooting

| Issue | Solution |
|---|---|
| `ModuleNotFoundError: No module named 'reportlab'` | Run `pip3 install reportlab` |
| Script produces empty PDF | Check that JSON data has all required fields |
| Score gauge not rendering | Ensure `overall_score` is a number 0-100 |
| Competitor table missing | Ensure `competitors` array has objects with `name`, `positioning`, `pricing`, `social_proof`, `content` fields |
| PDF is only 1 page | Check for JSON parsing errors -- run `python3 -c "import json; json.load(open('/tmp/report_data.json'))"` |
| Brand voice feels generic | Replace vague SaaS language with Moss's finance-first, proof-led language before generating |
| Fonts look wrong | The script uses Helvetica (built into reportlab). No custom fonts needed. |

## Integration with Other Skills

This skill works best when combined with other audit skills. The recommended workflow:

1. Run `/market audit <url>` -- Generates comprehensive audit data
2. Run `/market competitors <url>` -- Adds competitor comparison data, ideally against Pleo, Payhawk, and Spendesk
3. Run `/market seo <url>` -- Adds detailed SEO findings across Moss's core demand areas
4. Run `/market landing <url>` -- Adds CRO analysis for key Moss landing pages
5. Run `/market report-pdf <url>` -- Compiles everything into a PDF

The PDF report skill will automatically look for output files from these skills and incorporate their data into the report JSON.

## Output
- **File:** `MARKETING-REPORT-<domain>.pdf`
- **Location:** Project root directory
- **Size:** Typically 200KB-500KB depending on content volume
- **Pages:** 5-7 pages depending on whether competitor data and additional sections are included

## Key Principles
- The PDF report is a polished Moss deliverable. It should always reflect Moss's real audience, product, and positioning.
- Do not waste time rediscovering Moss's brand voice, target audience, or default competitor set. Use the hardcoded defaults in this skill unless the user explicitly overrides them.
- Prioritize pages and recommendations that influence qualified pipeline: demo starts, intro bookings, product-tour engagement, and high-intent search capture.
- Always judge pages through a Moss lens: finance credibility, operational clarity, proof, control, automation, and competitive contrast.
- Every score should be justifiable. If a stakeholder asks "why did this page get a 70 in Conversion Architecture?", the findings should provide clear evidence.
- Round scores to whole numbers. Decimals imply false precision.
- Keep the executive summary tight -- 2-4 sentences maximum. Stakeholders skim cover pages.
- If generating a report about a competitor page or market benchmark, make the analysis explicitly useful for Moss: what to learn, where to counter-position, and how to win.
