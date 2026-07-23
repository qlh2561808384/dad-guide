# 已归档 Prompt

## 目录用途

本目录保存已废弃、被替代或仅供审计使用的 Prompt。归档文件不得作为当前任务入口。

## 分类目录

| 目录 | 用途 | Prompt Status |
| --- | --- | --- |
| `draft/` | 未通过或未成为正式执行版本的旧稿 | Archived |
| `superseded/` | 已被新版本或新 Prompt 明确取代的版本 | Archived 或 Deprecated |
| `obsolete/` | 不再适用但仍需保留审计价值的 Prompt | Deprecated |

## 归档规则

1. 归档前在 `../prompt-index.md` 更新 `Current Version`、`Previous Version` 和 `Status`。
2. 按当前 `PR-XXXX_<名称>_V<版本>.md` 规范保留编号和版本，避免覆盖历史版本。
3. 在索引备注中记录替代 Prompt 或归档原因。
4. 历史执行记录继续保留在 `../../docs/00-project/prompt-history.md`。

## 当前归档

| Prompt | 状态 | 替代版本 |
| --- | --- | --- |
| [PR-003 第一卷章节骨架 V1.0](superseded/PR-003_第一卷章节骨架_V1.0.md) | Deprecated | PR-009 V1.0 |
| [PR-009 第一卷章节架构设计 V0.9](draft/PR-009_第一卷章节架构设计_V0.9.md) | Archived | PR-009 V1.0 |
| [PR-010 第一卷章节架构整理与工程清理 V1.0](superseded/PR-010_第一卷章节架构整理与工程清理_V1.0.md) | Archived | PR-010 V1.1 |
