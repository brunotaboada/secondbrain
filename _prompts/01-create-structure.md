# 01 - Create Second Brain Structure

Create the complete structure of a second brain in this directory. The goal is to have an organized vault in Obsidian where I can store knowledge, record decisions, capture learnings, and maintain an updated state of everything I'm doing. Claude Code will use these files as persistent memory across sessions.

## Folders to create

- `_memory/` - Current state and persistent context between sessions
- `_knowledge/` - Personal knowledge base (who I am, goals, projects, references)
- `_knowledge/business/` - Optional business module (positioning, ideal customer, services, prices, voice)
- `_learnings/` - Documented insights and learnings over time
- `_decisions/` - Log of important decisions with date, context, and reasoning
- `_pipeline/` - Active items (projects, tasks, prospects, or whatever you use)
- `_sessions/` - Braindumps and work session logs
- `_prompts/` - Setup and configuration prompts (where this file lives)
- `.claude/commands/` - Brain's slash commands

## Files to create

### `_memory/current-state.md`
Current state template with YAML frontmatter:
```yaml
---
tags: [memory, state, current]
status: active
created: [today's date]
updated: [today's date]
---
```
Mandatory sections with fill-in instructions between brackets:
- `# Current State`
- `## Last Update:` [date] (first setup)
- `### What Was Done` - list of what was done in last session
- `### Decisions Made` - strategic decisions made
- `### Current Phase` - current phase of what you're doing
- `### Next Steps` - concrete next steps, ordered by priority
- `### Open Questions` - pending questions or decisions

### `_pipeline/_example.md`
Universal pipeline item template with YAML frontmatter (tags: [pipeline, example], status: template). Include:
- Basic Info table (name, type, status, priority, entry date, owner, source)
- Sections: Context, Analysis, Next Steps, History (with date format), Internal Notes
- Related section with WikiLinks to `[[projects]]` and `[[goals]]`
- Note explaining `_pipeline/` can be renamed (devs: `_projects/`, students: `_assignments/`, etc.)

### `.gitignore`
Ignore: `.obsidian/`, `.DS_Store`, `Thumbs.db`, `node_modules/`, `*.swp`

### `_learnings/.gitkeep`, `_decisions/.gitkeep`, `_sessions/.gitkeep`
Empty files to keep folders in Git.

## Rules

- Use YAML frontmatter in every .md file (tags, status, created, updated)
- All placeholders must be in brackets: `[Describe here]`
- Include practical examples in brackets with "Ex:": `[Ex: web development, design]`
- Do NOT create AGENTS.md — it already exists in this vault
- Do NOT fill real content in files — only structure with placeholders and instructions
- Use **English** with correct spelling throughout
