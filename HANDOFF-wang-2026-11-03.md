# Glofter 交接 — wang → 暂停（2026-11-03 20:05 CST）

用户指令（经 Hiker）：**立即暂停全部工作**。本交接后 wang 不再新开研发，直至用户再次下达。

## 1. 已停

- 本地子任务：无在跑（StopSubagent all）
- Cloud Agent：本会话启动的 38 个均已 **finished**；近期 P2 相关已 unwatch；无 running
- 后台业务进程：无自起的 studio/hub 服务；仅有 box 系统进程

## 2. Git / 分支 / push

| 路径 | 分支 | HEAD | dirty | 说明 |
|------|------|------|-------|------|
| `glofter-repos/hub` | `main` | `9e23b0a` | 干净 | 已含 P2.14+P2.15 |
| `glofter-repos/studio` | `main` | `60e2f1d` | 干净 | 已含 P2.12+P2.13 |
| `glofter-repos/app` | `main` | `a26426a` | 干净 | P0.5 hygiene |
| `glofter-repos/protocol` | `main` | `939ed01` | 干净 | |
| `glofter-repos/themes` | `main` | `81186fb` | 干净 | |
| `glofter-repos/website` | `main` | `3c1286e` | 干净 | |
| `glofter-arc` | `main` | WIP commit（见下） | 已 commit | **无 remote**；仅冻结本机脏改动 |

- **无 open PR**（hub / studio / app / .github）
- 六仓无需额外 commit/push（均已对齐 origin/main）
- `glofter-arc`：无 GitHub remote；已本地 WIP commit 冻结 P0 时代残留（themes-zip / media-backfill / docs）；**真源是 split repos**，勿把 arc 当继续开发主线

## 3. 已合入（本轮关键）

### P2.14 — Hub PK resolver
- PR: https://github.com/glofter/hub/pull/8 → merge `4945533`
- 口径：cache→nft→chain→body；`GLOFTER_HUB_PK_RESOLVER`；`GLOFTER_HUB_ALLOW_BODY_STUDIO_PK` 默认 1；链仅 beta/test；PaymentKit/stake OUT
- 计划勾选：https://github.com/glofter/.github/pull/13

### P2.15 — Signed JSON discover push
- PR: https://github.com/glofter/hub/pull/9 → merge `9e23b0a`
- 口径：json-cards-only；`POST /api/hub/studios/self/content`；仅 approved；默认 upsert，`mode=replace` 全量；与 pull 并存写 `discover_items`；无 binary
- 计划勾选：https://github.com/glofter/.github/pull/14 → merge `63ffeee`

### 更早已勾（计划页）
- P0 全勾；P1.7–10 全勾；P2.12–15 全勾
- 计划：https://github.com/glofter/.github/blob/main/DEVELOPMENT_PLAN.md

### 近期合并索引（节选）
| 项 | PR | merge |
|----|-----|-------|
| P2.15 hub push | [hub#9](https://github.com/glofter/hub/pull/9) | `9e23b0a` |
| P2.14 hub PK | [hub#8](https://github.com/glofter/hub/pull/8) | `4945533` |
| P2.13 media-store | [studio#11](https://github.com/glofter/studio/pull/11) | `60e2f1d` |
| P2.12 GIF/HEIC/resize | [studio#10](https://github.com/glofter/studio/pull/10) | （main 上，早于 60e2f1d） |
| P2.15 plan check | [.github#14](https://github.com/glofter/.github/pull/14) | `63ffeee` |
| P2.14 plan check | [.github#13](https://github.com/glofter/.github/pull/13) | |
| P2.13 plan check | [.github#12](https://github.com/glofter/.github/pull/12) | |

## 4. 未完成与 blocker

| 项 | 状态 | Blocker |
|----|------|---------|
| **P1.11** App store prep（`eas init` / credentials / 商店物料） | 未勾 | **需用户 EAS + App Store / Play 账号**；wang 无法独自推进 |
| AUP in-daemon SPA | 明确延期 | P1.8 选 (B) shell-only；另立项 |
| 完整 Web Device 主题 | 明确延期 | 另立项重建，非迁移开关 |
| PaymentKit / stake | OUT | 产品冻结 |

## 5. 口径备忘（用户定调）

- AUP = 门面（`:4900` deep-link）
- Fastify = 产品（Choice B）
- CSS packs = ARC 公网主题
- 不承诺旧 React 主题在 AUP/Web Device 原样开发/运行

## 6. 下一步建议（用户再开闸后）

1. **优先**：用户提供 EAS/商店账号 → 做 **P1.11**
2. 或：新产品切片（需 Hiker/用户点名范围）— 例如 in-daemon SPA、Web Device 主题立项、Studio 侧 content-push 客户端调用
3. 可选：用 `sync-repos.sh` 把 split mains 回灌 `glofter-arc`（当前 arc 落后，且仅本机）

## 7. 本机路径

- Split clones: `/workspace/glofter-repos/{hub,studio,app,protocol,themes,website}`
- Monorepo mirror: `/workspace/glofter-arc`（无 remote）
- 本交接文件: `/workspace/notes/glofter-wang-handoff-2026-11-03.md`
