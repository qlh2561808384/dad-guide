# 项目状态

> 最近更新：2026-07-22

## Phase

Phase 1

## Milestone

第一卷内容生产准备

## Status

Ready for Content Specification

## Completed

- PR-009：第一卷章节架构设计
- PR-010：第一卷章节架构整理与工程清理

## Current

第一卷章节架构、Prompt 命名、归档和状态模型已完成并通过审核。

## Next

PR-011 第一卷正文生成规范设计

## Phase 0 Engineering Status

Frozen

## Freeze Date

2026-07-22

Phase 0 已正式完成并冻结。除重大设计缺陷外，不再修改工程结构。

## 当前状态

- Phase 0 工程骨架、治理与工程完善已完成并冻结。
- Phase 0.1 AI 文档工程治理升级已完成。
- Phase 0.2 工程完善已完成。
- Prompt 命名规范升级已完成，并通过 ADR-005 记录冻结后的治理变更授权。
- Prompt 归档分类与状态模型升级已完成，并通过 ADR-006 记录授权。
- Prompt 分类、索引、执行历史、项目上下文和 ADR 已建立。
- 第一卷 Prompt 已纳入分层目录并统一使用 PR 编号命名。
- 第一卷历史 Prompt 已按 draft、superseded、obsolete 分类管理。
- 第一卷七个章节空模板及模块导航已创建，尚未生成业务正文。
- PR-009 与 PR-010 已完成并通过审核，第一卷工程治理停止扩展。
- `docs/02` 至 `docs/08` 未修改业务内容。
- 当前工作区变更尚未执行 Git commit 或 Git push。

## 冻结规则

- 允许新增 Prompt。
- 允许新增业务内容。
- 允许修复 Bug。
- 禁止随意调整目录、治理体系或 Prompt 生命周期。
- 如确需修改冻结结构，必须先新增 ADR 并取得用户明确授权。

## 当前任务

准备 PR-011：第一卷正文生成规范设计。

## 下一步

执行 PR-011：第一卷正文生成规范设计，并在生成正文前确认医学来源与核验方案。

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
