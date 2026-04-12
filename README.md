# project-updater

> 🇰🇷 [한국어 README](./README.ko.md)

**Unified engine for project CLAUDE.md and GRAPH.md — bootstrap project instructions and build Obsidian-native knowledge graphs in one go.**

## Prerequisites

- **Claude Cowork or Claude Code** environment
- **Obsidian Vault** with wikilink-based note structure

## Goal

Every new project folder needs two things: a CLAUDE.md that tells the AI how to work in this project, and a GRAPH.md that maps document relationships so the AI doesn't have to re-read everything each session. This skill creates both from a single invocation — interview-driven templates for CLAUDE.md, content-aware knowledge graphs for GRAPH.md.

## When & How to Use

Invoke when starting a new project, when a project folder has no CLAUDE.md or GRAPH.md, or when documents have changed and the knowledge graph needs updating. Say "프로젝트 업데이터" or "프로젝트 업데이트 실행해줘" to trigger. For vault-wide updates across all project folders, say "전체 프로젝트 업데이트".

## Use Cases

| Scenario | Prompt | What Happens |
|---|---|---|
| New project folder | `"새 프로젝트 세팅해줘"` | Interview → type detection → CLAUDE.md + GRAPH.md created |
| Documents added/changed | `"GRAPH.md 갱신해줘"` | Folder rescan → surgical diff update to knowledge graph |
| Vault-wide health check | `"전체 프로젝트 업데이트"` | Parallel scan of all project folders → report table |

## Key Features

- **3-type CLAUDE.md templates** — Full-spec (A), Standard (B), Minimal (C) matched to project complexity
- **Obsidian wikilink knowledge graphs** — GRAPH.md with `[[wikilinks]]` for native graph view integration
- **Interview protocol** — Structured questions that minimize round-trips while capturing essential context
- **Surgical graph updates** — Only changed documents are touched; existing summaries preserved
- **Vault-wide batch mode** — Agent-parallel processing of 3-5 projects at a time

## Works With

- **[skill-builder](https://github.com/jasonnamii/skill-builder)** — Creates/modifies skills; project-updater is NOT for skill creation
- **[up-manager](https://github.com/jasonnamii/up-manager)** — Handles CLAUDE.md *updates* after initial creation

## Installation

```bash
git clone https://github.com/jasonnamii/project-updater.git ~/.claude/skills/project-updater
```

## Update

```bash
cd ~/.claude/skills/project-updater && git pull
```

Skills placed in `~/.claude/skills/` are automatically available in Claude Code and Cowork sessions.

## Part of Cowork Skills

This is one of 25+ custom skills. See the full catalog: [github.com/jasonnamii/cowork-skills](https://github.com/jasonnamii/cowork-skills)

## License

MIT License — feel free to use, modify, and share.
