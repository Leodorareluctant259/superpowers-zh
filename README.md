# superpowers-zh（AI 编程超能力 · 中文版）

🌐 **简体中文** | [English (upstream)](https://github.com/obra/superpowers)

> **让你的 AI 编程助手真正会干活** — 从头脑风暴到代码审查，从 TDD 到调试，每个 skill 都是经过实战验证的工作方法论。

Chinese community edition of [superpowers](https://github.com/obra/superpowers), including full translations and China-specific development skills.

[![GitHub stars](https://img.shields.io/github/stars/jnMetaCode/superpowers-zh?style=social)](https://github.com/jnMetaCode/superpowers-zh)
[![npm version](https://img.shields.io/npm/v/superpowers-zh)](https://www.npmjs.com/package/superpowers-zh)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://makeapullrequest.com)
[![QQ群](https://img.shields.io/badge/QQ群-833585047-blue?logo=tencentqq)](https://qm.qq.com/q/x8kyqzlfDc)

### 📊 项目规模

| 📦 翻译 Skills | 🇨🇳 中国特色 Skills | 🤖 支持工具 |
|:---:|:---:|:---:|
| **14** | **5** | **Claude Code / Cursor / Codex / Kiro / DeerFlow / Trae / Antigravity / VS Code / Gemini** |

---

## 这是什么？

[superpowers](https://github.com/obra/superpowers) 是目前最火的 AI 编程 skills 框架（99k+ stars），为 Claude Code、Cursor 等 AI 编程工具提供**系统化的工作方法论**。

**superpowers-zh** 在完整翻译的基础上，新增了面向中国开发者的特色 skills：

### 翻译的 Skills（14 个）

| Skill | 用途 |
|-------|------|
| **头脑风暴** (brainstorming) | 需求分析 → 设计规格，不写代码先想清楚 |
| **编写计划** (writing-plans) | 把规格拆成可执行的实施步骤 |
| **执行计划** (executing-plans) | 按计划逐步实施，每步验证 |
| **测试驱动开发** (test-driven-development) | 严格 TDD：先写测试，再写代码 |
| **系统化调试** (systematic-debugging) | 四阶段调试法：定位→分析→假设→修复 |
| **请求代码审查** (requesting-code-review) | 派遣审查 agent 检查代码质量 |
| **接收代码审查** (receiving-code-review) | 技术严谨地处理审查反馈，拒绝敷衍 |
| **完成前验证** (verification-before-completion) | 证据先行——声称完成前必须跑验证 |
| **派遣并行 Agent** (dispatching-parallel-agents) | 多任务并发执行 |
| **子 Agent 驱动开发** (subagent-driven-development) | 每个任务一个 agent，两轮审查 |
| **Git Worktree 使用** (using-git-worktrees) | 隔离式特性开发 |
| **完成开发分支** (finishing-a-development-branch) | 合并/PR/保留/丢弃四选一 |
| **编写 Skills** (writing-skills) | 创建新 skill 的方法论 |
| **使用 Superpowers** (using-superpowers) | 元技能：如何调用和优先使用 skills |

### 🇨🇳 中国特色 Skills（5 个）

| Skill | 用途 | 上游有吗？ |
|-------|------|:---:|
| **中文代码审查** (chinese-code-review) | 符合国内团队文化的代码审查规范 | 无 |
| **中文 Git 工作流** (chinese-git-workflow) | 适配 Gitee/Coding/极狐 GitLab | 无 |
| **中文技术文档** (chinese-documentation) | 中文排版规范、中英混排、告别机翻味 | 无 |
| **中文提交规范** (chinese-commit-conventions) | 适配国内团队的 commit message 规范 | 无 |
| **MCP 服务器构建** (mcp-builder) | 构建生产级 MCP 工具，扩展 AI 能力边界 | 无 |

---

## 快速开始

### 方式一：npm 安装（推荐）

```bash
cd /your/project
npx superpowers-zh
```

### 方式二：手动安装

```bash
# 克隆仓库
git clone https://github.com/jnMetaCode/superpowers-zh.git

# 复制 skills 到你的项目（选择你使用的工具）
cp -r superpowers-zh/skills /your/project/.claude/skills      # Claude Code
cp -r superpowers-zh/skills /your/project/.cursor/skills      # Cursor
cp -r superpowers-zh/skills /your/project/.codex/skills       # Codex CLI
cp -r superpowers-zh/skills /your/project/.kiro/steering      # Kiro
cp -r superpowers-zh/skills /your/project/skills/custom       # DeerFlow 2.0
cp -r superpowers-zh/skills /your/project/.trae/rules         # Trae
cp -r superpowers-zh/skills /your/project/.antigravity        # Antigravity
```

### 方式三：在配置文件中引用

根据你使用的工具，在对应配置文件中引用 skills：

| 工具 | 配置文件 | 说明 |
|------|---------|------|
| Claude Code | `CLAUDE.md` | 项目根目录 |
| Kiro | `.kiro/steering/*.md` | 支持 always/globs/手动三种模式 |
| DeerFlow 2.0 | `skills/custom/*/SKILL.md` | 字节跳动开源 SuperAgent，自动发现自定义 skills |
| Trae | `.trae/rules/project_rules.md` | 项目级规则 |
| Antigravity | `GEMINI.md` 或 `AGENTS.md` | 项目根目录 |
| VS Code | `.github/copilot-instructions.md` | Copilot 自定义指令 |
| Cursor | `.cursor/rules/*.md` | 项目级规则目录 |

> **详细安装指南**：[Kiro](docs/README.kiro.md) · [DeerFlow](docs/README.deerflow.md) · [Trae](docs/README.trae.md) · [Antigravity](docs/README.antigravity.md) · [VS Code](docs/README.vscode.md) · [Codex](docs/README.codex.md) · [OpenCode](docs/README.opencode.md)

---

## 对比上游

| 特性 | superpowers (英文) | superpowers-zh (中文) |
|------|-------------------|----------------------|
| Skills 数量 | 14 | **19**（14 翻译 + 5 原创） |
| 语言 | 英文 | 中文（技术术语保留英文） |
| 代码审查规范 | 西方直接风格 | 适配国内团队沟通文化 |
| Git 平台 | GitHub 为主 | GitHub + Gitee + Coding + 极狐 |
| Git 提交规范 | 无 | Conventional Commits 中文适配 |
| 文档规范 | 英文 | 中文排版规范 + 中英混排 |
| MCP 构建 | 无 | MCP 服务器构建方法论 |
| 社区 | Discord | QQ 群 |

---

## 贡献

欢迎参与！翻译改进、新增 skills、Bug 修复都可以。

### 贡献方向

我们只接收符合 superpowers 定位的 skill——**AI 编程工作流方法论**。好的 skill 应该：

- 教 AI 助手**怎么干活**，而不是某个框架/语言的教程
- 解决上游英文版不覆盖的**中国开发者痛点**
- 有明确的步骤、检查清单、示例，AI 加载后能直接执行

欢迎提 Issue 讨论你的想法！

---

## 社区交流

| 群名 | 群号 | 加入方式 |
|------|------|---------|
| AI Agent 中文实践群 | **833585047** | [点击加入](https://qm.qq.com/q/x8kyqzlfDc) |

---

## 致谢

- 原始英文版：[obra/superpowers](https://github.com/obra/superpowers)（MIT 协议）
- 感谢 [@obra](https://github.com/obra) 创建了这个优秀的项目
- 姊妹项目：
  - [agency-agents-zh](https://github.com/jnMetaCode/agency-agents-zh) — 186 个 AI 智能体专家团队
  - [agency-orchestrator](https://github.com/jnMetaCode/agency-orchestrator) — 多智能体编排引擎，零代码 YAML 工作流
  - [shellward](https://github.com/jnMetaCode/shellward) — AI 智能体安全中间件，注入检测 + 数据防泄露

---

## 许可证

MIT License — 自由使用，商业或个人均可。

---

<div align="center">

**AI 编程超能力：让你的 AI 助手真正会干活**

[Star 本项目](https://github.com/jnMetaCode/superpowers-zh) · [提交 Issue](https://github.com/jnMetaCode/superpowers-zh/issues) · [贡献代码](https://github.com/jnMetaCode/superpowers-zh/pulls)

</div>
