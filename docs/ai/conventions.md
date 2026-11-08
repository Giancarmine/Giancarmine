# Engineering conventions

Conventions harvested from the owner's active repositories. They are defaults, not
universal law: when a repository has its own `AGENTS.md` or `CONTRIBUTING.md`, that file
wins. Treat this document as the "how Carmine likes to work" summary.

## General principles

- **Documentation is part of the product.** A change is not done until the owning
  document is updated.
- **Smallest safe change.** Prefer additive, focused diffs. Do not reformat or rename
  unrelated code in a bug-fix change.
- **Evidence over claims.** Run the checks; report the exact commands and results. If a
  check could not run, say why and mark the step unverified.
- **No secrets in Git.** Never commit passwords, API tokens, private keys, Wi-Fi
  credentials, alarm codes, or real `.env` files. Use `.env.example` for variable names.
- **Public-ready by default.** Assume every commit, issue, PR, and artifact may become
  public. Keep personal data, private network details, and device identifiers out.
- **Declarative where practical, explicit where not.** If a step is manual, record it as
  a documented exception.
- **Standard, boring tools.** Committed wrappers, version catalogs, `.editorconfig`,
  Docker Compose over Kubernetes where it fits, GitHub Actions for CI.

## Branches

Use a short, typed branch name:

| Prefix | Use for |
| --- | --- |
| `feat/` | User-visible behavior or a new endpoint. |
| `fix/` | Bug fixes. |
| `test/` | Test-only changes. |
| `docs/` | Documentation, comments, templates. |
| `chore/` | Build, dependency, tooling. |
| `security/` | Security controls or hardening. |

Examples: `feat/local-probe`, `docs/testing-gates`,
`security/free-plan-controls`, `fix/backup-path`.

Do not push directly to `main`. Use a branch and a pull request.

## Commits

- Imperative mood, subject under ~72 characters.
- Conventional Commit prefixes (`feat:`, `fix:`, `docs:`, `test:`, `chore:`) are welcome
  but not mandatory.
- Explain *why* in the body when the change is not obvious.
- Keep secrets and private data out of commit messages.
- Sign commits when a signing key is configured; do not block on it for small projects.

## Merge policy

This differs per repository; check before merging:

- `rock-paper-scissors-lizard-spock-bot`: **squash-merge** after CI.
- Some repositories require **merge commits** and reject squash or rebase merges. Check
  the repository's `CONTRIBUTING.md` or `AGENTS.md` before merging, and delete the branch
  afterward.

## Kotlin / JVM

- Kotlin official style, **4-space** indentation, **LF** line endings, UTF-8, final
  newline, no trailing whitespace (see `.editorconfig`).
- Run `./gradlew ktlintCheck`; use `./gradlew ktlintFormat` to fix.
- Keep dependency versions in `gradle/libs.versions.toml`; avoid hardcoding versions in
  `build.gradle.kts`.
- Use the committed Gradle wrapper. Do not rely on a system Gradle.
- Package layout follows the project. In `rock-paper-scissors-lizard-spock-bot`:
  `com.el_giancar.{config,domain,application,infrastructure}`; keep services stateless
  and free of framework imports so they stay unit-testable.
- Services accept typed values (enums), not raw strings. Parsing and validation belong at
  the edge (HTTP/Telegram layer).
- Put user-facing text in one place (for example `Messages.kt`), not in domain or
  application services.
- `src/test/kotlin` with `kotlin.test` on the JUnit Platform; prefer deterministic
  overloads over random stubbing. New behavior needs a test.
- Build/test command pattern:
  `./gradlew ktlintCheck test buildFatJar` (or `./gradlew build`).

## Java / Spring Boot

- Standard Maven/Gradle layout, constructor injection, typed DTOs.
- Keep controllers thin; put business logic in services.
- Do not commit `application-local.*` files with real credentials.

## Ansible / YAML

- YAML: 2-space indentation; `yamllint` with `extends: default`, line length disabled,
  `truthy` restricted to `true`/`false`, no implicit or explicit octal values.
- Run `ansible-lint` and `yamllint .`.
- Idempotent tasks; `become` only where needed; no secrets in playbooks or inventories.
- Ask before running `ansible-playbook` against a real host.

## Shell

- `bash` with `set -euo pipefail` in scripts.
- Quote variables; prefer `[[ ]]`; keep scripts small and documented.
- Run `shellcheck` when available.

## TypeScript / JavaScript

- Match the existing project style; do not introduce a second formatter.
- Keep secrets in environment variables, never in source.
- Add or update tests for behavior changes.

## Python

- Prefer the standard library and a small dependency set.
- Use a virtual environment; do not commit it.

## Documentation

- Markdown, American English, short paragraphs, tables for structured facts.
- Every long-lived decision gets an ADR; every operational procedure gets a runbook.
- Update the owning document instead of creating a near-duplicate.
- Keep a changelog in Keep a Changelog style when the repository has one.
- For the profile repository, preserve inline HTML in `README.md` and keep links valid.

## Testing and validation

Use what the repository provides. Common checks:

```sh
./gradlew ktlintCheck test buildFatJar   # Kotlin projects
ansible-lint && yamllint .               # Ansible roles
docker compose config                    # Compose files
terraform fmt -check -recursive           # Terraform
terraform validate
npx --yes markdownlint-cli2@0.24.0 "**/*.md"
git diff --check
```

Do not disable a security control, TLS verification, firewall rule, MFA, or secret scan
to make a check pass.

## Security habits

- No WAN exposure for management interfaces; use a VPN such as Tailscale.
- Least privilege; separate credentials per service; rotate on exposure.
- Redact tokens in logs. In the Telegram bot, the Logback redaction pattern and the
  JUL-to-SLF4J bridge are load-bearing; do not remove them.
- Back up before destructive work; verify restores; a snapshot is not a backup.
- Report vulnerabilities privately (see each repository's `SECURITY.md`).

## AI-specific conventions

- `AGENTS.md` is the canonical agent file. Keep per-tool files
  (`.github/copilot-instructions.md`, `CLAUDE.md`, `GEMINI.md`, `.cursor/rules/`)
  short and pointing at it.
- Document hard rules (secrets, destructive commands, out-of-scope work) explicitly.
- Include a repository map, a verification checklist, and a definition of done.
- Do not let generated AI files drift from reality; update them with the code.
