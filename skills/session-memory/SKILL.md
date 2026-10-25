---
name: session-memory
description: Maintain local, plain-Markdown long-term memory across Codex sessions. Use when starting or resuming work in a known workspace, when the user asks to remember or recall something, or when finishing substantial work that should survive a new session. Do not use for transient details, secrets, or full conversation transcripts.
metadata:
  short-description: Local memory across Codex sessions
---

# Session Memory

Keep durable context in `~/.codex/memory/` so a new Codex session can resume without replaying the conversation. Memory is plain Markdown, local-only, and user-inspectable.

## Layout

- `INDEX.md`: compact global index with user preferences, active projects, important decisions, and pointers.
- `projects/<slug>.md`: one file per workspace, covering goal, current state, decisions, constraints, next steps, and important paths.
- `sessions/YYYY-MM-DD.md`: append-only daily log covering what changed, why, verification, and open questions.

Use a stable project slug derived from the workspace path. For example, `E:\ccc` becomes `ccc`.

## Recall

At the start of work in a workspace:

1. Read `INDEX.md`.
2. Read the matching project file and the latest relevant session note.
3. If the workspace is not indexed, search `sessions/` for its path before concluding that no memory exists.
4. Load only what the current task needs. Do not dump memory into the reply.
5. Treat memory as context, not authority. The current user instruction wins; if it conflicts, follow the user and record the change.

## Record

After substantial work, or when the user says "记住" or "remember":

1. Update the project file with durable facts: goal, state, decisions and reasons, constraints, next steps, and important paths.
2. Append a short entry to today's session log with the date, work done, verification, and open questions.
3. Update `INDEX.md` only when the project list, a user preference, or a cross-project decision changed.
4. Keep entries concise and date-stamped. Prefer facts that change future decisions over narration.
5. Keep a short `## Wake-up card` at the top of each project file: goal, current state, next action, and any blocker.

## Boundaries

- Never store API keys, passwords, tokens, private keys, or full conversation transcripts.
- Do not store guesses as facts. Mark uncertainty explicitly.
- Do not send memory to a network service or install a background service for it.
- Keep `INDEX.md` under roughly 80 lines; move detail into project files.
- Use the `memory-compact` skill when the index approaches that limit or project/session files contain duplicates.
- If the user asks to forget something, remove it from all memory files and state what was removed.
