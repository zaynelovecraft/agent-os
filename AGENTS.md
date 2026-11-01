# Personal Operating System

You are working inside my central OS folder. This is my command center — not an application codebase. Code lives in sibling repos under `../`.

## Before every task

1. Read `context/` for who I am, my stack, and my projects.
2. Read `memory.md` for learned preferences and past corrections.
3. Load only the context files relevant to the task (don't bloat the session).

## Repo map (sibling folders)

| Repo | Path | Notes |
|------|------|-------|
| my-app | `../my-app` | Next.js + Postgres |

## Todo list (`todo.md`)

| When | Do |
|------|-----|
| I mention something to do | Add one `- [ ]` line to the right section in `todo.md` (check for duplicates first) |
| I ask for my todo / what's next | Read `todo.md` and summarize — **Now** first, then open items by section |
| A task is completed in session | Mark `[x]` in `todo.md` |

## Research (`research/`)

**Save research on disk — not in chat.** `context/` is stable identity; `research/` is what we learn.

| When | Do |
|------|-----|
| After a site scan, benchmark, or tool eval | Create `research/logs/YYYY-MM-DD-slug.md` (copy `_template.md`) |
| Same session | Add one row to `research/index.md` |
| Findings are permanent / reusable | Merge into a canonical doc or `.cursor/skills/` and link the log |

## When I correct you

Add a clear, one-line rule to `memory.md` under **Learned rules**. Check `memory.md` before every task.

## How I like to work

- Goal -> result. Don't just advise — execute when I give you a task.
- Minimize scope. Match existing conventions in each repo.
- Lean context — high signal, no filler.
- Draft destructive actions (deploys, DB migrations, external messages) for approval first.
