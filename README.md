---
AIGC:
    Label: "1"
    ContentProducer: 001191440300708461136T1XGW3
    ProduceID: 7af529a0f6360cc6a80ea7b1bc937927_39aa476971c311f1b2f55254006c9bbf
    ReservedCode1: vKD0C/N8mNvOvFXXg3MtWqKwOx4XHFoA6KvtHvdWDt8ZOh1eMr43PNJnyQolH0NFzRXFFuemBIE7sYQiDgaDQ+cflg9gjh37Vfo3xkyIloHIxg8S/UDeFz5cjxiwGb+v9EcYdTTrxohEp4tSyEthe26bw+irHta2W3EGZDKMeqzyGqt63oh+1D3QDsg=
    ContentPropagator: 001191440300708461136T1XGW3
    PropagateID: 7af529a0f6360cc6a80ea7b1bc937927_39aa476971c311f1b2f55254006c9bbf
    ReservedCode2: vKD0C/N8mNvOvFXXg3MtWqKwOx4XHFoA6KvtHvdWDt8ZOh1eMr43PNJnyQolH0NFzRXFFuemBIE7sYQiDgaDQ+cflg9gjh37Vfo3xkyIloHIxg8S/UDeFz5cjxiwGb+v9EcYdTTrxohEp4tSyEthe26bw+irHta2W3EGZDKMeqzyGqt63oh+1D3QDsg=
---



# AGENTS.md 项目基础规范

> A baseline specification for AI coding agents — every project should have one.

---

## English

### What is this?

**AGENTS.md** is a simple, open format for guiding AI coding agents (Cursor, Windsurf, Copilot, etc.) in your project. Think of it as a README for agents: a dedicated, predictable place to provide context and instructions that help AI agents collaborate effectively with your codebase.

### Why AGENTS.md?

- **For Agents, not Humans**: README.md stays clean for human contributors; AGENTS.md provides precise, agent-oriented guidance.
- **Predictable Location**: Agents always know where to look — the project root.
- **Reduces Guesswork**: Explicit rules prevent agents from making wrong assumptions about your tech stack, conventions, and workflows.

### Quick Start

1. Create a file named `AGENTS.md` in your project root.
2. Fill it with agent-specific instructions (see the template in this repo).
3. Also keep `README.md` (for humans) and `LESSONS.md` (for accumulated experience).

### Recommended Companion Files

| File | Purpose |
|------|---------|
| `AGENTS.md` | Rules and conventions for AI coding agents |
| `README.md` | Project introduction for human contributors |
| `LESSONS.md` | Mistakes, failures, and lessons learned |
| `CONTRIBUTING.md` | How to contribute to the project |
| `CHANGELOG.md` | Version history and release notes |
| `LICENSE` | Open source license |
| `.gitignore` | Files and directories to exclude from version control |

### Core Principles

1. **Open Source = Zero Secrets**: `.gitignore` blocks all credentials, keys, tokens, and personal configs. Anyone cloning the repo should be able to run it but never access your secrets.
2. **Private Repo = Maximize Transferability**: Upload everything except cache and build artifacts. Better to push one extra config file than leave a teammate stranded.
3. **Copyleft by Default**: GPL v3 ensures derivatives stay open. Use my code → your code must also be GPL.

See `.gitignore` for detailed scenario switching comments.

### License

GNU General Public License v3.0 — Derivatives must also be GPL open source.

---

## 中文

### 这是什么？

**AGENTS.md** 是一个简单、开放的格式，用于在你的项目中指导 AI 编程智能体（如 Cursor、Windsurf、Copilot 等）。可以把它理解为给 Agent 看的 README：一个专门且可预测的位置，用来提供上下文和指令，帮助 AI Agent 与你的代码库高效协作。

### 为什么需要 AGENTS.md？

- **面向 Agent，非人类**：README.md 保持简洁，专注于人类贡献者；AGENTS.md 提供精确的、面向 Agent 的指导。
- **可预测的位置**：Agent 永远知道去哪里找 —— 项目根目录。
- **减少猜测**：明确的规则防止 Agent 对你的技术栈、规范和流程做出错误假设。

### 快速开始

1. 在项目根目录创建名为 `AGENTS.md` 的文件。
2. 填入面向 Agent 的专属指令（参考本仓库中的模板）。
3. 同时维护 `README.md`（面向人类）和 `LESSONS.md`（积累经验教训）。

### 推荐配套文件

| 文件 | 用途 |
|------|------|
| `AGENTS.md` | AI 编程智能体的规则与规范 |
| `README.md` | 面向人类贡献者的项目介绍 |
| `LESSONS.md` | 错误、失败和经验教训记录 |
| `CONTRIBUTING.md` | 如何为项目做贡献 |
| `CHANGELOG.md` | 版本历史与发布说明 |
| `LICENSE` | 开源许可证 |
| `.gitignore` | 排除版本控制的文件与目录 |

### 核心原则

1. **开源项目 = 零秘密**：`.gitignore` 拦截所有密钥、密码、Token 和个人配置。随便谁 clone 下来都能跑，但拿不到你任何秘密。
2. **私有项目 = 最大化可传输性**：除了缓存和编译垃圾，能传的全传。宁可多传一个配置文件，也别让同事 clone 下来跑不起来。
3. **默认 Copyleft**：GPL v3 确保衍生作品必须同样开源。用了我的代码，你的也得 GPL。

详见 `.gitignore` 中的场景切换注释。

### 许可证

GNU General Public License v3.0 — 衍生作品必须同样以 GPL 开源。
*（内容由AI生成，仅供参考）*
*（内容由AI生成，仅供参考）*
