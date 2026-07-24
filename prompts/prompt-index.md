# Prompt 索引

本文件是 Prompt 项目管理信息的唯一数据源（Single Source of Truth），统一维护 PR 编号、版本关系、Status、Phase、Milestone、Volume、Stage 和文件路径。实际执行结果与人工 Review 状态记录在 `docs/00-project/prompt-history.md`。

## Prompt 清单

| 编号 | Prompt 名称 | Current Version | Previous Version | Status | Phase | Milestone | Volume | Stage | 文件路径 | 作用 | 使用时机 | 输入 | 预期输出 | 预计输出文件数 | 依赖 | 创建人 | Review 人 | 最近执行时间 | 最近更新时间 | 备注 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| PR-001 | 家庭迎新生命操作手册初始化 | V2.0 | — | Approved | Phase 0 | — | 全项目 | Initialization | `initialization/PR-001_家庭迎新生命操作手册初始化_V2.0.md` | 初始化项目工程骨架 | 新项目首次初始化 | 项目背景与目录要求 | `README.md`、`docs/`、`templates/`、`assets/`、`release/` | 76 | 无 | 用户 | 用户 | 2026-07-22 | 2026-07-22 | 对应 EXEC-0001 |
| PR-002 | 已有项目增加AI文档工程治理 | V1.0 | — | Approved | Phase 0.1 | — | 全项目 | Governance | `initialization/PR-002_已有项目增加AI文档工程治理_V1.0.md` | 增加 Prompt 管理、执行历史、项目上下文和 ADR | 工程骨架完成后 | 现有项目结构与治理要求 | `prompts/`、治理文档、Agent 规则与 Prompt 迁移记录 | 21（含迁移） | PR-001 | 用户 | 待指定 | 2026-07-22 | 2026-07-22 | 对应 EXEC-0002；执行结果 Review 状态见 Prompt History |
| PR-003 | 第一卷章节骨架 | V1.0 | — | Deprecated | Phase 1 | Milestone 1 | Volume 01 | Outline | `archive/superseded/PR-003_第一卷章节骨架_V1.0.md` | 旧版第一卷章节骨架设计 | 已由 PR-009 取代 | 已确认的章节范围与命名规则 | 第一卷章节空模板及导航 | — | PR-007 | 用户 | 待指定 | — | 2026-07-22 | 未执行；已由 PR-009 V1.0 取代 |
| PR-004 | — | — | — | Reserved | Phase 2 | Milestone 1 | Volume 01 | Content | — | 根据已审核章节骨架逐章生成正文 | 第一卷章节架构审核后 | 已确认章节与核验来源 | 第一卷业务正文 | 待确认 | PR-009、PR-010 | 待定 | 待指定 | — | 2026-07-22 | 无 Prompt 文件、无执行记录，编号不得复用 |
| PR-005 | — | — | — | Reserved | Phase 5 | 跨里程碑 | 全卷 | Review | — | 审核医学内容的准确性与边界 | 业务正文完成后 | 待审核正文与权威来源 | 审核意见及修订内容 | 待确认 | 业务正文 | 待定 | 待指定 | — | 2026-07-22 | 无 Prompt 文件、无执行记录，编号不得复用 |
| PR-006 | — | — | — | Reserved | Phase 5 | 跨里程碑 | 全卷 | Release | — | 生成发布版本 | 内容审核通过后 | 已审核 Markdown | PDF、Word 发布文件 | 待确认 | 内容审核 | 待定 | 待指定 | — | 2026-07-22 | 无 Prompt 文件、无执行记录，编号不得复用；本轮不执行发布 |
| PR-007 | 工程完善 | V1.0 | — | Approved | Phase 0.2 | — | 全项目 | Governance | `initialization/PR-007_工程完善_V1.0.md` | 完善工程入口、Prompt 分层和治理元数据 | Phase 0.1 完成后 | 现有治理结构与第一卷 Prompt | `STATUS.md`、路线图、术语表、Prompt 分层和扩展元数据 | 18（含迁移与删除） | PR-002 | 用户 | 待指定 | 2026-07-22 | 2026-07-22 | 对应 EXEC-0003；执行结果 Review 状态见 Prompt History |
| PR-008 | Phase0最终收尾 Freeze | V1.0 | — | Approved | Phase 0 | — | 全项目 | Freeze | `initialization/PR-008_Phase0最终收尾_Freeze_V1.0.md` | 完成 Phase 0 最终收尾并冻结工程结构 | Phase 0.2 完成后 | 已完成的工程治理结构和 release 空目录 | `CHANGELOG.md`、版本化 release、冻结状态和治理规则 | 15（含迁移） | PR-007 | 用户 | 待指定 | 2026-07-22 | 2026-07-22 | 对应 EXEC-0004；执行结果 Review 状态见 Prompt History |
| PR-009 | 第一卷章节架构设计 | V1.0 | V0.9 | Approved | Phase 1 | Milestone 1 | Volume 01 | Outline | `volume-01/01-outline/PR-009_第一卷章节架构设计_V1.0.md` | 建立第一卷七章架构并统一章节模板 | Phase 0 冻结并取得 ADR-005 授权后 | 已冻结工程规范与确认后的七章方案 | 第一卷 README 和七个章节空模板 | 27（含迁移） | PR-008、ADR-005 | 用户 | 用户 | 2026-07-22 | 2026-07-22 | V0.9 位于 `archive/draft/`；对应 EXEC-0006、EXEC-0008 |
| PR-010 | 第一卷章节架构整理与工程清理 | V1.1 | V1.0 | Approved | Phase 1 | Milestone 1 | Volume 01 | Outline | `volume-01/01-outline/PR-010_第一卷章节架构整理与工程清理_V1.1.md` | 整理 Prompt 命名、归档、版本关系和状态模型 | 第一卷章节架构完成、正文规范设计前 | ADR-006 与现有 Prompt 治理信息 | Prompt 命名修正、archive 分类、索引与阶段状态校正 | 详见 EXEC-0008 | PR-009、ADR-006 | 用户 | 用户 | 2026-07-22 | 2026-07-22 | V1.0 位于 `archive/superseded/`；对应 EXEC-0007、EXEC-0008 |
| PR-011 | Content Production Framework | V1.0 | — | Approved | Phase 1 | 全项目内容生产准备 | 全项目 | Framework | `framework/PR-011_Content_Production_Framework_V1.0.md` | 建立八卷统一内容生产、写作、医学引用、风格、Review 和发布规范 | PR-012～PR-090 内容生产开始前 | PR-001～PR-010 治理成果与已确认 Framework 设计 | `docs/00-project/content-production-framework.md` | 1 | PR-010 | 用户 | 用户 | 2026-07-23 | 2026-07-23 | 项目最后一个架构类 Prompt；对应 EXEC-0009 |
| PR-012 | 第一卷第一章《孕晚期概览》正文生成 | V1.0 | — | Approved | Phase 1 | 第一卷内容生产 | Volume 01 | Content | `volume-01/02-content/PR-012_第一卷第一章_孕晚期概览_V1.0.md` | 生成第一卷第一章正文，建立孕晚期家庭行动入口 | 第一卷内容生产开始时 | PR-011、第一卷章节骨架、已核验医学来源和用户确认的家庭时间信息 | `docs/01-late-pregnancy/third-trimester-overview.md` | 1 | PR-011 | 用户 | 用户 | 2026-07-23 | 2026-07-23 | 最高风险等级 L3；正文已由用户人工 Review；对应 EXEC-0010 |
| PR-013 | 第一卷第二章《产检管理》正文生成 | V1.0 | — | Approved | Phase 1 | 第一卷内容生产 | Volume 01 | Content | `volume-01/02-content/PR-013_第一卷第二章_产检管理_V1.0.md` | 生成第一卷第二章正文，建立产检信息与行动闭环 | 第一卷第二章内容生产时 | PR-011、第一卷章节骨架、已核验医学来源和用户确认的家庭预约信息 | `docs/01-late-pregnancy/prenatal-checkup-management.md` | 1 | PR-011、PR-012 | 用户 | 用户 | 2026-07-23 | 2026-07-23 | 最高风险等级 L3；正文已由用户人工 Review；对应 EXEC-0011 |

