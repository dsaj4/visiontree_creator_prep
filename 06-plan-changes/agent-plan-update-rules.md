# Agent 计划修改规范

## 核心规则

计划修改只改变 `plans`，不创建 `contents`。

Agent 收到“设定计划、修改计划、删除旧计划、上传前计划安排”等请求时，应默认执行计划日历更新，而不是创建内容库草稿。只有用户明确说“创建草稿 / 保存草稿 / 写入内容池草稿”，才可以调用内容草稿接口。

## 正确流程

1. 在本目录新增或更新计划修改记录。
2. 检查是否需要删除旧计划。
3. 通过 `content-system` 计划 API 或受控脚本更新 `plans`。
4. 校验 `plans` 数量、状态和 `content_id`。
5. 确认 `contents` 没有被误创建。
6. 更新总控状态、change-log、handoff-log。

## API 使用边界

- 新增计划：`POST /api/plans`
- 更新计划：`PATCH /api/plans/:id`
- 删除未绑定内容的计划：`DELETE /api/plans/:id`
- 查看计划：`GET /api/plans`

不要用以下接口处理单纯计划修改：

- `POST /api/contents`
- `POST /api/contents/drafts`
- `PATCH /api/contents/:id`

## 删除旧计划规则

当用户要求“只保留新计划”时：

- 删除旧 `plans` 记录。
- 若旧计划已绑定内容，不能静默删除，必须先让用户确认内容处理方式。
- 不删除已发布内容记录，除非用户明确要求。

## 验证清单

- `plans` 中只存在预期计划。
- 单纯计划修改后 `contents` 数量不增加。
- 新计划 `content_id` 应为 `NULL`。
- 新计划默认状态为 `待领取`，除非用户明确指定其他状态。
- 没有写入 `publishedAt` 或平台指标。
