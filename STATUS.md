# 项目状态

> 最近更新：2026-07-22

## 当前阶段

Phase 1：第一卷章节设计 —— 待开始。

## Phase Status

Frozen

## Freeze Date

2026-07-22

Phase 0 已正式完成并冻结。除重大设计缺陷外，不再修改工程结构。

## 当前状态

- Phase 0 工程骨架、治理与工程完善已完成并冻结。
- Phase 0.1 AI 文档工程治理升级已完成。
- Phase 0.2 工程完善已完成。
- Prompt 分类、索引、执行历史、项目上下文和 ADR 已建立。
- 第一卷 Prompt 已纳入分层目录。
- `docs/01` 至 `docs/08` 尚未生成业务正文。
- 当前工作区变更尚未执行 Git commit 或 Git push。

## 冻结规则

- 允许新增 Prompt。
- 允许新增业务内容。
- 允许修复 Bug。
- 禁止随意调整目录、治理体系或 Prompt 生命周期。
- 如确需修改冻结结构，必须先新增 ADR 并取得用户明确授权。

## 当前任务

第一卷《孕晚期准备（32周～生产）》章节骨架设计。

## 下一步

执行 `prompts/volume-01/01-outline/Codex_Prompt_第一卷章节骨架_V1.0.md`。

## 快速入口

- [项目上下文](docs/00-project/project-context.md)
- [项目路线图](docs/00-project/roadmap.md)
- [Prompt 管理说明](prompts/README.md)
- [Prompt 索引](prompts/prompt-index.md)
- [Prompt 执行历史](docs/00-project/prompt-history.md)

## 当前约束

- 不重新初始化项目。
- 未经确认不批量生成业务正文。
- 医学内容写入前必须完成来源核验。
- PDF、Word 仅作为后续发布产物。
