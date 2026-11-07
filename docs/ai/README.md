# AI context index

This directory holds public-safe context that helps AI agents understand the owner and
his repositories. Start with [`../../AGENTS.md`](../../AGENTS.md).

| File | Purpose |
| --- | --- |
| [`context.md`](context.md) | Who Carmine is, what he works on, and how he works. |
| [`repositories.md`](repositories.md) | Catalog of public repositories and which context to read for a task. |
| [`conventions.md`](conventions.md) | Branch, commit, formatting, testing, and security conventions. |
| [`glossary.md`](glossary.md) | Terms used across the projects. |
| [`profile.json`](profile.json) | The same profile data in machine-readable form. |

## Rules for these files

- **Public-safe only.** No secrets, private data, customer information, or private network
  details.
- **Facts, not guesses.** If something is unknown, write `TBD` or mark it **(inferred)**.
- **Update the owner.** When a fact changes, update the file that owns it; do not create a
  near-duplicate.
- **Keep it short.** Another agent should be able to read the whole set in a few minutes.

## Quick map

```text
AGENTS.md                     Canonical agent contract
llms.txt                      LLM-friendly index
docs/ai/README.md             This index
docs/ai/context.md            Owner context
docs/ai/repositories.md       Repository catalog
docs/ai/conventions.md        Engineering conventions
docs/ai/glossary.md           Glossary
docs/ai/profile.json          Machine-readable profile
```
