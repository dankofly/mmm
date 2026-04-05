# Claude Code Full Course — 6-Step Learning Path

**Source:** Sabrina Ramonov — "The ULTIMATE Claude Code Tutorial"
**Duration:** 90 minutes
**Goal:** Build a personalized AI Marketing Officer

## Prerequisites

- Claude Code installed (VSCode extension recommended)
- Blotato account with connected social media
- Blotato API key
- Use Opus 4.6 model

## Step 1: Create the `/post` Skill

Build a slash command that publishes to a single platform via Blotato API.

**Test:** `/post "ChatGPT prompt tips for beginners" twitter`

**Key concepts:** Skill architecture, async API polling patterns.

## Step 2: Add Per-Platform Brand Voice

Add platform-specific writing guidelines and 10+ voice samples per platform.

**Rules:**
- Short sentences, active voice
- Banned words list (same as humanize prompt)
- No AI patterns: metaphors, cliches, passive voice

**Test:** `/post "tips" linkedin` vs `/post "tips" twitter` — outputs should differ significantly.

## Step 3: Create Quality Gate Hook

Auto-validate before publishing:
- Em dashes (replace with "...")
- Character limits per platform
- Missing media check
- Banned word detection

Hooks run automatically without manual invocation.

## Step 4: Multi-Platform with Subagents

Modify `/post` to accept "all" — spawns parallel subagents per platform.

**Test:** `/post "Ski tips on icy conditions" all`

Reduces posting from ~2 min sequential to ~30 sec parallel.

## Step 5: Create `/plan-week` Skill

One sentence in → full week of content out.

**Workflow:**
1. Accept topic/URL/drafts/images
2. Research via Blotato API
3. Generate `content-plan.md` with per-post details
4. Request approval
5. Spawn subagents to publish in parallel

**Test:** `/plan-week "Ski tips for beginners"`

## Step 6: Create CLAUDE.md

Persistent project memory. Include:
- API documentation links
- Environment variable references
- Brand voice file location
- Quality gate config
- Published posts log

## End Result

```
/plan-week "one sentence topic"
```
→ Claude researches, drafts, generates visuals, shows plan, publishes to 4+ platforms in parallel.

---

# 30 Claude Code Concepts for Normal People

**Source:** Sabrina Ramonov — "Every Claude Code Concept Explained"

## Getting Started
1. **Terminal** — text-based interface replacing browser copy-paste
2. **Installation** — Max ($100-200/mo unlimited) or Pro ($20/mo limited)
3. **File Access** — reads/edits files directly on your computer
4. **Image + PDF Reading** — processes screenshots, PDFs, diagrams

## First Tasks
5. **Tool Use** — executes actions (read, edit, search, command)
6. **How to Talk** — be specific, use @file tags, ask clarifying questions
7. **CLAUDE.md** — instruction file read at conversation start
8. **Plan Mode** — outlines approach before making changes

## How Claude's Brain Works
9. **Context Window** — working memory with limited capacity
10. **Tokens + Costs** — use /clear, /compact, switch models
11. **Model Selection** — Opus (smart), Sonnet (balanced), Haiku (fast)

## Managing Conversations
12. **/compact** — summarize to free whiteboard space
13. **/clear** — wipe for clean-slate new tasks
14. **Session Management** — `claude --resume` to continue

## Controlling Claude
15. **Permission Modes** — "ask before edits" to "autonomous"
16. **Effort Levels** — low/high, "ultrathink" for max reasoning
17. **Interrupt** — Escape to stop and redirect

## Reviewing + Teaching
18. **VSCode** — see changes highlighted side-by-side
19. **Memory** — Claude's personal preference notebook
20. **Project vs Global Scope** — per-project vs everywhere settings

## Skills + Automation
21. **Slash Commands** — /help, /clear, /compact, /model, /usage, /insights
22. **Skills** — saved workflows triggered by single commands
23. **Hooks** — automated guardrails before/after actions

## Connecting to the World
24. **Web Browsing** — fetch and analyze public web pages
25. **MCP Servers** — bridge to Google Drive, Slack, Notion, Stripe
26. **Perplexity MCP** — AI-powered research with citations

## Agents + Scheduling
27. **Subagents** — parallel workers for independent tasks
28. **Remote Control** — continue from mobile via QR code
29. **Scheduled Tasks** — /loop for recurring tasks
30. **Git** — version control with rollback capability
