# Content System 兼容规范

更新时间：2026-05-09

本规范要求 `creator-prep-workspace` 的所有产物都能兼容 `content-system` 的素材池、模板库和个人主页。

## 1. 素材池兼容

素材卡必须可映射到 `assets`：

| 本工作区 | content-system |
| --- | --- |
| 素材卡 ID / assetId | `id` |
| 标题 | `title` |
| 主题 | `theme` |
| 来源 | `source` |
| 格式 | `format` |
| 新鲜度 | `freshness` |
| 优先级评分 | `score` |
| 标签 | `tags` |
| 创作摘要 | `summary` |
| 适合账号 / owner | `owner` |
| 视觉标识 | `palette` |
| 使用提示和误用边界 | `notes` |
| 原始资料链接或文件 | `resources` |

主动更新触发条件：

- 来源不完整。
- 摘要不能直接帮助创作。
- notes 缺少“适合怎么用”或“不要怎么误用”。
- 适合账号或标签不准确。

## 2. 模板库兼容

模板必须可映射到 `templates`：

| 本工作区 | content-system |
| --- | --- |
| 模板 ID / templateId | `id` |
| 模板名 | `title` |
| 内容类型 | `format` |
| 渠道 | `channels` |
| 结构步骤 | `structure` |
| 开场方式 | `hook` |
| 建议长度 | `length` |
| 使用提示和禁忌 | `notes` |
| 参考资料 | `resources` |

主动更新触发条件：

- 模板不能体现账号差异。
- `structure` 不够可执行。
- 缺少适用素材或禁忌写法。
- 同一主题在多个账号上出现同质化表达。

## 3. 个人主页兼容

账号人设必须可映射到 `users` / persona：

| 本工作区 | content-system |
| --- | --- |
| 账号名 | `accountName` |
| 展示名 | `displayName` |
| 负责人 / 角色 | `role` |
| 平台 | `platform` |
| 平台 handle | `handle` |
| 主页链接 | `profileUrl` |
| 账号定位 | `positioning` |
| 人设作用 | `personaRole` |
| 声音关键词 | `voice` |
| 内容类型 | `contentTypes` |
| 禁忌写法 | `avoid` |
| 发布节奏 | `cadence` |
| 互动对象 | `interactionTarget` |

主动更新触发条件：

- 主页资料和账号定位不一致。
- 人设说明不能指导创作者。
- 语气边界不清导致多个账号声音趋同。
- 内容类型、发布节奏或互动对象发生变化。

## 4. 同步状态

每个素材、模板、人设产物都必须标记：

- `未同步`：只在准备区存在。
- `待同步`：已整理完成，建议更新到 `content-system`。
- `已同步`：已经进入 `content-system`。
- `不同步`：仅作为内部参考，不进入系统。

