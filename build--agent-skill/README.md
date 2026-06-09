# Build Your Own X — Agent Skill

> Transform the legendary 500k+ star `build-your-own-x` repository into a
> practical skill for AI coding agents like Codex, Claude Code, and Cursor.

[![Stars](https://img.shields.io/badge/Stars-513k+-gold)](https://github.com/codecrafters-io/build-your-own-x)
[![License: CC0 1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey)](https://creativecommons.org/publicdomain/zero/1.0/)

This project repackages the curated tutorials from
[codecrafters-io/build-your-own-x](https://github.com/codecrafters-io/build-your-own-x)
into an **AI Agent Skill** — a structured knowledge file that teaches coding
agents how to guide users through building real technologies from scratch.

## What's Inside

```
build-your-own-x-agent-skill/
├── README.md                  # This file (English)
├── README_CN.md               # Chinese version
├── skills/
│   └── SKILL.md               # Core agent skill (ingest this into your agent)
└── references/                # (Coming soon: full categorized indexes)
```

### skills/SKILL.md
The main skill file. It contains:
- **30+ technology categories** from 3D Renderers to Web Servers
- **250+ curated tutorials** with language annotations
- **Agent workflow** (identify → choose → guide → verify)
- **Compatibility matrix** for Codex, Claude Code, Cursor, etc.
- **Test cases** to verify your agent picks up the skill

## How to Use

### With Codex
Place `skills/SKILL.md` in your agent's skill directory, or reference it
in your agent's configuration. The agent will automatically recognize
the skill and use it when you ask to build something.

### With Claude Code
Reference the SKILL.md content in your CLAUDE.md or load it as a custom
instruction. Claude can navigate the categories and guide you through
tutorials.

### With Cursor
Add the SKILL.md content to your `.cursorrules` file for the project
you're working on.

### With Any Agent
Give the agent a prompt like:
> "I want to build a database from scratch. Use the build-your-own-x skill."

## Why This Exists

The original [build-your-own-x](https://github.com/codecrafters-io/build-your-own-x)
is an **awesome list** — a curated collection of links. While invaluable for
humans browsing tutorials, AI agents can't easily navigate an awesome list
to help you build things interactively.

This skill bridges that gap by:
1. Structuring the knowledge into a machine-readable format
2. Defining a clear agent workflow (identify → choose → guide → verify)
3. Making it testable so you know your agent actually "gets it"

## Compatibility Matrix

| Agent | Status | Integration |
|-------|--------|-------------|
| **Codex** | Full | Native SKILL.md support |
| **Claude Code** | Full | CLAUDE.md or custom instructions |
| **Cursor** | Partial | .cursorrules |
| **GitHub Copilot Chat** | Partial | Reference doc style |
| **Windsurf** | Partial | Can ingest references |
| **Continue.dev** | Partial | Custom documentation source |
| **Aider** | Partial | Can read as context file |

## Test Your Agent

Try these prompts to see if your agent has picked up the skill:

1. **"I want to build a Redis clone from scratch"**
   → Agent should identify Database category and select a C++/Go/Redis tutorial

2. **"Teach me how compilers work by making one"**
   → Agent should pick Programming Language, suggest Crafting Interpreters

3. **"How does Git store my files? Let's build minimal git"**
   → Agent should explain blobs/trees/commits via pygit or wyag

4. **"What cool things can I build?"**
   → Agent should list categories and ask your interests

## Roadmap

- [x] Extract and structure all 30+ categories
- [x] Write core SKILL.md with agent workflow
- [x] Chinese translation (README_CN.md)
- [ ] Full categorized tutorial index (`references/`)
- [ ] Per-language index for polyglot learners
- [ ] Step-by-step starter templates for top categories
- [ ] Automated test suite for agent compatibility
- [ ] Community contributions via PR

## Contributing

Contributions welcome! See the
[original repository](https://github.com/codecrafters-io/build-your-own-x)
for new tutorials. For improvements to the agent skill itself, open an issue
or PR here.

## License

CC0 1.0 Universal — see [LICENSE](LICENSE).
