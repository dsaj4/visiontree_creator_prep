# 模板库索引

更新时间：2026-05-17

| 模板 ID | 标签 | 适合账号 | 内容类型 | 用途 | 状态 |
| --- | --- | --- | --- | --- | --- |
| `tpl-garden-web-video-presentation` | 工具 / 流程 | `thinking-lab` / `visiontree` / `milo` / `eli` | 网页视频 / 动态演示 | 把文章、口播稿或产品说明转成可录屏的 16:9 点击驱动网页演示 | 已同步 |
| `tool-garden-gpt-image-2` | 工具 / 流程 | `thinking-lab` / `visiontree` / `thinking-tree` / `nora` / `milo` / `eli` | 图像生成 / 视觉工具 | 用模式感知工作流把视觉需求转成可执行 prompt 或图片生成任务 | 已同步 |

## 最新案例

| 案例 ID | 对应模板 | 产物类型 | 运行效果 | 用途 | 文件 |
| --- | --- | --- | --- | --- | --- |
| `case-labor-education-web-video` | `tpl-garden-web-video-presentation` | 劳动教育结课报告网页视频 | 9 章点击驱动 16:9 网页舞台，可录屏为 3-5 分钟口播视频 | 展示模板如何把完整口播、分镜、视觉风格、素材清单和 React 演示工程串成案例 | `examples/labor-education-web-video/README.md` |

## 下一步改造方向

已确定采用“创作者运行手册版”：模板正文保留可同步字段，案例细节沉淀在 `examples/`。详见 `template-library-upgrade-plan.md`。

2026-05-17 前端实现状态：`content-system` 模板详情页已按“创作者快速判断 / 开始使用 / 运行效果与验收 / 真实案例与来源”展示，前端会读取 `notes` 前缀进行分组。本工作区后续新增模板时必须按此展示结构填写。

## 模板文件格式

```md
# 模板名称

- 模板 ID：
- content-system templateId：
- 标签：
- 适合账号：
- 内容类型：
- 适合素材：
- title：
- format：
- channels：
- Hook：
- Structure：
- Length：
- notes：
- resources：
- 使用边界：
- 运行效果：
- 使用方法：
- 最新案例：
- content-system 展示映射：
- 语气：
- 禁忌：
- 创作者提示：
- 人工判断点：
- 同步到模板库：未同步 / 待同步 / 已同步 / 不同步
- 最近更新原因：
```

## 兼容要求

- 模板必须能转换为 `content-system` 的模板库记录。
- `structure` 必须简洁、可执行，供前端展示和创作者套用。
- 同一主题给不同账号使用时，应使用不同模板或不同模板变体。
- `notes` 必须包含适用账号、适用素材、禁忌写法。
- `notes` 进入前端后应使用 `适用范围：`、`准备输入：`、`使用边界：`、`操作方式：`、`运行效果：`、`验收方式：`、`最新案例：` 等前缀，便于前端分组展示。
- `resources` 必须至少包含来源资料；有真实案例时，必须补一个案例资源，说明运行效果和可迁移方法。
- `referenceCount` 不在本工作区手写，由 `content-system` 根据已发布内容计算。

## 工具型模板说明

- `tool-*` 条目表示可被创作者 brief 引用的制作工具或工作流。
- 具备制作能力或操作流程属性的条目，统一在索引和正文中标记 `工具 / 流程`，即使模板 ID 暂未使用 `tool-*` 前缀。
- 工具型模板仍需保留 `content-system` 模板字段映射，方便后续进入模板库。
- 工具型模板不表示 `content-system` 已具备对应执行能力；同步前必须由系统负责人确认运行边界。
- 已同步到 `content-system` 时，默认同步为介绍卡片；真实工具说明继续保留在本目录，案例截图后续补进卡片资源。
