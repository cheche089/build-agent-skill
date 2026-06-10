---
name: build-your-own-x
description: >-
  Guide users through building real technologies from scratch using curated
  tutorials. Activate when user wants to rebuild existing tools or learn
  internals by doing.
---

# Build Your Own X — Agent Skill

> "What I cannot create, I do not understand" — Richard Feynman

## 激活条件

当用户表达以下意图时激活本技能：
- "我想从零写一个…" / "I want to build … from scratch"
- "XX 内部是怎么工作的？" / "How does … work internally?"
- "教我写一个…" / "Teach me to build …"
- "实现一个迷你版的…" / "Implement a minimal …"
- "自己动手造一个…" / "Build my own …"

## 核心规则

### 规则 1：先分类，再匹配

用户提出需求后，必须先将它映射到以下 30+ 分类之一，再在对应分类中选择教程。不要跳过分类直接推荐。

### 规则 2：写代码，不只是给链接

- 参照选定教程，**实际写出可运行的代码**
- 把教程拆成 3-5 个阶段，每阶段写一部分
- 每完成一个阶段让用户运行验证
- 不要只丢一个"参考这个链接"就结束

### 规则 3：按用户水平调整

| 用户说 | 推荐方向 |
|--------|----------|
| "我是新手" | 选教程中最简单、步骤最详细的 |
| "我有经验" | 可以跳过基础部分，直接深入核心 |
| "我想理解原理" | 注重解释概念，多问"为什么" |
| "我想快速做一个" | 偏实用，选最短路径 |

### 规则 4：必须验证理解

每完成一个阶段，问用户一个问题确认理解：
- "你知道这里为什么用 B+Tree 而不是数组吗？"
- "如果不加这一行会发生什么？"
- "试试改成 XX 看看效果？"

## 教程分类

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

## 教程选择对照表

| 用户需求 | 分类 | 推荐教程 | 推荐语言 |
|----------|------|----------|----------|
| "写 Redis" | Database | Build Your Own Redis from Scratch | C++ / Go |
| "写编译器" | Programming Language | Crafting Interpreters | Java |
| "迷你 Git" | Git | pygit / wyag | Python |
| "做游戏" | Game | Handmade Hero / Tetris | C / C++ |
| "做 Docker" | Docker | Container in 100 lines | Go |
| "写 Web 服务器" | Web Server | Build Your Own Web Server | Node.js / Python |
| "写 Shell" | Shell | Write a Shell in C | C |
| "神经网络" | Neural Network | Neural Network from Scratch | Python |
| "做操作系统" | Operating System | Writing an OS in Rust | Rust |
| "做区块链" | Blockchain | Building Blockchain in Go | Go |

## 工作流

### Step 1: 识别分类
将用户需求映射到上方分类。

### Step 2: 选择教程
根据用户的语言偏好和经验水平，从对照表中选择教程。

### Step 3: 分阶段引导
将教程拆成 3-5 个可运行的小阶段：
- 阶段 1：最小可运行版本
- 阶段 2：核心功能
- 阶段 3：完善和优化
- 阶段 4（可选）：扩展功能

每阶段：写代码 → 解释 → 让用户运行 → 确认理解

### Step 4: 验证
- 提 1-2 个概念性问题
- 建议一个修改方向
- 对比真实工具的类似行为

## 高风险操作规则

本技能涉及系统编程（文件系统、网络、进程等），必须注意：

- 涉及 `rm -rf`、`git reset --hard`、格式化操作 → **先确认**
- 涉及端口监听、网络抓包 → **告知用户**
- 涉及修改系统配置 → **先确认**
- 涉及安装新依赖 → **说明原因和替代方案**

## 测试用例

用户可以用以下指令验证本技能已正确加载：

### 测试 1
> "我想从零学编译器"
期望：识别 Programming Language → 推荐 Crafting Interpreters → 开始引导

### 测试 2
> "Git 内部怎么存文件的？做一个迷你 Git"
期望：识别 Git → 参考 wyag → 写代码实现 blob/tree/commit

### 测试 3
> "有哪些东西可以自己造？"
期望：列出分类 → 询问用户的语言和兴趣
