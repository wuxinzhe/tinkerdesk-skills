# tinkerdesk-skill-release-management

TinkerDesk 技能包 —— **项目发布管理**：Git 分支策略、发版流程、多环境隔离、Docker 部署方案。

| 元信息 | 值 |
|---|---|
| 包名 | `tinkerdesk-skill-release-management` |
| 版本 | 1.4.0 |
| 分类 | `code`（开发） |
| 生态 | `tinkerdesk-skill` |
| 许可 | MIT |

## 安装

通过 **TinkerDesk 技能市场**（npm 在线）安装：

- 市场按 `tinkerdesk-skill` keyword 检索生态包
- 分类选择「code（开发）」过滤命中本包
- 点安装 → 后端下载 tarball → 解析 SKILL.md → 结构化入库 → 立即可用

## 技能内容（SKILL.md）

frontmatter：

```yaml
name: release-management
description: "项目发布管理：Git 分支策略（main/release/feat）、发版流程、多环境隔离（dev/staging/prod）、Docker 部署方案"
version: 1.4.0
author: Hermes Agent
license: MIT
platforms: [windows, linux, macos]
```

正文涵盖：

- **Git 分支策略** — `main`（受保护）/ `release`（发版）/ `feat/*`（开发）分支模型
- **发版流程** — 迭代开发 → 合并 release → 打 tag → 发布
- **多环境隔离** — dev / staging / prod 三环境边界与配置管理
- **Docker Compose 部署** — 服务编排、日志、数据卷方案

## 使用

在 TinkerDesk 中加载 Agent 后，调用该技能可获得发布管理流程指引（Agent 按技能正文执行分支/发版/部署操作）。

## 参考

- 配套技能：`github-workflow`（GitHub 全流程：认证/仓库/PR/CI）、`docker-ops`（Docker Compose 运维）
- agentskills 规范：<https://agentskills.io/specification>

## 发布维护

- 改版：更新 `SKILL.md` 的 `version` → `npm version <next>`（同步 package.json ∕ 打 tag）→ 重发 npm
- 仓库：GitHub（`wuxinzhe` 维护者，官方标记）