## 版本关系

| PR 编号 | Current Version | Previous Version | Previous Version 路径 | Previous Version Status |
| --- | --- | --- | --- | --- |
| PR-009 | V1.0 | V0.9 | `archive/draft/PR-009_第一卷章节架构设计_V0.9.md` | Archived |
| PR-010 | V1.1 | V1.0 | `archive/superseded/PR-010_第一卷章节架构整理与工程清理_V1.0.md` | Archived |

未列出的 PR 当前没有已登记的历史版本。

## Status 定义

- `Draft`：已有实际 Prompt 草案文件，正在设计且尚未进入试运行。
- `Testing`：Prompt 正在执行、验证或等待执行结果 Review。
- `Approved`：Prompt 当前版本已确认可用。
- `Reserved`：仅保留 PR 编号，尚无实际 Prompt 文件；该编号不得复用。
- `Archived`：历史版本已归档，但对应 PR 仍有有效版本。
- `Deprecated`：对应 PR 已整体停止使用，不再作为任务入口。

`Status` 不表示执行结果是否通过人工审核；执行结果的 `Review 状态` 只在 Prompt History 中维护。

## 索引字段职责

- `编号` 是 Prompt 的唯一身份标识。
- `Current Version`、`Previous Version` 和 `Status` 表达当前版本、直接前序版本和 Prompt 生命周期。
- `Phase`、`Milestone`、`Volume`、`Stage` 和 `文件路径` 只在本索引维护，不编码为独立文件名前缀。
- 目录负责分类，文件名负责身份和版本，执行历史负责记录实际影响。

## 维护规则

1. 新增或迁移 Prompt 时同步更新本索引。
2. Prompt 版本变化时更新版本关系和备注，不覆盖历史执行记录。
3. Prompt 执行后在 `docs/00-project/prompt-history.md` 中追加实际文件映射和 Review 状态。
4. 仅占用编号且文件尚未创建时必须使用 `Reserved`，`Prompt 名称`、`Current Version`、`Previous Version` 和 `文件路径` 均登记为 `—`；不得以 `Draft` 或虚构路径代替。
5. 历史 Prompt 不直接删除，按原因迁移到 `archive/draft/`、`archive/superseded/` 或 `archive/obsolete/`。
6. 不在 Prompt 文件名中重复维护 Phase、Milestone、Volume 或 Stage。
7. 修改索引字段职责、状态模型或命名规范前必须新增 ADR 并取得用户明确授权。
