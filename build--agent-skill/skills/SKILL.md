---
name: build-your-own-x
description: >-
  Master programming by recreating your favorite technologies from scratch.
  A comprehensive skill based on the 500k+ star GitHub repo that curates
  step-by-step tutorials for building 3D Renderers, Databases, Git, OS,
  Compilers, Web Servers, and 25+ other technologies from zero.
---

# Build Your Own X — AI Coding Agent Skill

This skill enables AI coding agents (Codex, Claude Code, Cursor, etc.) to guide
users through building real technologies from scratch, using the curated
tutorial collection from codecrafters-io/build-your-own-x.

> "What I cannot create, I do not understand" — Richard Feynman

## Installation

This SKILL.md file is the **only file you need** to give your agent this skill.

**Codex:** Place in `~/.codex/skills/build-your-own-x/SKILL.md`
**Claude Code:** Add content to `CLAUDE.md`
**Cursor:** Add to `.cursorrules` or `.cursor/rules/`
**GitHub Copilot:** Add to `.github/copilot-instructions.md`

## When to Use This Skill

Invoke this skill when a user wants to:
- Learn a technology deeply by rebuilding it
- Understand internals of tools they use daily
- Get a structured, tutorial-based learning path
- Practice systems programming, compilers, databases, or graphics
- Work on a hands-on project that teaches fundamentals

## Categories Overview

There are 30+ technology categories with 250+ curated tutorials.

### Core Systems
- 3D Renderer — C++, C#, Python, JavaScript, Java
- Database — C, C++, Go, Rust, Python, Ruby, Clojure
- Docker / Containers — C, Go, Python, Shell
- Emulator / VM — C, C++, Rust, Python, JavaScript, Common Lisp
- Git — Python, Haskell, JavaScript, Ruby, Go
- Network Stack — C, Ruby, Python
- Operating System — C, C++, Rust, Assembly
- Processor — Verilog
- Shell — C, Go, Rust
- Memory Allocator — C

### Languages & Compilers
- Programming Language — C, C++, Python, Haskell, OCaml, JS, Rust, Go, Ruby, Elixir, F#, Java, Racket, Swift, TypeScript, Assembly
- Regex Engine — C, Go, JavaScript, Python, Scala, Perl
- Template Engine — JavaScript, Python, Ruby

### Web & Networking
- Web Server — Python, Node.js, C#, PHP, Ruby
- Web Browser — Rust, Python
- Front-end Framework — JavaScript
- BitTorrent Client — Go, C#, Python, Node.js, Nim

### Blockchain & AI
- Blockchain / Crypto — Go, JS, TS, Python, Rust, Java, Kotlin, Ruby, Scala
- Neural Network / AI — Python, Go, C#, JavaScript, F#
- AI Model — Python (LLM, Diffusion, RAG)

### Games & Media
- Game — C, C++, C#, Python, JavaScript, Rust, Lua, Ruby, Go, Java
- Physics Engine — C, C++, JavaScript
- Voxel Engine — C++
- Visual Recognition — Python
- Augmented Reality — C#, Python

### Tools & More
- Command-Line Tool — Go, Rust, Nim, Node.js, Zig
- Bot — Python, Node.js, Rust, R, Haskell
- Text Editor — C, C++, Python, Ruby, Rust
- Search Engine — Python, CSS
- Distributed Systems — Java

## Agent Workflow

### Step 1: Identify the Category
Map the user's request to a category. Examples:
- "I want to build Redis" -> Database
- "How does Git work?" -> Git
- "Teach me compilers" -> Programming Language
- "Make a game like Minecraft" -> Voxel Engine

### Step 2: Choose a Tutorial
For the matched category, select based on:
- Preferred language — e.g., Python option for Python users
- Experience level — beginner vs advanced
- Goal — theory vs practical implementation

### Tutorial Selection Examples

| User Says | Category | Best Tutorial | Language |
|-----------|----------|---------------|----------|
| "Build Redis" | Database | Build Your Own Redis from Scratch | C++ / Go |
| "Write a compiler" | Programming Language | Crafting Interpreters | Java |
| "Build git" | Git | pygit or wyag | Python |
| "Make a game" | Game | Handmade Hero / Tetris tutorial | C / C++ |
| "Build Docker" | Docker | Container in 100 lines of Go | Go |
| "Make a web server" | Web Server | Build Your Own Web Server | Node.js / Python |
| "Write a shell" | Shell | Write a Shell in C | C |
| "Neural network" | Neural Network | Neural Network from Scratch | Python |

### Step 3: Guide Through the Build
- Break the tutorial into manageable stages
- Help write code, not just read
- Explain concepts as they arise
- Debug and test each stage
- Encourage running code early and often

### Step 4: Verify Understanding
- Ask conceptual questions at each milestone
- Suggest modifications
- Compare with the real tool's behavior

## How to Test

### Test 1: Compiler Building
Prompt: "I want to learn how compilers work by building one from scratch."
Expected: Agent identifies Programming Language category, selects Crafting
Interpreters or Build Your Own Lisp, guides step by step.

### Test 2: Git Internals
Prompt: "How does git store my files internally? Show me by building a minimal git."
Expected: Agent references pygit or wyag tutorials, explains blob/tree/commit,
implements a minimal version.

### Test 3: Category Discovery
Prompt: "What can I build today?"
Expected: Agent lists categories and asks about interests/language.

## Compatibility

| Agent | Status | Notes |
|-------|--------|-------|
| Codex | Full | SKILL.md format natively supported |
| Claude Code | Full | Can follow workflow; manual SKILL.md loading |
| Cursor | Partial | SKILL.md can be placed in .cursorrules |
| GitHub Copilot Chat | Partial | Works as reference, no native skill loading |
| Windsurf | Partial | Can ingest references |

## References
See references/ directory for full categorized listings.

## Contributing
Original repository: https://github.com/codecrafters-io/build-your-own-x
