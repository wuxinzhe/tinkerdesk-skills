# tinkerdesk-skills

TinkerDesk 技能 monorepo —— **单仓库维护所有技能包**。

## 结构

每个技能是一个独立 npm 包（保留独立发布端——`search` 分页/`keywords` 分类能力），收敛到这一个仓库维护：

```
packages/
├── release-management/    → tinkerdesk-skill-release-management
│   ├── SKILL.md / README.md / LICENSE / package.json
└── humanizer-zh/          → tinkerdesk-skill-humanizer-zh
    ├── SKILL.md / README.md / LICENSE / package.json
```

## 新增技能

```bash
mkdir packages/<skill-name>
cp <源 SKILL.md> packages/<skill-name>/SKILL.md
# package.json keywords: ["tinkerdesk-skill", "<classification>"]
# 推送 → CI 自动 npm publish
```

## 发布

单仓库 + CI 自动拆包发布：检测 `packages/*` 任一目录变更 → 对变更的包 `npm publish`（独立包名的 search 分页/分类能力保留）。

## 规范

- 包名 `tinkerdesk-skill-<name>`
- `keywords` 含 `tinkerdesk-skill`（市场生态打标） + 分类词（`SKILL_MARKET_CATEGORIES`）
- 每个包：`SKILL.md`（frontmatter+正文）+ `README.md` + `LICENSE` + `package.json`
