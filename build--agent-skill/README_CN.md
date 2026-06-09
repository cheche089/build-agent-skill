# Build Your Own X — AI Agent 技能包

> 将传奇的 51 万+ Star 的 `build-your-own-x` 仓库，转化为 Codex、Claude Code 等
> AI 编程代理可用的实战技能。

[![Stars](https://img.shields.io/badge/Stars-513k+-gold)](https://github.com/codecrafters-io/build-your-own-x)
[![License: CC0 1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey)](https://creativecommons.org/publicdomain/zero/1.0/)

本项目将 [codecrafters-io/build-your-own-x](https://github.com/codecrafters-io/build-your-own-x)
中精心整理的教程集合，重新打包为 **AI Agent 技能包（Skill）**——一份结构化的知识文件，
让 AI 编程代理能够引导你从零开始亲手构建真正的技术。

## 目录结构

```
build-your-own-x-agent-skill/
├── README.md                  # 英文版说明
├── README_CN.md               # 本文件（中文版）
├── skills/
│   └── SKILL.md               # 核心技能文件（注入给你的 Agent）
└── references/                #（即将推出：完整分类索引）
```

### skills/SKILL.md
核心技能文件，包含：
- **30+ 技术分类**：从 3D 渲染器到 Web 服务器
- **250+ 精选教程**：标注了适用的编程语言
- **Agent 工作流**：识别 → 选择 → 引导 → 验证
- **兼容性矩阵**：Codex、Claude Code、Cursor 等
- **测试用例**：验证你的 Agent 是否学会

## 如何使用

### 在 Codex 中使用
将 `skills/SKILL.md` 放入 Codex 的技能目录，或通过配置引用它。
当你要求"构建一个 Redis"或"教我写编译器"时，Codex 会自动调用该技能。

### 在 Claude Code 中使用
将 SKILL.md 的内容写入 `CLAUDE.md`，或作为自定义指令加载。

### 在 Cursor 中使用
将 SKILL.md 内容添加到 `.cursorrules` 文件中。

### 在任何 Agent 中使用
直接给出指令：
> "我想从零构建一个数据库，请使用 build-your-own-x 技能。"

## 为什么需要这个？

原始 [build-your-own-x](https://github.com/codecrafters-io/build-your-own-x)
是一个 **awesome list**——精心整理的链接集合。对于人类浏览教程来说非常棒，
但 AI 代理很难直接导航一个外链列表来帮助你交互式地完成任务。

这个技能包填补了空白：
1. 将知识结构化，变成机器可读的格式
2. 定义了清晰的 Agent 工作流
3. 可测试性——你能验证你的 Agent 是否真正理解了

## 兼容性矩阵

| 代理 | 状态 | 集成方式 |
|------|------|----------|
| **Codex** | 完整 | 原生 SKILL.md 支持 |
| **Claude Code** | 完整 | CLAUDE.md 或自定义指令 |
| **Cursor** | 部分 | .cursorrules |
| **GitHub Copilot Chat** | 部分 | 作为参考文档 |
| **Windsurf** | 部分 | 读取 references 目录 |
| **Continue.dev** | 部分 | 自定义文档源 |
| **Aider** | 部分 | 作为上下文文件读取 |

## 测试你的 Agent

用以下提示测试你的 AI 代理是否学会：

1. **"我想从零克隆一个 Redis"**
   → Agent 应识别 Database 分类，选择 C++/Go Redis 教程

2. **"教我如何写一个编译器"**
   → Agent 应选择 Programming Language，
      推荐 Crafting Interpreters 或 Build Your Own Lisp

3. **"Git 的文件是怎么存的？让我们做一个迷你 Git"**
   → Agent 应通过 pygit 或 wyag 解释 blob/tree/commit

4. **"我能构建什么好玩的东西？"**
   → Agent 应列出分类，询问你的兴趣和语言偏好

## 路线图

- [x] 提取并结构化所有 30+ 分类
- [x] 编写核心 SKILL.md 及 Agent 工作流
- [x] 中文翻译（本文件）
- [ ] 完整分类教程索引（references/）
- [ ] 按编程语言索引
- [ ] 热门分类的快速启动模板
- [ ] Agent 兼容性自动化测试
- [ ] 社区贡献（PR）

## 贡献指南

欢迎贡献！添加新教程请访问
[原始仓库](https://github.com/codecrafters-io/build-your-own-x)。
改进 Agent 技能包请提 Issue 或 PR。

## 许可证

CC0 1.0 Universal — 详见 [LICENSE](LICENSE)。
