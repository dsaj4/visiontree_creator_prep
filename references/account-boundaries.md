# 账号与口径边界

更新时间：2026-05-09

## 账号分工

- `thinking-lab`：视觉 + 互动实验室。三秒看懂，少解释，多动作。
- `milo`：工程师号 / 产品建设者。短句、克制，讲真实技术选择和产品取舍。
- `ai-doubt`：反 AI 怀疑者 / 公开怀疑笔记。短、刺、冷静、有事实。
- `nora`：普通人试用号 / 非技术用户。真实、日常、不装懂。
- `eli`：造概念的慢思考号。慢、稳、有思想密度。
- `thinking-tree`：一棵会说话的树。平静，淡淡幽默，不卖萌。
- `visiontree`：官方号 / 叙事收拢。清楚、克制、有定义感。

## 人设管理要求

每个账号都要维护可同步到 `content-system` 个人主页的字段：

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

人设资料必须同时服务两类使用：

- 给人工创作者看：帮助理解账号声音、边界和选题倾向。
- 给 `content-system` 用：可更新个人主页与账号资料字段。

当账号声音、内容边界、主页展示或互动目标发生变化时，应主动更新 `05-account-personas/persona-index.md`，并标记是否需要同步到个人主页。

## 全局禁写

- 不写成替人思考的 AI。
- 不写成自动决策系统。
- 不写成成熟第二大脑或知识管理工具。
- 不写成模型库、prompt 模板库或 skill 平台。
- 不把 Tree 写成当前成熟产品能力。
- 不虚构用户结果、平台数据或产品成熟度。
