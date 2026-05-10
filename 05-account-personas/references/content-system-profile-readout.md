# content-system 个人主页读取说明

更新时间：2026-05-10

本文件记录 `content-system` 当前“个人主页”模块如何读取和展示 persona 数据，用于将 `05-account-personas` 作为后续人设修改后台。

## 1. 当前页面位置

- 前端文件：`content-system/src/App.tsx`
- 组件：`ProfileView`
- 入口导航：`个人主页`
- 类型定义：`UserAccount`
- 后端文件：`content-system/server/api.mjs`
- 数据表：`users`

当前个人主页是只读展示页，不提供前端编辑、头像上传、banner 管理或人设版本管理。

## 2. 当前展示结构

### Hero 区

展示字段：

- `displayName`
- `personaRole`
- `positioning`
- `role`
- `platform`
- `handle`
- `profileUrl`

当前头像不是图片，而是：

```tsx
currentUser.displayName.slice(0, 2)
```

也就是用展示名的前两个字符生成文本头像。

### 账号设定

展示字段：

- `voice`
- `contentTypes`
- `avoid`

展示形式为三组标签：

- 语气
- 内容类型
- 不要写

### 首周运营

展示字段：

- `cadence`
- `interactionTarget`

展示形式：

- 发布节奏
- 互动目标

### V2 账号矩阵

展示字段来自 `accounts` 列表：

- `displayName`
- `positioning`
- `role`
- `platform`
- `handle`

当前登录账号会高亮。

## 3. 数据链路

```text
users 表
  -> api.mjs mapUser(row)
  -> POST /api/login 返回 user
  -> GET /api/bootstrap 返回 user + accounts
  -> App.tsx ProfileView 展示
```

### 后端字段映射

| SQLite 字段 | API 字段 | 05 人设卡字段 |
| --- | --- | --- |
| `account_name` | `accountName` | `accountName` |
| `display_name` | `displayName` | `displayName` |
| `role` | `role` | `role` |
| `platform` | `platform` | `platform` |
| `handle` | `handle` | `handle` |
| `profile_url` | `profileUrl` | `profileUrl` |
| `positioning` | `positioning` | `positioning` |
| `persona_role` | `personaRole` | `personaRole` |
| `voice_json` | `voice` | `voice` |
| `content_types_json` | `contentTypes` | `contentTypes` |
| `avoid_json` | `avoid` | `avoid` |
| `cadence` | `cadence` | `cadence` |
| `interaction_target` | `interactionTarget` | `interactionTarget` |

`voice`、`contentTypes`、`avoid` 在数据库中是 JSON 字符串，在 API 中解析为数组。

## 4. 与 05 后台的关系

当前 `05-account-personas/accounts/{accountName}/00_persona_card.md` 已覆盖 `content-system` 个人主页所需字段。

`05` 中额外维护、但当前个人主页尚未展示的内容：

- X 头像资产
- X banner 资产
- profile screenshots
- tagline / bio 候选
- Pinned Post 方向
- 创作者讨论记录
- 人设演化日志
- 社媒例证调研
- 人设修改请求和质量评估

这些内容可以作为后续扩展个人主页或后台编辑系统的新增模块。

## 5. 当前缺口

如果要让 `05` 真正成为个人主页人设修改后台，需要补齐：

- 个人主页字段编辑接口，目前没有 `PATCH /api/users/:id` 或 persona 更新 API。
- 头像 / banner 字段，目前 `users` 表没有 `avatar_url`、`banner_url`。
- 主页 bio / tagline / pinned post 字段，目前只存在 `personaRole`，没有独立主页文案字段。
- 人设版本字段，目前没有 `persona_version`、`updated_at`、`change_id`。
- 例证与审核流程字段，目前没有关联 `change-requests`、`social-evidence` 或质量评估结果。
- 前端个人主页目前展示的是当前登录账号，不支持切换查看其他账号详情，只在矩阵卡片里展示摘要。

## 6. 建议的下一步对接方向

### 最小同步

先将 `05` 的 `00_persona_card.md` 作为源文档，人工确认后同步到 `users` 表现有字段。

优点：改动小，能立刻更新个人主页。

限制：头像、banner、bio、版本记录和例证流程仍然只在 05 中维护。

### 后台化扩展

新增 persona 更新 API 和字段：

- `avatarUrl`
- `bannerUrl`
- `tagline`
- `bio`
- `pinnedPostDirection`
- `personaVersion`
- `personaUpdatedAt`
- `personaChangeId`

同时在个人主页增加：

- 主页资产预览
- bio / tagline 展示
- 人设版本与最近变更说明
- “来自 05 后台”的同步状态

### 工作流闭环

把 `05-account-personas/workflow/00_persona_update_workflow.md` 中的变更请求、社媒例证、质量评估和正式提交记录，未来映射为 `content-system` 的后台审核状态。

建议状态：

- `draft`
- `researching`
- `reviewing`
- `approved`
- `synced`
- `rejected`

## 7. 关键判断

当前 `content-system` 的个人主页足够展示基础人设，但还不是人设管理后台。`05-account-personas` 应继续作为人设后台源头，先维护深度理解、资产和证据链；等字段稳定后，再决定是否把编辑和同步能力接入 `content-system`。
