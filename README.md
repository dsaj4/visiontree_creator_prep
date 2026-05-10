# Creator Prep Workspace

更新时间：2026-05-09

这个工作区用于“创作前准备”，服务人工创作者。这里不生成最终草稿，不写入内容池，也不替代人工完成内容转化。

## 职责范围

负责：

- 素材整理：整理上游资料和素材来源，提炼可供创作者使用的素材卡。
- 模板制作：制作账号差异化模板、结构模板、禁忌写法和使用说明。
- 账号人设完善管理：维护 7 个账号的定位、语气、内容边界、主页资料和创作者使用提示。
- 为创作者准备选题、素材、模板和口径边界简报。
- 主动更新 `content-system` 可消费的素材池、模板库和个人主页兼容产物。

不负责：

- 生成最终草稿。
- 创建 `content-system` 内容记录。
- 代替人工判断内容是否发布。
- 将平台指标写成事实。

## 工作区目录

- `00-inbox/`：新收到但未整理的资料、链接、截图说明、会议摘录。
- `01-source-materials/`：上游资料索引和来源追踪。
- `02-asset-cards/`：可直接服务创作者的素材卡。
- `03-template-library/`：账号模板、结构模板和禁忌写法。
- `04-creator-briefs/`：交给创作者的创作前简报。
- `05-account-personas/`：账号人设、主页资料、语气边界和更新台账。
- `references/`：项目口径、账号矩阵、字段规则。

## 输出标准

每个交付给创作者的准备包应包含：

- 适合账号。
- 内容入口或选题方向。
- 可引用素材。
- 推荐模板。
- 必守口径。
- 禁忌误写。
- 需要人工判断的问题。

## 与 content-system 兼容

本工作区的产物必须能被 `content-system` 继续使用，至少兼容以下三个模块：

- 素材池：素材卡必须能映射到 `assets` 字段，包括 `title`、`theme`、`source`、`format`、`freshness`、`score`、`tags`、`summary`、`owner`、`palette`、`notes`、`resources`。
- 模板库：模板必须能映射到 `templates` 字段，包括 `title`、`format`、`channels`、`structure`、`hook`、`length`、`notes`、`resources`。
- 个人主页：账号人设资料必须能映射到 `users` / persona 字段，包括 `accountName`、`displayName`、`role`、`platform`、`handle`、`profileUrl`、`positioning`、`personaRole`、`voice`、`contentTypes`、`avoid`、`cadence`、`interactionTarget`。

## 主动更新机制

- 发现素材口径、来源、可引用重点或误用边界不完整时，主动更新素材卡，并标记是否需要同步到 `content-system` 素材池。
- 发现模板结构不清、账号声音趋同或禁忌写法缺失时，主动更新模板，并标记是否需要同步到 `content-system` 模板库。
- 发现账号定位、主页资料、语气边界或互动目标不完整时，主动更新账号人设，并标记是否需要同步到 `content-system` 个人主页。
- 所有主动修改必须记录修改原因、影响模块、兼容字段和同步状态。

## VisionTree 口径边界

- 当前对外主定义：认知增强引擎。
- 当前传播重点：Vision，即内部一致的视角 / 认知框架。
- Tree 是长期方向，不能写成已经成熟落地的产品能力。
- 不写成“AI 替你思考”。
- 不写成第二大脑、知识管理工具、模型库、prompt 模板库或 skill 平台。
