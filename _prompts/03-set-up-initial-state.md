# 03 - Setup Initial Brain State

Read all files in the `_knowledge/` folder that I already filled. Based on this information, generate the first real brain state by updating the `_memory/current-state.md` file.

## What to do

1. Read `_knowledge/about-me.md` and extract: name, field, role, tools
2. Read `_knowledge/goals.md` and extract: goals prioritized by timeframe
3. Read `_knowledge/projects.md` and extract: active projects with status and next step
4. Read `_knowledge/references.md` and extract: relevant tools and resources
5. If `_knowledge/business/` exists, read those files and extract business context

## current-state.md Format

Keep the existing YAML frontmatter, update the date, and fill with real data:

```markdown
---
tags: [memory, state, current]
status: active
created: [keep original date]
updated: [today's date]
---

# Current State

## Last Update: [today's date] (initial state configured)

### What Was Done
- Initial second brain setup
- Knowledge base filled: [list which files were filled]
- Initial state generated from _knowledge/ data

### Decisions Made
None recorded yet — use `/end-session` to start accumulating.

### Current Phase
[Infer from goals.md + projects.md combination. Ex: "Initial phase - 2 active projects, focus on [short-term goal]"]

### Next Steps
[Infer from projects and goals. List 3-5 concrete actions ordered by priority.]

1. [Action from highest priority project]
2. [Action from second project/goal]
3. [Next step from short-term goal]

### Open Questions
[List pending questions inferred from data. If none, use:]
- Which projects deserve more time this week?
- Does any short-term goal need adjustment?
```

## After generating

1. Confirm what was done and which files were read
2. Show a 3-line summary of the generated state
3. Explain how to run `/daily-briefing` to test: "In Claude Code, inside the vault folder, type `/daily-briefing`"
4. If any file in `_knowledge/` still has placeholders, warn which ones are still empty

## Rules

- Don't invent data — use only what's extracted from files
- If a file is empty or only has placeholders, register as "not filled yet"
- Keep clean format with clear markdown headers
- Use **English** with correct spelling
