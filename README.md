# agent-os 🧠

A filesystem-first personal operating system for Cursor & Claude Code agents — persistent memory (`memory.md`), lean identity context (`context/`), a 3-layer research archive (`research/`), and reusable skills (`.cursor/skills/`).

Instead of re-explaining who you are, how your repos are wired, and what mistakes the agent made yesterday, point your editor at one central `OS/` workspace.

```text
agent-os/
├── AGENTS.md                        # Root entrypoint & operating rules
├── memory.md                        # Self-updating learned rules (updated on every correction)
├── todo.md                          # Living inbox (Now <= 5 items + pillar sections)
├── context/                         # Stable identity (who we are — not research dumps)
│   ├── about-me.md
│   └── tools-stack.md
├── research/                        # Three-layer knowledge base (index -> log -> canonical)
│   ├── README.md
│   ├── index.md
│   └── logs/_template.md
└── .cursor/
    ├── rules/personal-os.mdc        # Always-applied workspace rule
    └── skills/                      # Repeatable SOPs invoked via /skill-name
        ├── youtube-to-os/SKILL.md   # Turn any YouTube URL into an actionable skill
        └── site-audit/SKILL.md      # Technical SEO, JSON-LD schema & GEO audit SOP
```

## Core Architecture

### 1. The Correction Loop (`memory.md`)

Every time you correct the agent ("don't run `supabase start`", "use `rg` instead of `grep`", "keep answers under 5 lines"), the agent appends a permanent rule to `memory.md`. Before every task, the agent reads `memory.md` so you never repeat the same correction twice.

### 2. Context vs. Research Separation

Most agent setups rot because every note gets dumped into one folder, blowing up the context window. `agent-os` enforces a strict split:
- **`context/` is stable identity** — who you are, your stack, your voice. Loaded selectively per task.
- **`research/` is what you learn** — a 3-layer model:
  1. `research/index.md` — scannable one-row-per-study catalog
  2. `research/logs/YYYY-MM-DD-slug.md` — dated deep dives, SERP studies, tool evaluations
  3. Canonical playbooks — distilled rules promoted out of logs once proven

### 3. Skills as Repeatable SOPs (`.cursor/skills/`)

When a workflow works once, capture it as a `SKILL.md` so you can run `/youtube-to-os` or `/site-audit` in one command.

## Quick Start

```bash
git clone https://github.com/zaynelovecraft/agent-os.git ~/Repos/OS
cd ~/Repos/OS
```

1. Fill in `context/about-me.md` and `context/tools-stack.md`.
2. Open `~/Repos/OS` in Cursor (or run `claude` from the root).
3. Correct the agent once — watch it write the rule to `memory.md`.

## License

MIT
