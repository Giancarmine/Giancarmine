# Owner context

Public-safe context about **Carmine Cuofano** for AI agents. Facts come from the
public GitHub profile, this repository's `README.md`, and the repositories listed in
[`repositories.md`](repositories.md). Anything inferred rather than stated is marked
**(inferred)**.

Last reviewed: **2026-11-08**.

## Identity

| Field | Value |
| --- | --- |
| Name | Carmine Cuofano |
| GitHub | [`@Giancarmine`](https://github.com/Giancarmine) |
| Handle note | It is `Giancarmine` (ends in **mine**). `giancarme` is not the account and returns 404. |
| Location | Madrid, Spain |
| Role | I&O Platform Engineer at **Holcim EMEA Digital Center** |
| GitHub company field | `@eits-lafargeholcim` |
| Bio | "Confused DevOps developer" |
| Experience | 8+ years in IT, per the profile README |
| Website | <https://giancarmine.github.io/> |
| LinkedIn | <https://www.linkedin.com/in/carmine-cuofano-271417124/> |
| X / Twitter | [@el_giancar](https://twitter.com/el_giancar) |
| Telegram | [@Giancarmine](https://t.me/Giancarmine) |
| Medium | [@giancarmine.cuofano](https://medium.com/@giancarmine.cuofano) |
| dev.to | [el_giancar](https://dev.to/el_giancar) |

The profile README also links a Gmail badge. Prefer the public links above; do not add
a private email address to repository content.

## Professional summary

Platform / DevOps engineer with a backend-developer background. The public profile
describes a focus on **cloud computing, DevOps, and security**, plus a strong
preference for **open source** and **continuous improvement**.

The career path visible on GitHub runs from Java/Android and Flutter learning projects
and university coursework, through Spring Boot backends and Kotlin/Ktor services, to
the current platform-engineering role.

## What he works on

- **Platform engineering and infrastructure:** Ansible, Vagrant, Docker, Kubernetes,
  Terraform, Linux, SSH, Bash, CI/CD.
- **Observability and operations:** Grafana, Prometheus, monitoring and alerting.
- **Backend services:** Kotlin/Ktor, Java/Spring Boot, Node.js/Express, TypeScript,
  Python, REST APIs.
- **Data stores:** PostgreSQL, MySQL, SQL Server, Oracle, MongoDB, SQLite.
- **Mobile and frontend (past and side projects):** Flutter/Dart, Android/Java,
  Angular/TypeScript, Storybook.
- **Cloud:** AWS.
- **Tooling:** GitHub and GitLab, Gradle, Cucumber, CMake.

The icon strip in `README.md` is the canonical list of advertised tools:
AWS, Docker, Kubernetes, Terraform, Ansible, Vagrant, Kotlin, Ktor, Flutter, Dart,
Java, Spring, Gradle, Cucumber, Node.js, Express, Python, TypeScript, GitHub, GitLab,
Linux, SSH, Bash, CMake, Grafana, Prometheus, SQLite, MySQL, PostgreSQL, Oracle,
SQL Server, MongoDB, Storybook.

## Active projects

The repositories that best represent current work:

1. **`ansible-DRP`** — Ansible playbooks that turn a fresh Ubuntu machine into a
   ready-to-work dev box (zsh, Docker, Kubernetes CLIs, VS Code, Topgrade). Shell,
   Vagrant, GitHub Actions, MIT.
2. **`homelab`** — documentation-first home lab: a virtualization platform, a home-automation platform, a private alarm system
   alarm integration, a DNS filter, Tailscale, a health-check service, Docker Compose. Private, small
   project with a strict security and testing process.
3. **`rock-paper-scissors-lizard-spock-bot`** — Kotlin/Ktor Telegram bot, long polling,
   health/readiness endpoints, Render deployment, CI, ktlint, no persistence.
4. **`ktor_phrases`** — Kotlin/Ktor REST API for emoji/phrase association using
   `kotlinx.serialization`, with Docker and CI.
5. **`carmine-cuofano-revolut-test`** — Kotlin DevOps engineer take-home test.
6. **`extraday-backend`** — Spring Boot REST API backed by MongoDB.
7. **`MediterraneApp`** — recipe API in Spring Boot.
8. **`full-swapi-test`** — full-stack Star Wars API exercise (JavaScript).
9. **`http-autocaller-bot`**, **`ligogram-bot`** — TypeScript bots.
10. **`n8n-workflow`** — automation workflows.
11. **`giancarmine.github.io`** — personal site (`mytemplate.xyz` template).

Full catalog, including archived learning projects:
[`repositories.md`](repositories.md).

## How he works (inferred from the repositories)

These are patterns visible in his `AGENTS.md` and `CONTRIBUTING.md` files. Treat them as
strong defaults, not absolute rules for every repository.

- **Documentation is part of the product.** The homelab repository is documentation-first
  and updates status, changelog, ADRs, runbooks, and security notes with each iteration.
- **Small, focused, reviewable changes.** Branch names are typed (`feat/`, `fix/`,
  `docs/`, `test/`, `chore/`, `security/`). Avoid unrelated reformatting.
- **Evidence over claims.** Tests, validation commands, and recorded evidence matter.
  Do not claim a check passed without running it.
- **Security is a gate, not a checklist.** No secrets in Git, no WAN exposure, least
  privilege, MFA, patching, and tested recovery.
- **Declarative where practical, explicit where not.** Manual exceptions are recorded.
- **Public-ready by default.** Even private repositories are written as if they could be
  published.
- **Prefer standard, boring tools.** Docker Compose over Kubernetes in the homelab;
  committed Gradle wrappers; `libs.versions.toml`; `.editorconfig`.
- **AI-friendly repositories.** The newer projects include `AGENTS.md`, short
  `.github/copilot-instructions.md` pointers, and explicit safety rules for agents.

## Communication style (inferred)

- Direct, concise, and practical; low tolerance for fluff.
- Comfortable with technical detail and explicit trade-offs.
- Uses English for code, documentation, and commit messages.
- Italian appears in older university repositories and personal context.
- Self-deprecating humor is part of the public voice ("Confused DevOps developer",
  "Eat Spaghetti. DON'T do Spaghetti."). Keep it in the profile; do not force it into
  technical documentation.

## Preferences when asking an AI for help

Derived from the repository conventions:

- Read the existing `AGENTS.md` and `CONTRIBUTING.md` before proposing changes.
- State assumptions and unknowns instead of inventing them.
- Prefer the smallest safe change; include rollback or recovery for operational work.
- Keep secrets and private data out of examples, logs, commits, and diffs.
- Update the owning documentation when behavior or decisions change.
- Show the exact commands run and their results.

## Open questions

- The README says both "8+ years" and "9+ years" in different places. Use **8+ years**
  unless the owner confirms a precise figure.
- Employer naming varies between "Holcim EMEA Digital Center" (README) and
  `@eits-lafargeholcim` (GitHub company). Keep both, in their respective contexts.
- `open-cv` is currently an empty repository; the public CV source is not available.
- Spoken languages are not stated publicly; do not assume them.
