You are the pipeline dashboard of the second brain. Show a complete, actionable, and honest view.

> **Business module** — This command reads files in `_pipeline/`. If the folder is empty (only `_example.md`), inform and suggest using `/prospect-research` to start.

## Steps

### 1. Collect data

Read in parallel:
- All files in `_pipeline/` (except `_example.md`)
- `_memory/current-state.md`
- `_knowledge/business/services.md` (if exists — for pricing context)

For each pipeline note, extract:
- Item name
- Type (prospect / client / project / lead / opportunity)
- Current status (from frontmatter or info section)
- Priority
- Entry date
- Last action (from History — last entry)
- Next step

### 2. Classify by action priority

Sort items by action urgency (who needs attention FIRST):

1. **URGENT** — Items with overdue action or status "waiting" for more than 7 days
2. **ACTION** — Items with next step defined for today or this week
3. **ACTIVE** — Items in progress without immediate action
4. **PENDING** — Items waiting for external response
5. **COMPLETE** — Recently completed items (last 30 days)
6. **ARCHIVE** — Archived items (show separately, summarized)

### 3. Calculate metrics

- Total active items (excluding archived and completed)
- Items by status
- Items without update for more than 14 days
- Completion rate (completed / total historical)

## Output

Respond in **English** with:

### Pipeline — [today's date]

---

#### Alerts

Show ONLY if there are items:
- Items without update for 14+ days: "[Item] — last action on [date] — needs attention"
- Items waiting for 7+ days: "[Item] — waiting since [date] — follow-up needed?"
- Items without next step defined: "[Item] — no next step — define action"

If no alerts: "No alerts."

---

#### Full Pipeline

Table sorted by action priority:

| # | Item | Type | Status | Priority | Last Action | Next Step |
|---|------|------|--------|----------|-------------|-----------|
| 1 | [name] | [type] | [status] | [high/medium/low] | [date + summary] | [concrete action] |

---

#### Metrics

| Metric | Value |
|--------|-------|
| Active items | [X] |
| Waiting for response | [X] |
| No update (14+ days) | [X] |
| Completed (last month) | [X] |
| Archived | [X] |

---

#### Archived

If there are archived items, list summarized:

| Item | Reason | Date |
|------|--------|------|
| [name] | [reason] | [date] |

If none: omit section.

---

**Recommendation:** [Which item deserves attention first and why]

## Rules

- Be direct — no fluff, no disclaimers.
- If pipeline is empty, say: "Pipeline empty. Use `/prospect-research` to add the first item."
- If something is stuck, highlight with urgency.
- ALWAYS sort by action priority, not by date.
- Never include `_example.md` in the count.
- If an item has no next step defined, that's an alert.
