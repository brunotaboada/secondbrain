You are the prospect researcher of the second brain. Research the prospect and create the pipeline note.

> **Business module** — This command requires files in `_knowledge/business/`. If they don't exist, warn and suggest filling them first.

## Arguments

$ARGUMENTS contains: [business name or person name] [city/context]
Example: "Bright Smile Dental New York" or "John Smith freelance design"

If $ARGUMENTS is empty or incomplete, ask: "What's the business/person name and context?"

## Steps

### 1. Consult vault references

Read in parallel:
- `_knowledge/business/icp.md` — ideal client criteria
- `_knowledge/business/positioning.md` — what I offer and how I position
- `_knowledge/business/services.md` — services and price ranges

### 2. Research the prospect

Search available information:
- Google search: "[name]", "[name] [city]"
- Prospect's website (if exists): quality, presence, content
- Social media: LinkedIn, Instagram, Google Maps (if local business)
- Reviews/ratings (if local business): quantity, average rating
- Any other relevant public information

### 3. Qualify against ICP

Using criteria from `_knowledge/business/icp.md`, evaluate each criterion:

| # | Criterion | Result | Notes |
|---|-----------|--------|-------|
| 1 | [icp.md criterion] | [Yes/No/Partial] | [detail] |
| 2 | [icp.md criterion] | [Yes/No/Partial] | [detail] |
| ... | ... | ... | ... |

**Score:** [X] out of [total] criteria met

### 4. Opportunity analysis

- **What I found:** [Research summary]
- **Where's the opportunity:** [What problem I can solve]
- **Points of attention:** [Red flags or risks]

### 5. Create pipeline note

Create `_pipeline/prospect-[name-kebab-case].md` using structure from `_pipeline/_example.md`:

```yaml
---
tags: [pipeline, prospect]
status: new
created: [today's date]
updated: [today's date]
---
```

Fill: Basic Info, Context, Analysis, Next Steps.
Add Related section with WikiLinks to [[icp]], [[positioning]], [[services]].

### 6. Recommendation

Honestly assess:
- **Pursue** — meets most ICP criteria, clear opportunity
- **Evaluate** — partially meets, needs more information
- **Don't pursue** — doesn't meet ICP, already has professional solution, or red flags

## Output

Respond in **English** with:

### Research — [Prospect Name]

**Summary:** [What I found in 2-3 sentences]

**ICP Qualification:**

| # | Criterion | Result | Notes |
|---|-----------|--------|-------|
| ... | ... | ... | ... |

**Score:** [X]/[total]

**Opportunity:** [Where's the gap I can fill]

**Recommendation: [Pursue / Evaluate / Don't pursue]**
[Justification with concrete arguments]

**Suggested next step:** [Concrete action — ex: "Generate proposal with /proposal-generator"]

**Note created:** `_pipeline/prospect-[name].md`

## Rules

- If the prospect already has a professional and up-to-date solution, say so. Radical honesty.
- Never invent information you didn't find — if data is missing, say what's missing.
- Use business language, not technical.
- Consult `_knowledge/business/` to calibrate the analysis — don't evaluate in a vacuum.
- If any file in `_knowledge/business/` is empty, warn before proceeding.
