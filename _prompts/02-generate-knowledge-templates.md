# 02 - Generate Knowledge Templates

Create knowledge templates in the `_knowledge/` folder to feed the second brain. These files are the foundation the brain uses to know you and contextualize everything you do.

## Rules for all templates

- Mandatory YAML frontmatter: `tags`, `status: active`, `created`, `updated`
- Each file starts with H1 header explaining its purpose
- Guide questions in checklist format (`- [ ] **Field:** [Ex: example]`)
- Practical examples in brackets with "Ex:" for each question
- Sections organized by theme with H2 headers
- Final tip (blockquote `>`) explaining how the file connects to slash commands
- Simple, direct language — no technical jargon in guide questions
- Use **English** with correct spelling

## Files to create

### 1. `_knowledge/about-me.md` — Who I Am
Tags: `[knowledge, identity, core]`

Sections:
- **Identity:** name, preferred name, field, current role, time in field
- **What I Do:** one-line description, what sets me apart, what I DON'T do
- **Main Skills:** hard skills, soft skills, currently learning
- **Tools and Stack:** daily tools, tech stack, AI tools I use
- **How I Prefer to Work:** productive hours, work style, preferred communication, what slows me down, what speeds me up
- **Personal Context (optional):** location, languages, timezone

Final tip: "You don't need to fill everything at once. Start with what seems most relevant and fill in over time. `/end-session` will remind you to update."

### 2. `_knowledge/goals.md` — My Goals
Tags: `[knowledge, goals, core]`

Introduction mentioning that `/weekly-review` uses this file.

Sections with 2 goals each (reusable template):
- **Short Term (next 30 days):** what success looks like, metrics, what's stopping me, next concrete step
- **Medium Term (next 6 months):** what success looks like, metrics, what I need to do first, risks or blockers
- **Long Term (next 1 year):** what success looks like, metrics, what needs to happen first, why this matters
- **Anti-goals (what I DON'T want):** list with examples (don't work 10h/day, don't take cheap clients, etc.)

Final tip: "`/weekly-review` will compare your goals with what you actually did this week."

### 3. `_knowledge/projects.md` — My Projects
Tags: `[knowledge, projects, core]`

Introduction mentioning that `/daily-briefing` uses this file.

Structure:
- **Template (copy for each project):** table with fields Status (not-started/in-progress/paused/completed/cancelled), Priority (high/medium/low), Start, Deadline, Next step, Blockers. Plus Description and Notes fields.
- **2 filled dummy examples** to demonstrate format:
  - Example 1: "Portfolio Redesign" — status in-progress, high priority, with deadline, real blocker, WikiLink to `[[references]]`
  - Example 2: "Advanced TypeScript Course" — status in-progress, medium priority, no deadline, no blockers
- Mark examples with "(delete after understanding format)"

Final tip: "When a project changes status, update here. `/end-session` will remind you."

### 4. `_knowledge/references.md` — References and Resources
Tags: `[knowledge, references, core]`

Sections with tables and lists:
- **Tools I Use:** table with Tool, What I use it for, Link (5 examples like VS Code, Obsidian, Figma)
- **Useful Links:** subsections for Documentation & Learning, Online Tools, Communities
- **People and Reference Profiles:** table with Person, Area, Why I follow them, Where to find
- **Saved Content:** subsections for Articles, Videos/Courses, Books, Templates and Examples

Final tip: "When `/braindump` captures a reference, it will suggest adding here automatically."
