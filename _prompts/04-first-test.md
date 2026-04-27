# 04 - Validate Second Brain is Working

I want to test if the second brain is properly configured and ready for use. Do a complete check.

## Validation Checklist

### 1. Memory
- Read `_memory/current-state.md`
- Tell me a 3-line summary of current state
- Check if date is updated (cannot be placeholder `[TODAY'S DATE]`)
- Check if sections have real content (not just placeholders)

### 2. Knowledge base
- Read each file in `_knowledge/` (about-me, goals, projects, references)
- For each, say: filled / partially filled / still with placeholders
- If `_knowledge/business/` exists, check those too

### 3. Folder structure
Check if all folders exist:
- `_memory/`, `_knowledge/`, `_learnings/`, `_decisions/`, `_pipeline/`, `_sessions/`, `_prompts/`, `.claude/commands/`
- If any are missing, say exactly which ones

### 4. Slash commands
- List all files in `.claude/commands/`
- For each, read first line and briefly describe what it does
- If any essential command is missing (daily-briefing, end-session, braindump, weekly-review), warn

### 5. AGENTS.md
- Check if AGENTS.md exists and is filled
- Check if identity section (Section 2) has real data or still has `[YOUR NAME]`
- Check if vault structure in AGENTS.md reflects actual folder structure

### 6. Functional test
- Run `/daily-briefing` and show complete output
- If output mentions non-existent data or broken references, flag it

## Output

Respond with:

### Second Brain Diagnosis

**Overall score:** [X/10]

| Component | Status | Note |
|-----------|--------|------|
| Memory (current-state) | [OK / Pending / Error] | [detail] |
| Knowledge base | [X/4 filled] | [which ones missing] |
| Business module | [Active / Not configured / Removed] | [detail] |
| Folder structure | [Complete / Missing X] | [which missing] |
| Slash commands | [X/8 available] | [which missing] |
| AGENTS.md | [Configured / Pending] | [what's missing] |
| Functional test | [Passed / Failed] | [detail] |

**What's needed to reach 10:**
[Concrete list of what needs to be done, ordered by priority]

**Recommended next step:**
[Most important action to take now]
