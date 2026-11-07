# AGENTS.md

Canonical guidance for AI agents (OpenCode, GitHub Copilot, Cursor, Claude Code,
Gemini CLI, Codex, and similar tools) working in this repository.

This repository is **not a software project**. It is the GitHub profile repository for
**Carmine Cuofano ([@Giancarmine](https://github.com/Giancarmine))**. Its product is
`README.md`, rendered at <https://github.com/Giancarmine>.

## What this repository is for

- The public profile README: bio, links, stack, and GitHub stats.
- A small set of AI context files that let agents understand the owner and his
  projects without guessing: `AGENTS.md`, `llms.txt`, and `docs/ai/`.
- Nothing is built, tested, packaged, or deployed here.

## Owner at a glance

| Field | Value |
| --- | --- |
| Name | Carmine Cuofano |
| GitHub | [`@Giancarmine`](https://github.com/Giancarmine) — the handle ends in **mine**, not **me** |
| Role | I&O Platform Engineer at Holcim EMEA Digital Center |
| GitHub company field | `@eits-lafargeholcim` |
| Location | Madrid, Spain |
| Website | <https://giancarmine.github.io/> |
| Bio | "Confused DevOps developer" |
| Focus | Cloud, DevOps, platform engineering, security, and open source |

Full context: [`docs/ai/context.md`](docs/ai/context.md).

## Ground rules

1. **Do not invent facts.** Use this file, `docs/ai/`, and the linked public profiles.
   If a fact is unknown, write `TBD` or ask the owner. Never guess employers, dates,
   credentials, hardware, or private network details.
2. **Public-safe by default.** This is a public repository. Never add secrets, tokens,
   private keys, real `.env` files, customer data, private IP addresses, device serials,
   alarm codes, or anything that is not already public on the owner's profiles.
3. **Keep personal data minimal.** The owner's public links are already in `README.md`.
   Do not add home addresses, phone numbers, birth dates, or private emails.
4. **Preserve the profile design.** `README.md` uses hand-written HTML, shields.io
   badges, devicon images, and GitHub Readme Stats cards. Do not reformat it into plain
   Markdown, reorder the design, or remove badges unless the owner asks.
5. **Keep the context concise.** The next agent should be able to read this repository
   in a few minutes. Prefer updating the owning file over creating a new document.
6. **The profile is not a CV dump.** Keep it readable. Long career detail belongs in
   the CV or external profiles, not in the README.
7. **Do not add trackers, analytics, ads, or third-party scripts** to the README.
8. **Do not change the license.** The repository is MIT; see `LICENSE`.
9. **Respect per-project rules.** Other repositories have their own `AGENTS.md`. This
   file only governs the profile repository. When working in a project repository, read
   that repository's `AGENTS.md` first.
10. **Do not force-push, rewrite history, delete branches, or publish releases** unless
    the owner explicitly asks.

## Read order

Before changing anything, read:

1. `README.md` — the current public profile.
2. `docs/ai/context.md` — compact, public-safe context about the owner.
3. `docs/ai/repositories.md` — what each repository is and which ones matter.
4. `docs/ai/conventions.md` — branch, commit, formatting, testing, and security habits.
5. `docs/ai/glossary.md` — project-specific terms.
6. `docs/ai/profile.json` — the same profile data in machine-readable form.

## Repository map

```text
README.md                          Public GitHub profile (the only rendered product)
AGENTS.md                          Canonical agent contract (this file)
llms.txt                           LLM-friendly index for this profile and repos
CLAUDE.md                          Pointer for Claude Code
GEMINI.md                          Pointer for Gemini CLI
LICENSE                            MIT license
.github/copilot-instructions.md    Pointer for GitHub Copilot
.cursor/rules/profile.mdc          Pointer for Cursor
docs/ai/README.md                  Index of the AI context set
docs/ai/context.md                 Who the owner is and how he works
docs/ai/repositories.md            Repository catalog and per-project notes
docs/ai/conventions.md             Engineering conventions harvested from the repos
docs/ai/glossary.md                Terms an agent is likely to meet
docs/ai/profile.json               Machine-readable profile data
```

## Editing the profile README

- Keep the HTML structure balanced. The file mixes `<div>`, `<h1>`, `<h3>`, `<p>`, and
  `<img>` blocks; do not leave unclosed tags.
- Keep image and badge URLs working. When replacing a stats or badge service, verify
  the new URL returns an image before committing.
- Keep the tone: short, friendly, a little self-deprecating ("Confused DevOps
  developer", "Eat Spaghetti. DON'T do Spaghetti."), and professional underneath.
- Do not claim a new role, certification, or metric unless the owner confirms it.
- If you add a link, prefer HTTPS and a stable destination.

## Keeping the AI context current

Update the owning file when reality changes:

| Change | Update |
| --- | --- |
| New role, employer, location, or bio | `README.md`, `docs/ai/context.md`, `docs/ai/profile.json` |
| New active repository or archived repo | `docs/ai/repositories.md`, `llms.txt` |
| New language, framework, or platform in regular use | `docs/ai/context.md`, `docs/ai/conventions.md` |
| New branch/commit/test/security convention | `docs/ai/conventions.md` |
| New term an agent may not know | `docs/ai/glossary.md` |
| New AI entry-point file | `docs/ai/README.md` and this file |

Do not update files mechanically. If a statement becomes false, fix it.

## Validation

This repository has no build. Run the checks that apply:

```sh
npx --yes markdownlint-cli2 "**/*.md"
git diff --check
```

`README.md` intentionally uses inline HTML and images, so a lint configuration must
allow `MD033` and `MD041`. If no config exists, either add one or skip markdown lint for
the README and validate the HTML and links manually.

Manual checks:

- Every tag opened in `README.md` is closed.
- Every new or changed URL returns `2xx` (or is a known badge service).
- The rendered profile still looks correct at <https://github.com/Giancarmine>.
- No secret, token, private key, or private data appears in `git diff`.

Do not claim a check passed unless it was actually run.

## Change workflow

1. Inspect `README.md` and the relevant `docs/ai/` file.
2. State the scope and whether the change is public-safe.
3. Make the smallest additive change.
4. Validate links and HTML.
5. Update the owning AI context file if a fact changed.
6. Report what changed, what was validated, and what remains unverified.

Use a branch and pull request for non-trivial changes. Do not push directly to `main`
unless the owner asks for it.

## Definition of Done

- [ ] The requested change is complete.
- [ ] No sensitive or private data was added.
- [ ] `README.md` still renders and its links work.
- [ ] `docs/ai/` still matches reality.
- [ ] Validation was run, or the reason it could not run is stated.
- [ ] The change is focused; unrelated formatting was not touched.
- [ ] No secrets, generated files, or local tool state were added.

## Out of scope unless asked

- Redesigning the profile or replacing the existing visual style.
- Adding analytics, trackers, ads, or third-party scripts.
- Turning the profile into a full CV or portfolio site.
- Creating new repositories, releases, deployments, or GitHub Actions.
- Force-pushing, rewriting history, or deleting branches.

## Related files

- [`README.md`](README.md) — human-facing profile.
- [`llms.txt`](llms.txt) — LLM-friendly index.
- [`docs/ai/context.md`](docs/ai/context.md) — owner context.
- [`docs/ai/repositories.md`](docs/ai/repositories.md) — repository catalog.
- [`docs/ai/conventions.md`](docs/ai/conventions.md) — engineering conventions.
- [`docs/ai/glossary.md`](docs/ai/glossary.md) — glossary.
- [`docs/ai/profile.json`](docs/ai/profile.json) — machine-readable profile.
