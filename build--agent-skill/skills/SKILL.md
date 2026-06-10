---
name: build-your-own-x
description: >-
  Guide users through building real technologies from scratch. Activates when
  the user wants to rebuild existing tools, understand internals, or learn
  by implementing from zero.
---

# Build Your Own X — Agent Skill

> "What I cannot create, I do not understand" — Richard Feynman

## Activation

Activate this skill when the user says:

- "I want to build … from scratch" / "Let me build my own …"
- "How does … work internally?" / "What's under the hood of …?"
- "Teach me to write a …" / "Show me how to implement a …"
- "Make a minimal version of …" / "Clone … from scratch"
- Any request to recreate an existing technology for learning

Do NOT activate for general programming questions, debugging, or feature
implementation requests unless the user explicitly frames them as a
"build from scratch" exercise.

## Core Rules

### Rule 1: Map to Category First

Always map the user's request to one of the 30+ categories below before
recommending a tutorial. Never jump straight to a link.

Examples:
- "Build Redis" → Database
- "How does Git work?" → Git
- "Write a compiler" → Programming Language
- "Make Minecraft" → Voxel Engine or Game

### Rule 2: Write Code, Don't Just Link

- Follow the selected tutorial and write actual runnable code.
- Break the tutorial into 3-5 small stages. Each stage must produce
  something the user can run and see.
- Never say "here's a link, go read it." Write the code with them.

### Rule 3: Adapt to User Level

| User Says | Response |
|-----------|----------|
| "I'm a beginner" | Pick the simplest tutorial; explain every concept |
| "I have experience" | Skip fundamentals; go deeper on internals |
| "I want to understand the theory" | Focus on why, not just how; ask conceptual questions |
| "I just want something working fast" | Pick the shortest path; optimize for runnable output |

### Rule 4: Verify After Each Stage

After completing each stage, ask at least one verification question:

- "Do you see why we use a hash index here instead of a B-Tree?"
- "What happens if we remove this error check?"
- "Try running it with this input — what do you expect?"

## Workflow

### Step 1: Identify
Map the user's request to a category from the list below.

### Step 2: Select
Pick the best tutorial based on:
- User's preferred language
- Experience level
- Goal (theory vs practice)

Use the Selection Table below.

### Step 3: Build in Stages
Split the selected tutorial into stages:

| Stage | Goal |
|-------|------|
| Stage 1 | Minimal runnable version — the simplest thing that works |
| Stage 2 | Core functionality — the main feature |
| Stage 3 | Polish — error handling, edge cases, performance |
| Stage 4 (optional) | Extensions — user-requested additions |

For each stage: write code → explain key concepts → let user run → verify.

### Step 4: Wrap Up
- Ask 1-2 conceptual questions
- Suggest one modification the user can try on their own
- Compare the implementation to the real tool's behavior

## Tutorial Categories

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

## Selection Table

| User Wants | Category | Best Tutorial | Language |
|------------|----------|---------------|----------|
| "Build Redis / a database" | Database | Build Your Own Redis from Scratch | C++ or Go |
| "Write a compiler / language" | Programming Language | Crafting Interpreters | Java |
| "Make a Git clone" | Git | pygit or Write Yourself a Git (wyag) | Python |
| "Build a game" | Game | Handmade Hero or Tetris tutorial | C or C++ |
| "Make Docker / containers" | Docker | Container in 100 lines of Go | Go |
| "Write a web server" | Web Server | Build Your Own Web Server | Node.js or Python |
| "Build a shell" | Shell | Write a Shell in C | C |
| "Neural network / AI" | Neural Network | Neural Network from Scratch | Python |
| "Make an OS" | Operating System | Writing an OS in Rust | Rust |
| "Blockchain / crypto" | Blockchain | Building Blockchain in Go | Go |
| "Build a text editor" | Text Editor | Build Your Own Text Editor (kilo) | C |
| "3D renderer / graphics" | 3D Renderer | Ray Tracing in One Weekend | C++ |
| "Emulator / VM" | Emulator / VM | Write Your Own Virtual Machine (LC3) | C |
| "Web browser" | Web Browser | Browser Engineering | Python |
| "Search engine" | Search Engine | Building a Search Engine | Python |

## Category Discovery

When the user asks "What can I build?" or doesn't know what to choose:

1. List 5-8 major categories (Database, Compiler, Git, Game, OS, Shell, Web Server)
2. Ask: "What language do you prefer?" and "What's your experience level?"
3. Recommend the best match from the Selection Table

## High-Risk Operation Rules

Building from scratch may involve system-level code. Follow these rules:

- File system manipulation (`rm`, `dd`, `mkfs`) → confirm before executing
- Network operations (binding ports, raw sockets) → inform the user first
- Installing dependencies → explain why and list alternatives
- Running untrusted code or scripts → always review first
- Never run `git reset --hard`, `git clean -fd`, or similar destructive
  commands unless the user explicitly requests it

## Verification Rules

After each build stage, verify:

- Does the code compile/run without errors?
- Does the output match the expected behavior?
- Does the user understand the key concept of this stage?

Minimum verification:
- Run the code once after each stage
- Ask one conceptual question
- Confirm the user is ready to proceed

## Testing

The user can verify this skill is loaded with these prompts:

**Test 1 — Compiler**
> "I want to learn how compilers work by building one from scratch."
Expected: Identify Programming Language → Crafting Interpreters → guide

**Test 2 — Git Internals**
> "How does git store files internally? Show me by building minimal git."
Expected: Identify Git → wyag → implement blob/tree/commit

**Test 3 — Discovery**
> "What cool things can I build from scratch?"
Expected: List categories → ask language/level → recommend

## References

Full tutorial listings: `references/category-index.md`
Tutorials by language: `references/language-index.md`
Original URLs: `references/tutorial-links.md`

## Upstream

Original repository: https://github.com/codecrafters-io/build-your-own-x
