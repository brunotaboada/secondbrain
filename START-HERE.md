# Welcome to Your Second Brain

You just acquired a persistent memory system for Claude Code. It will remember who you are, what you do, your projects, your decisions, and your learnings — across sessions, without needing to re-explain everything.

---

## What You Got

| Component | What it does |
|-----------|--------------|
| **AGENTS.md** | The brain's soul — defines how Claude thinks, operates, and protects your data |
| **8 slash commands** | Ready-to-use commands that execute complex tasks in one line |
| **Knowledge templates** | Guide questions for you to fill so the brain gets to know you |
| **Business module** | Extra templates and commands for using the brain to manage a business (optional) |
| **4 setup prompts** | Same prompts from the video + complementary ones for full setup |
| **Complete guides** | Step-by-step installation and personalization by profile |
| **AI support** | A prompt that transforms any LLM into an assistant that knows the entire kit |

---

## Setup in 3 Steps

### Step 1: Install and open

Follow the [[setup-guide]] to install Obsidian and Claude Code (if you don't have them yet), and open the vault.

**If you already have Obsidian and Claude Code installed:** Just open this folder as a vault in Obsidian and run `claude` in the terminal inside it.

### Step 2: Personalize

Follow the [[personalization-guide]] to fill your identity in AGENTS.md and feed the brain with your data.

**Estimated time:** 15-30 minutes for basic setup. You can keep filling in over time.

### Step 3: Test

Run your first command in Claude Code:

```
/daily-briefing
```

If everything is configured, the brain will generate a briefing of your day based on what you filled.

---

## Your Commands

### Universal (everyone uses)

| Command | What it does |
|---------|--------------|
| `/daily-briefing` | Generates daily briefing: current state, projects, priorities, next steps |
| `/end-session` | Closes session: saves what was done, decisions, learnings. **The brain evolves with each use.** |
| `/braindump [text]` | Captures an idea or thought and automatically connects it to the vault |
| `/weekly-review` | Weekly review: what advanced, what stalled, priority adjustments |

### Semi-universal

| Command | What it does |
|---------|--------------|
| `/content-idea` | Generates content ideas based on your profile, goals, and positioning |

### Business module (optional)

| Command | What it does |
|---------|--------------|
| `/prospect-research [name]` | Researches a prospect and creates pipeline note |
| `/pipeline` | Complete dashboard of your funnel with metrics and alerts |
| `/proposal-generator [name]` | Generates personalized proposal based on vault data |

---

## Need Help?

Open the [[llm-support-prompt]] file and copy the entire content as the first message in a new Claude (web) or ChatGPT chat. You'll have an assistant that knows the entire kit and can help with any question — personalization, troubleshooting, creating new commands, everything.

---

## Vault Structure

```
AGENTS.md                    ← Brain's soul (personalize first)
START-HERE.md                ← You are here
setup-guide.md               ← Step-by-step setup
personalization-guide.md     ← How to adapt to your use
llm-support-prompt.md        ← AI support

_prompts/                    ← Prompts used in the video
_memory/                     ← Current state (auto-updated)
_knowledge/                  ← Your knowledge base
  business/                  ← Business module (optional)
_pipeline/                   ← Active funnel items
_learnings/                  ← Accumulated learnings
_decisions/                  ← Decision log
_sessions/                   ← Braindumps and sessions
.claude/commands/            ← The 8 slash commands
```

---

> **Tip:** The second brain gets smarter with use. Every time you run `/end-session`, it consolidates what happened and prepares better for the next session. Use it consistently and within weeks it'll know your context better than any new chat.
