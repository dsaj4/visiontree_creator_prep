# 模板库索引

更新时间：2026-05-09

| 模板 ID | 适合账号 | 内容类型 | 用途 | 状态 |
| --- | --- | --- | --- | --- |
| `tpl-thinking-lab-visual-experiment` | `thinking-lab` | 图解 / 实验 | 把一个模型转成图或互动题 | 待整理 |
| `tpl-eli-slow-concept` | `eli` | 概念帖 | 命名概念并分场景打开 | 待整理 |
| `tpl-ai-doubt-short-note` | `ai-doubt` | 三句短帖 | 观察、反问、判断 | 待整理 |
| `tpl-milo-build-note` | `milo` | 工程取舍 | 真实问题、两个选项、最终选择、为什么 | 待整理 |
| `tpl-nora-diary-note` | `nora` | 试用日记 | 使用、卡住、帮助、不确定 | 待整理 |
| `tpl-thinking-tree-monologue` | `thinking-tree` | 树的独白 | 树的动作、思维模型、隐喻、图像方向 | 待整理 |
| `tpl-visiontree-category` | `visiontree` | 官方定义 | 不是什么、是什么、为什么重要 | 待整理 |

## 模板文件格式

```md
# 模板名称

- 模板 ID：
- content-system templateId：
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
- `referenceCount` 不在本工作区手写，由 `content-system` 根据已发布内容计算。
