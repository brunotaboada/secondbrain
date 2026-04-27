# Personalization Guide

How to transform the generic template into **your** second brain. Works for any profile.

**Estimated time:** 15-30 minutes for basic setup. You can fill in over time.

---

## Step 1: Fill Your Identity in AGENTS.md

Open `AGENTS.md` and go to **Section 2 — Identity**. Fill the fields:

- **Name:** Your name
- **Field:** What you do
- **Role:** Your current role
- **Main Goal:** What you're pursuing now
- **Main Tools:** What you use daily
- **Tech Stack:** Your technologies (if applicable)

### Examples by profile

**Web design freelancer:**
```
- Name: Marina Costa
- Field: Design and development of websites for local businesses
- Role: Solo freelancer
- Main Goal: Get 5 recurring clients in the next 6 months
- Main Tools: Figma, VS Code, Obsidian, Claude Code
- Tech Stack: HTML, CSS, JavaScript, WordPress, Elementor
```

**Startup developer:**
```
- Name: Lucas Pereira
- Field: Full-stack development
- Role: Senior dev at TechCo
- Main Goal: Lead the migration from monolith to microservices
- Main Tools: VS Code, GitHub, Linear, Slack, Claude Code
- Tech Stack: TypeScript, React, Node.js, PostgreSQL, AWS
```

**Software engineering student:**
```
- Name: Ana Souza
- Field: Software Engineering (final year)
- Role: Student + intern
- Main Goal: Finish thesis and get permanency at internship
- Main Tools: IntelliJ, Obsidian, Google Docs, Claude Code
- Tech Stack: Java, Spring Boot, MySQL
```

**Content creator:**
```
- Name: Pedro Almeida
- Field: Technology and productivity content
- Role: Content creator on Instagram and YouTube
- Main Goal: Reach 50k followers and launch first info-product
- Main Tools: CapCut, Canva, Obsidian, Claude Code
- Tech Stack: N/A
```

**Project manager:**
```
- Name: Carla Mendes
- Field: IT project management
- Role: PM at a tech consultancy
- Main Goal: Organize 4 simultaneous projects and reduce delays
- Main Tools: Jira, Confluence, Slack, Obsidian, Claude Code
- Tech Stack: N/A (management, not coding)
```

### Adjust language rules (if needed)

In **Section 0 — Language Rules**, the default is everything in English. Adjust if needed:
- If you work with international clients, you might want outputs in another language
- If you prefer vault in a different language, change the vault language rule

---

## Step 2: Fill the Knowledge Base

Open each file in `_knowledge/` and fill the guide questions. No need to fill everything at once — start with the essentials:

### Recommended order

1. **[[about-me]]** — Most important. The brain needs to know who you are to contextualize everything.
2. **[[goals]]** — Your objectives. Without these, `/daily-briefing` can't prioritize.
3. **[[projects]]** — Your active projects. Delete the fake examples and add yours.
4. **[[references]]** — Links and tools. Can fill gradually.

### Tip: use the prompts

If you prefer having Claude Code help you fill them, use the prompts from `_prompts/` folder:

1. Open Claude Code in the vault folder
2. Copy and paste the content of `_prompts/03-set-up-initial-state.md` in the chat
3. Claude will read what you filled and generate the initial state

---

## Step 3: Business Module (OPTIONAL)

If you use the second brain to manage a business (freelancing, agency, consulting, etc.), fill the files in `_knowledge/business/`:

1. **[[positioning]]** — What you do, for whom, what problem you solve
2. **[[icp]]** — Who's your ideal client
3. **[[services]]** — Your services and price ranges
4. **[[pricing]]** — How you price
5. **[[tone-of-voice]]** — How you communicate

This activates the business commands: `/prospect-research`, `/pipeline`, `/proposal-generator`.

### If you DON'T need the business module

You can simply ignore the `_knowledge/business/` folder. The 5 universal commands work without it.

If you want a full cleanup:
1. Delete the `_knowledge/business/` folder
2. In `AGENTS.md`, remove the entire **Section 5 — Business Module**
3. Delete commands: `prospect-research.md`, `pipeline.md`, `proposal-generator.md` from `.claude/commands/`

---

## Step 4: Test Commands

Run each command and see if the output makes sense:

```
/daily-briefing
```
Should show your projects, priorities, and next steps.

```
/braindump I'm thinking about shifting project X focus to Y because...
```
Should capture the idea, categorize, and connect to the vault.

```
/end-session
```
Should consolidate what you did, update current-state, and prepare context for next session.

If any command mentions data that doesn't exist or produces empty output, it means the knowledge base is missing data. Go back to Step 2.

---

## Step 5: Consolidate Initial State

After filling the knowledge base and testing, run:

```
/end-session
```

This will generate the first real state of the brain in `_memory/current-state.md`. From now on, the brain is operational.

---

## Advanced Tips

### Create New Slash Commands

Create a `.md` file in `.claude/commands/` with this structure:

```markdown
You are the brain's [role]. [What it does].

## Arguments

$ARGUMENTS contains: [what the user passes]

## Steps

1. [What to do first]
2. [What to do next]

## Output

[Expected response format]

## Rules

- [Specific guardrails]
```

The command becomes automatically available as `/file-name`.

### Rename Folders

Folders are conventions, not fixed rules. Rename according to your use:

| Default | Alternatives |
|---------|--------------|
| `_pipeline/` | `_clients/`, `_projects/`, `_tasks/`, `_assignments/` |
| `_learnings/` | `_notes/`, `_insights/`, `_til/` |
| `_sessions/` | `_journal/`, `_logs/` |

If you rename, update references in slash commands and AGENTS.md.

### Add Modules

You can create new knowledge folders for specific themes:

- `_knowledge/content/` — Content strategy, editorial calendar
- `_knowledge/studies/` — Subjects, schedules, class notes
- `_knowledge/health/` — Routines, workouts, health goals

And create slash commands that query these modules.

---

## Summary

| Step | What to do | Time |
|------|-------------|------|
| 1 | Fill identity in AGENTS.md | 5 min |
| 2 | Fill knowledge base (about-me, goals, projects) | 10-20 min |
| 3 | Business module (if using) | 10-15 min |
| 4 | Test commands | 5 min |
| 5 | Run `/end-session` to consolidate | 2 min |

**Total:** 15-30 minutes for basic setup. The brain gets smarter with use — each `/end-session` feeds the memory.
