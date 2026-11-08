# Glossary

Terms an agent is likely to meet in this profile and the owner's repositories. Keep
definitions short and factual.

## Project and process terms

| Term | Meaning |
| --- | --- |
| `AGENTS.md` | Canonical instructions for AI coding agents working in a repository. |
| ADR | Architecture Decision Record: a short document recording a decision, context, and consequences. |
| Definition of Done | The checklist a change must satisfy before it is considered complete. |
| Declarative | Described as desired state (for example Ansible or Terraform) instead of imperative steps. |
| Manual exception | A step that is intentionally not automated, recorded so it is not forgotten. |
| Runbook | A documented operational procedure, usually for recovery, rotation, or maintenance. |
| Public-safe | Safe to publish: no secrets, private data, or private network details. |
| CGNAT | Carrier-Grade NAT: the ISP shares one public IPv4 address among customers, so inbound IPv4 is not available. |

## Platforms and tools

| Term | Meaning |
| --- | --- |
| Tailscale | WireGuard-based mesh VPN used for remote access without exposing services to the WAN. |
| Docker Compose | Tool for defining and running multi-container Docker applications from a Compose file. |
| Vagrant | Tool for building and managing reproducible virtual machine environments. |
| Ansible | Agentless configuration-management and provisioning tool. |
| Terraform | Infrastructure-as-code tool for declarative resource management. |
| n8n | Workflow automation tool; `n8n-workflow` stores workflow definitions. |
| Render | Cloud application platform used to deploy the Telegram bot. |
| GitHub Actions | CI/CD service used across the repositories. |
| Topgrade | CLI tool that upgrades many package managers and tools in one command. |

## Languages and frameworks

| Term | Meaning |
| --- | --- |
| Kotlin | JVM language used for the Ktor services and the Telegram bot. |
| Ktor | Kotlin framework for asynchronous servers and clients. |
| `kotlinx.serialization` | Kotlin multiplatform serialization library. |
| tgbotapi | Kotlin Telegram Bot API library (`dev.inmo:tgbotapi`). |
| Gradle | JVM build tool; projects commit the wrapper (`./gradlew`). |
| `libs.versions.toml` | Gradle version catalog for dependency versions. |
| ktlint | Kotlin linter and formatter. |
| Spring Boot | Java framework for building stand-alone Spring applications. |
| Flutter | Dart UI toolkit for mobile, web, and desktop apps. |
| Dart | Language used by Flutter. |
| Ktor Netty | Netty engine used to run Ktor servers. |

## Project-specific terms

| Term | Meaning |
| --- | --- |
| `ansible-DRP` | Ansible playbooks that provision a fresh Ubuntu machine as a developer workstation. The exact expansion of "DRP" is not documented publicly. |
| Homelab | The owner's private home infrastructure and automation project. Details are intentionally not public. |
| `ktor_phrases` | REST API that associates emojis with phrases. |
| RPSLS | Rock–Paper–Scissors–Lizard–Spock, the five-move variant of the game. |
| Long polling | Telegram update mode where the bot repeatedly requests updates instead of receiving webhooks. |
| `/healthz` | Liveness endpoint: always returns 200 while the process is alive. |
| `/readyz` | Readiness endpoint: reports whether the bot is connected to Telegram. |
| JUL-to-SLF4J bridge | Routes `java.util.logging` records through SLF4J/Logback so token redaction applies. |
| Holcim EMEA Digital Center | The owner's employer per the profile README. |
| LafargeHolcim / `eits-lafargeholcim` | Holcim group naming used in the GitHub company field. |

## Acronyms

| Acronym | Meaning |
| --- | --- |
| CI / CD | Continuous Integration / Continuous Delivery or Deployment. |
| IaC | Infrastructure as Code. |
| MFA | Multi-Factor Authentication. |
| PR | Pull Request. |
| VPN | Virtual Private Network. |
| WAN | Wide Area Network; "no WAN exposure" means do not publish management interfaces to the internet. |
| SWAPI | Star Wars API. |
| EMEA | Europe, Middle East, and Africa. |
| I&O | Infrastructure and Operations. |
