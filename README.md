# Skills

面向多种 AI Agent 的个人 Skill 仓库。仓库中的 Skill 优先遵循 [Agent Skills](https://agentskills.io/) 开放规范，核心指令保持跨产品兼容，产品专属配置放在独立的附加文件中。

## Skill 列表

| Skill | 作用 |
| --- | --- |
| [`writing-source-code-analysis`](skills/writing-source-code-analysis/) | 研究源码，并规划、撰写、改写或审校中文源码解析文章 |

## 安装

使用 [`skills`](https://github.com/vercel-labs/skills) CLI 可以将仓库中的 Skill 安装到 Codex、Claude Code、Kimi Code CLI 等本地 Agent。

从 GitHub 全局安装：

```bash
npx skills add Minjo620/skills \
  --skill writing-source-code-analysis \
  --global \
  --agent codex \
  --agent claude-code \
  --agent kimi-code-cli
```

本地开发时，在仓库根目录运行：

```bash
npx skills add . \
  --skill writing-source-code-analysis \
  --global \
  --agent codex \
  --agent claude-code \
  --agent kimi-code-cli
```

交互安装时优先选择符号链接，让 Git 仓库成为唯一源码。

## 调用

```text
Codex:      $writing-source-code-analysis
Claude Code: /writing-source-code-analysis
Kimi Code:   /skill:writing-source-code-analysis
```

自然语言请求与 Skill 的 `description` 匹配时，各 Agent 也可以自动调用。
