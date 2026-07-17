# Changelog

All notable changes to **reverse-skill** are documented in this file.

Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
Versioning follows [Semantic Versioning](https://semver.org/).

## [Unreleased]

### Added

- Ten new first-class skills (R21–R30): `protocol-reverse`, `ghidra-reverse`, `cloud-k8s`, `windows-ad`, `digital-forensics`, `code-audit`, `threat-hunting`, `game-reverse`, `wifi-wireless`, `browser-extension-reverse`
- Wired into `MASTER-ROUTING.md`, `master-route.ps1`, `routing.md`, module table, domain map, role-map, and coherence tests

## [1.0.0] — 2026-07-18

First **formal** public release of the reverse-skill skill-router pack.

### Added

#### Ops / combat contract layer (`skills/ops/`)

- `IDENTITY.md` — product identity: lightweight skill router + bootstrap + field-journal (not a Z3r0-style platform)
- `scope-contract.md` — case scope + `network_profile`; **auth not granted → no ACT on target**
- `evidence-finding-path.md` — Evidence → Finding → Path chain
- `role-map.md` — lead / specialist role mapping and handoff
- `timeline-workitem.md` — timeline + workitem coverage
- `sandbox-profile.md` — tool profile mapping
- `skill-supply-chain.md` — Agent Skill / MCP install gate (AST10-lite)

#### PRIMARY routing & case tooling (`skills/scripts/`)

- `master-route.ps1` — PRIMARY route from task hint
- `case-init.ps1` / `case-guard.ps1` — case bootstrap + scope guard
- `append-evidence.ps1` — structured evidence append
- `smoke.ps1` — package smoke checks
- `verify-routing-coherence.ps1` — routing / ops coherence verification
- `test-p0-friction.ps1` — P0 client-side lab friction regression tests

#### Core skills & docs

- Full skill matrix: APK / IDA / radare2 / JS / .NET / mobile / malware / pwn / firmware / EDR / pentest / API / LLM / supply-chain / crypto / binary-diff / patch-diff / attack-chain / docs & diagrams
- `MASTER-ROUTING.md` + `routing.md` / `routing_zh.md` three-axis matrix
- Bootstrap + tool-index pipeline (`bootstrap-reverse.ps1` / `.sh`, `refresh-tool-index`)
- `field-journal` precedent library + completion checklist
- Multi-platform paths: Windows primary, Linux / macOS / Kali docs and scripts
- CTF-Sandbox-Orchestrator competition sub-skills
- Burp MCP extension package (`burp-mcp-full/`)

#### Quality / localization

- UTF-8 integrity for Chinese docs (`RULES_zh`, `routing_zh`, related guides)
- Client-side lab playbook and recon pipeline references for authorized testing friction reduction

### Notes

- `skills/tool-index.md` / `tool-index.json` are **machine-local** and intentionally gitignored; generate via `refresh-tool-index` after clone.
- This tag freezes the skill-router product surface at commit `9fc280b` plus this release metadata.

### Links

- Tag: `v1.0.0`
- Repository: https://github.com/zhaoxuya520/reverse-skill

[1.0.0]: https://github.com/zhaoxuya520/reverse-skill/releases/tag/v1.0.0
