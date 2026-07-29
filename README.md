# external-integrations-anakin

Anakin config snippets and submission drafts for AI coding clients that have
**no plugin marketplace to submit a package to** — the only install path for
each is a user pasting a JSON/YAML snippet into that client's own MCP
settings.

This is deliberately separate from
[`Anakin-Inc/agent-skills`](https://github.com/Anakin-Inc/agent-skills),
which holds genuine packaged plugins/skills (Claude Code, Codex, Grok,
Cursor, Gemini CLI, Copilot/VS Code) — those are real installable packages
with their own manifests. What's here isn't a skill or a package; it's
documentation of exactly what to paste where, verified per-client against
each vendor's current docs rather than assumed from a common convention.

## Clients covered

Windsurf, Cline, JetBrains AI Assistant, Goose, Kiro, LM Studio, Amp,
Augment Code, Qwen Coder, OpenCode, Zencoder, Trae, Raycast — see
[docs/CLIENTS.md](docs/CLIENTS.md) for the full snippet table, including
which clients actually expand `${VAR}`-style env references and which need
the literal key pasted in (getting this wrong doesn't error — the server
starts and lists all 21 tools, then fails every call with an auth error,
which is a confusing way to find out).

Two of these clients also have a real, submittable third-party directory
beyond just a config snippet — drafts for those are in
[docs/submissions/](docs/submissions/):

- [Cline](docs/submissions/cline.md) — `cline/mcp-marketplace`, GitHub issue submission
- [Raycast](docs/submissions/raycast.md) — a community-run (non-official) registry, PR-based

Filing either is a manual step for whoever owns the Anakin GitHub presence —
these files are prep, not filed submissions.

## API key

Get a free key at [anakin.io/dashboard](https://anakin.io/dashboard) — 300
credits, no card required.

## Why this repo exists

Every one of these clients was originally documented inside
`Anakin-Inc/agent-skills`, which is meant for actual skills/plugins. A
13-client PR sitting there mislabeled generic MCP config documentation as
"skills," so it was moved here — same content, correctly homed.
