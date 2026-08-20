# AGENTS.md

<!--
WHAT THIS FILE IS
-----------------
AGENTS.md is the README you write for your coding agent instead of for a human.
An agent reads it at the start of every session, so it should carry the things
that are true across the whole project and NOT obvious from reading the code.

RULES OF THUMB
  - Write for a competent new teammate, not a search engine. Short, declarative.
  - Prefer commands over prose: an agent can run `npm test`, it can't run "test it".
  - If the code already says it clearly, leave it out. Duplication rots.
  - Keep it under ~1-2 pages. A bloated file gets skimmed and ignored.
  - Update it when it becomes wrong. A stale line is worse than a missing one.

Delete every comment block like this one before you hand the file off.
-->

## Project Overview

<!--
Two to four sentences. What this thing is, who it's for, and what problem it
solves. Enough context that the agent's first guess about an unfamiliar file
lands in the right neighborhood.
-->

_e.g. A Flask API that serves practice problems to students and grades their
submissions. Single-tenant, deployed to one Heroku dyno. Students never touch
the DB directly — everything goes through the API layer._

## Tech Stack

<!--
Language + version, framework, database, package manager, and anything with a
non-obvious version pin. Versions matter: an agent that assumes the wrong
major version will write code that looks right and doesn't run.
-->

- **Language:**
- **Framework:**
- **Database:**
- **Package manager:**
- **Notable dependencies:**

## Setup

<!--
The exact sequence to get from a fresh clone to a running app. Include the
env-var story: which file, which keys, where the real values come from
(and never put actual secrets in this file).
-->

```bash
# install
# configure (e.g. cp .env.example .env)
# run
```

## Commands

<!--
The single highest-value section. If an agent knows nothing else, it should
know how to build, test, and lint. Give the real invocation, including any
flags you actually use.
-->

| Task | Command |
| --- | --- |
| Run dev server | |
| Run all tests | |
| Run a single test | |
| Lint | |
| Format | |
| Type check | |
| Build | |

## Project Structure

<!--
A shallow map — top-level directories and one line each. Don't paste a full
tree; it'll be out of date by Friday. Call out anything counterintuitive:
generated directories, code that lives somewhere surprising, dirs to not touch.
-->

```
src/        —
tests/      —
scripts/    —
```

## Code Style & Conventions

<!--
Only the things a linter won't catch and the agent can't infer: naming
patterns, preferred idioms, error-handling style, how you structure a new
module. If your formatter already enforces it, don't restate it here.
-->

- 
- 

## Testing

<!--
Where tests live, what framework, what the naming pattern is, and — most
importantly — your expectation. Should the agent write tests for every change?
Must the suite pass before it claims to be done? Say so explicitly.
-->

- **Framework:**
- **Location / naming:**
- **Expectation:**

## Git & PR Workflow

<!--
Branch naming, commit message format, whether the agent may commit and push on
its own, and what a PR needs before review. Be explicit about autonomy — the
default assumption should be "ask first."
-->

- **Branching:**
- **Commits:**
- **Agent may commit/push:** (yes / ask first / no)

## Guardrails

<!--
The "do not" list. Anything destructive, expensive, or outward-facing:
production credentials, live databases, migrations, deploys, third-party APIs
that cost money or send real email. Being specific here is what makes it safe
to give the agent a long leash everywhere else.
-->

- Never
- Never
- Always ask before

## Gotchas

<!--
Institutional knowledge — the stuff that cost you an afternoon. Flaky tests,
a service that must be running first, a config that looks unused but isn't,
a workaround that looks like a bug. This section earns its keep over time;
add a line every time you get surprised.
-->

- 

## Domain Glossary

<!--
Optional but valuable in any project with its own vocabulary. Terms whose
meaning here differs from their meaning in general use — especially where a
word names a specific model, table, or state in your system.
-->

| Term | Meaning |
| --- | --- |
| | |
