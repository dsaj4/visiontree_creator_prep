# 账号人设管理台账

更新时间：2026-05-10

这个文件用于管理 7 个账号的人设、主页资料、语气边界、创作者使用提示和后续人设升级流程。产物必须兼容 `content-system` 的个人主页 / persona 数据结构。

## 人设索引

| 账号 | displayName | 定位 | 工作区 | 主页资产状态 | 人设边界状态 | 例证工作流状态 | 同步到个人主页 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `thinking-lab` | Thinking Lab | 视觉 + 互动实验室 | `accounts/thinking-lab/` | 已预留 | v0.1 已初始化 | 待启动 | 待判断 |
| `milo` | Milo Reed | 工程师号 / 产品建设者 | `accounts/milo/` | 已预留 | v0.1 已初始化 | 待启动 | 待判断 |
| `ai-doubt` | AI Doubt Notes | 反 AI 怀疑者 / 公开怀疑笔记 | `accounts/ai-doubt/` | 已预留 | v0.1 已初始化 | 待启动 | 待判断 |
| `nora` | Nora Blake | 普通人试用号 / 非技术用户 | `accounts/nora/` | 已预留 | v0.1 已初始化 | 待启动 | 待判断 |
| `eli` | Eli Rowan | 造概念的慢思考号 | `accounts/eli/` | 已预留 | v0.1 已初始化 | 待启动 | 待判断 |
| `thinking-tree` | The Thinking Tree | 一棵会说话的树 | `accounts/thinking-tree/` | 已预留 | v0.1 已初始化 | 待启动 | 待判断 |
| `visiontree` | VisionTree | 官方号 / 叙事收拢 | `accounts/visiontree/` | 已预留 | v0.1 已初始化 | 待启动 | 待判断 |

## 工作区结构

每个账号工作区使用同一套目录，便于后续批量维护：

```text
accounts/{accountName}/
  00_persona_card.md
  01_x_profile_assets.md
  02_creator_discussion_log.md
  03_persona_evolution_log.md
  04_social_evidence_research.md
  assets/
    README.md
    avatar/
    banner/
    profile-screenshots/
  discussion-notes/
  persona-evolution/
  social-evidence/
  change-requests/
```

## 字段兼容要求

每个账号人设卡必须维护以下可同步字段：

- `accountName`
- `displayName`
- `role`
- `platform`
- `handle`
- `profileUrl`
- `positioning`
- `personaRole`
- `voice`
- `contentTypes`
- `avoid`
- `cadence`
- `interactionTarget`

## 主动更新规则

- 发现账号声音趋同，必须补充差异化语气和禁忌写法。
- 发现主页资料不能准确表达账号定位，必须提出主页字段修改。
- 发现某个账号的内容类型和实际运营不匹配，必须更新 `contentTypes` 与 `cadence`。
- 发现互动对象变化，必须更新 `interactionTarget`。
- 所有人设重大变动必须经过 `workflow/00_persona_update_workflow.md`：修改意见 -> 真实社媒例证 -> 同类案例整理 -> 修改质量评估 -> 正式提交。

## 当前初始化范围

本轮只完成 v0.1 人设卡、资产位置、讨论记录空间、演化日志空间和例证调研工作流。尚未开始真实 X 账号例证采集，也未替换 `content-system` 数据库中的 persona 字段。
