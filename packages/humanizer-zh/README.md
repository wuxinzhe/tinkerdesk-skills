# tinkerdesk-skill-humanizer-zh

TinkerDesk 技能包 —— **AI 写作去痕工具（中文版）**：去除文本中的 AI 生成痕迹，让内容更自然、更像人类书写。

| 元信息 | 值 |
|---|---|
| 包名 | `tinkerdesk-skill-humanizer-zh` |
| 版本 | 1.0.0 |
| 分类 | `creative`（内容创作/润色） |
| 生态 | `tinkerdesk-skill` |
| 许可 | MIT |

> **声明**：核心文件翻译自 [blader/humanizer](https://github.com/blader/humanizer/tree/main)；实用工具部分（核心规则/快速检查清单/质量评分）参考 [hardikpandya/stop-slop](https://github.com/hardikpandya/stop-slop)；原始理论基于维基百科 [Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) 指南。

## 安装

通过 **TinkerDesk 技能市场**（npm 在线）安装：

- 市场按 `tinkerdesk-skill` keyword 检索生态包
- 分类选择「creative（内容创作/润色）」过滤命中本包
- 点安装 → 后端下载 tarball → 解析 SKILL.md → 结构化入库 → 立即可用

## 技能内容（SKILL.md）

frontmatter：

```yaml
name: humanizer-zh
description: 去除文本中的 AI 生成痕迹——让文本更自然、更像人类书写
allowed-tools:
  - Read
  - Write
  - Edit
  - AskUserQuestion
```

正文涵盖 **24 种 AI 写作痕迹** 的检测与修复规范，分四大类：

- 📝 **内容模式（6 种）** — 夸大象征意义、媒体吹捧、-ing 肤浅分析、宣传语、模糊归因、"挑战与展望"套路段
- 🔤 **语言语法模式（6 种）** — AI 词汇、系动词回避、否定排比、三段式、同义词循环、虚假范围
- 🎨 **风格模式（6 种）** — 破折号滥用、粗体滥用、内联标题列表、标题大写、表情符号、弯引号
- 💬 **交流模式（6 种）** — 协作言论、知识截止免责声明、谄媚语气、填充短语、过度限定、通用积极结论

附带：
- 常见 AI 词汇警示列表（此外/至关重要/深入探讨/无缝…）
- 改写原则（⚠️ 不仅要"干净"更要"鲜活"——有观点、变节奏、允许混乱、具体细节）
- 改写前后示例对比

## 使用

在 TinkerDesk 对话中调用该技能，粘贴 AI 生成文本 → Agent 按 SKILL.md 规则扫描 24 种模式 → 输出人性化改写（保留核心含义 + 注入真实个性）。

无需依赖 CLI 或 Claude Code——纯技能正文驱动。

## 参考

- [blader/humanizer](https://github.com/blader/humanizer) — 英文原版
- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
- [WikiProject AI Cleanup](https://en.wikipedia.org/wiki/Wikipedia:WikiProject_AI_Cleanup)

## 语义说明

本工具不是为了"欺骗"AI 检测器，而是提升真实写作质量——最好的"去 AI 化"是让文字有真实的人类思考和声音。

> 由 tinkerdesk-skills monorepo CI 自动发布维护。

> CI pathspec 修复验证。
