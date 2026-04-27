# Setup Guide

From zero to working vault. Follow in order.

---

## 1. Install Obsidian

Obsidian is the app you use to view and navigate vault notes. It's free.

1. Go to [obsidian.md/download](https://obsidian.md/download)
2. Download for your system (Windows, Mac, or Linux)
3. Install normally

---

## 2. Open the vault in Obsidian

1. Extract the .zip kit file to an easy-access folder (ex: `Documents/second-brain/`)
2. Open Obsidian
3. Click **"Open folder as vault"**
4. Select the `second-brain/` folder you extracted
5. Obsidian will open with all notes visible in the sidebar

**You should see in the sidebar:** `_knowledge/`, `_memory/`, `_pipeline/`, `_decisions/`, `_learnings/`, `_prompts/`, `_sessions/`

---

## 3. Install Claude Code

Claude Code is the command-line tool that runs the brain's slash commands. It requires Node.js.

### 3a. Install Node.js (if you don't have it)

1. Go to [nodejs.org](https://nodejs.org)
2. Download **LTS** version (recommended)
3. Install normally
4. Verify installation by opening terminal and typing:
   ```
   node --version
   ```
   Should show something like `v20.x.x` or higher.

### 3b. Install Claude Code

In terminal, type:
```
npm install -g @anthropic-ai/claude-code
```

Verify installation:
```
claude --version
```

### 3c. Authenticate

In terminal, type:
```
claude login
```

Follow instructions to connect your Anthropic account. You need an active Claude subscription (Pro, Max, or API).

---

## 4. Open Claude Code in the vault

Navigate to the vault folder in terminal and start Claude Code:

```
cd ~/Documents/second-brain
claude
```

**On Windows:**
```
cd C:\Users\YourUser\Documents\second-brain
claude
```

When Claude Code opens, it will automatically read `AGENTS.md` and already be configured with the second brain rules.

---

## 5. Verify it works

Run the test command:

```
/daily-briefing
```

If everything is correct, the brain will generate a briefing (even if still with placeholders, it works). If there's an error, see Troubleshooting below.

---

## 6. Next step

Go to [[personalization-guide]] and fill your identity and knowledge base. This is what transforms the generic template into **your** second brain.

---

## Optional: Sync with Git

If you want vault backup and history, you can sync with GitHub.

### Option A: Via terminal (recommended for devs)

```
cd ~/Documents/second-brain
git init
git add .
git commit -m "initial second brain setup"
```

Create a **private** repository on GitHub and connect:
```
git remote add origin https://github.com/your-username/second-brain.git
git push -u origin main
```

### Option B: Via Obsidian Plugin

1. In Obsidian, go to **Settings → Community plugins**
2. Disable **Restricted mode**
3. Search and install **Obsidian Git** plugin
4. Configure plugin with your GitHub repository
5. Plugin does automatic commit and push every X minutes

**Important:** If using Git, make sure the repository is **private**. Your vault contains personal information.

---

## Troubleshooting

### "claude: command not found"
Claude Code wasn't installed globally. Try:
```
npm install -g @anthropic-ai/claude-code
```
If it persists, check if global npm is in system PATH.

### "Error: AGENTS.md not found"
You opened Claude Code in the wrong folder. Verify you're inside the `second-brain/` folder:
```
ls AGENTS.md
```
If it doesn't show, navigate to correct folder with `cd`.

### "Authentication error"
Run `claude login` again. Check if your subscription is active at [console.anthropic.com](https://console.anthropic.com).

### Obsidian doesn't show folders
Verify you opened the `second-brain/` folder as vault, not a folder above or below. The vault root folder must contain `AGENTS.md`.

### Slash commands don't appear
Commands are in `.claude/commands/`. The `.claude` folder is hidden by default. In Obsidian, go to **Settings → Files and Links** and enable **Show hidden files**. In terminal, use `ls -la` to see the folder.

### "Do I need Claude Max/Pro?"
The kit works with any Claude Code plan (Pro, Max, or API). It requires no specific plan — it's an accelerator for those already using Claude Code.
