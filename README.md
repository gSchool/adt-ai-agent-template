# adt-ai-agent-template

A starter template for the one file that makes a coding agent useful on your project: **`AGENTS.md`**.

`AGENTS.md` is the README you write for an agent instead of for a human. The agent reads it at the
start of every session, so it should carry the things that are true across the whole project and
that aren't obvious from reading the code — how to run the tests, what not to touch, which surprises
have already cost someone an afternoon.

This repo contains a single file, `AGENTS.template.md`: a skeleton with every section stubbed out and
a commented explanation of what belongs in it (and what doesn't).

## ⚠️ Rename the file first

The template ships as `AGENTS.template.md` so it doesn't get picked up as-is. **Agents look for a file
named `AGENTS.md`** — until you rename it, nothing will read it.

```bash
mv AGENTS.template.md AGENTS.md
```

Some tools use a different filename. If yours does, name the file accordingly (or symlink it):

| Tool | Filename |
| --- | --- |
| Claude Code | `CLAUDE.md` (also reads `AGENTS.md`) |
| Cursor, Codex, Copilot, Gemini CLI, Aider, and most others | `AGENTS.md` |

```bash
# Claude Code, keeping one source of truth
mv AGENTS.template.md AGENTS.md
ln -s AGENTS.md CLAUDE.md
```

## How to use it

1. **Copy it into your project.** Drop the file at the repo root — that's where agents look.
2. **Rename it** (see above).
3. **Fill it in top to bottom.** Leave a section blank rather than guessing; a wrong line is worse
   than a missing one.
4. **Delete the `<!-- -->` comment blocks.** They're instructions for you, not context for the agent.
   Every one of them costs tokens and dilutes the parts that matter.
5. **Commit it.** It's project documentation and belongs in version control alongside the code.

## What's in the template

| Section | What it's for |
| --- | --- |
| Project Overview | Two to four sentences so the agent's first guess lands in the right neighborhood |
| Tech Stack | Language, framework, DB, package manager — with **versions** |
| Setup | Fresh clone → running app, including the env-var story |
| Commands | Build, test, lint, format, typecheck. The highest-value section in the file |
| Project Structure | A shallow map of top-level directories, plus anything counterintuitive |
| Code Style & Conventions | Only what a linter won't catch and the agent can't infer |
| Testing | Framework, location, and your explicit expectation of the agent |
| Git & PR Workflow | Branch and commit conventions, and whether the agent may push on its own |
| Guardrails | The "do not" list: prod credentials, live data, deploys, APIs that cost money |
| Gotchas | Institutional knowledge — the stuff that surprised you once already |
| Domain Glossary | Terms whose meaning here differs from general use |

## Guidelines worth repeating

- **Commands over prose.** An agent can run `npm test`; it can't run "test it".
- **Keep it to one or two pages.** A bloated file gets skimmed and ignored.
- **Don't restate the code.** If the code says it clearly, leave it out — duplication rots.
- **Be explicit about autonomy.** "Ask before committing" is a sentence the agent will actually follow.
- **Update it when it goes stale.** Add a line to Gotchas every time something surprises you.
