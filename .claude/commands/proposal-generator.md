You are the proposal generator of the second brain. Produce a personalized proposal based on the vault.

> **Business module** — This command requires `_knowledge/business/` filled out and a prospect note in `_pipeline/`.

## Arguments

$ARGUMENTS contains: [prospect name]
Example: "bright-smile-dental" or "Bright Smile Dental"

If $ARGUMENTS is empty, ask: "What's the prospect name? (must have note in `_pipeline/`)"

## Steps

### 1. Load prospect data

Search for the note in `_pipeline/` — can be `prospect-[name].md` or similar name.
If not found, list files in `_pipeline/` and suggest the closest match.

Extract:
- Name, business type, context
- Analysis done (identified opportunity)
- Problems/needs detected
- Any relevant research information

### 2. Consult references

Read in parallel:
- `_knowledge/business/positioning.md` — how I position myself
- `_knowledge/business/services.md` — what I offer and at what price
- `_knowledge/business/pricing.md` — pricing strategy
- `_knowledge/business/tone-of-voice.md` — communication tone
- `_knowledge/business/icp.md` — whether prospect is ICP (calibrates time investment)

### 3. Define approach

Based on the data:
- **Which service/package to recommend?** (based on prospect's need and [[services]])
- **Which price range?** (based on [[pricing]] and prospect's profile)
- **Which tone to use?** (based on [[tone-of-voice]] and prospect context)
- **What opening angle?** (specific observation about the prospect — never generic)

### 4. Generate proposal

Write the proposal with:
1. **Opening with specific observation** about the prospect (real data from research — never generic)
2. **Problem identification** — what I found that might be impacting the prospect
3. **Value proposition** — how I can help (language of outcome, not features)
4. **Next step** — Clear low-commitment CTA (call, free diagnosis, etc.)

**Maximum: 5-7 sentences.** Every word must have purpose.

### 5. Save in prospect's note

Add `## Proposal` section to the prospect note in `_pipeline/`:

```markdown
## Proposal

| Field | Value |
|-------|-------|
| **Generated on** | [today's date] |
| **Suggested package** | [package name] |
| **Price range** | [range] |
| **Tone** | [tone description] |
| **Status** | Ready to send |

### Proposal text

[full proposal text]

### Internal notes

[observations about what to emphasize if prospect responds]
```

Update the prospect status to "proposal-ready" and register in History.

## Output

Respond in **English** with:

### Proposal for [Prospect Name]

**Suggested package:** [name] | **Price range:** [value] | **Tone:** [description]

**Proposal:**
```
[ready-to-send text — copy and paste]
```

**Data used from research:**
- [list of specific prospect data used in proposal]

**Internal notes:**
- [observations about what to emphasize if they respond]
- [risks or points of attention]

**Next step:** [What to do after sending — when to follow-up, etc.]

## Rules

- Proposal must be based on REAL prospect data — if no research, suggest running `/prospect-research` first.
- NEVER use generic language ("I can create a beautiful website for you!").
- ALWAYS open with observation about THE PROSPECT, not about you.
- Language of outcome and consequence, never technical features.
- If prospect is not ICP, adjust proposal (less customization investment, more direct).
- Follow tone defined in [[tone-of-voice]].
- The proposal MUST always persist in the vault — never exist only in conversation output.
