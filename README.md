# 科研流程协议 · Agent-Centric Research Protocol

> 一个 **Markdown 驱动 + Agent 主导** 的科研协作模板。
> 你给方向，Agent 跑实验，整个研究过程沉淀为可读、可复现、可多人协作的文档。

## 这是什么

- **模板仓库**：每个新研究项目从它实例化出独立 repo。
- **核心机制**：所有研究状态（idea / method / 议题 / 实验日志）都以 Markdown 落盘；Agent 负责重复执行，你专注高阶决策。
- **协议正文**：见 [`AGENTS.md`](AGENTS.md)（唯一来源）。

## 谁应该用

- 一作 / PhD 学生：把 Agent 当协作者跑实验、做消融。
- 小团队 PI + 学生：用 `Discussion.md` 作为异步主战场，多人协作不丢上下文。
- 任何想让"半年后还能复现自己实验"的人。

## 怎么实例化一个新研究

```bash
# 1. GitHub 上点 "Use this template" → 创建你的研究 repo（例如 my-research-X）
# 2. clone 下来
git clone <your-new-repo-url>
cd <your-new-repo>

# 3. 装协议自检 hook（pre-commit 自动跑 lint）
bash tools/install_hooks.sh

# 4. 打开 Claude Code（或 Cursor / Codex）
#    会自动检测到 bootstrap.md，引导你选 A=新手 / B=老手 模式
#    选完后开始写你自己的 idea.md
```

## 关键文件一览

| 文件 | 作用 |
|---|---|
| `AGENTS.md` | 协议正文（必读） |
| `bootstrap.md` | 首次初始化向导（用完即删） |
| `idea.md` / `method.md` | 研究问题 / 数学方法 |
| `Discussion.md` | 当前 active 议题（一议题一主线） |
| `LOGS/YYYY-Www.md` | 周实验日志 |
| `tools/` | 新建周志 / 新建实验 / 协议 lint 三件套 |

## License

模板本身按需自选；衍生的科研仓库内容版权归各使用者所有。
