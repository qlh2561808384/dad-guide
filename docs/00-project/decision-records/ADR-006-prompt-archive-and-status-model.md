# ADR-006：Prompt 归档分类与状态模型

## ADR编号

ADR-006

## 日期

2026-07-22

## 状态

已确认

## 背景

ADR-005 已将 PR 编号确立为 Prompt 的唯一身份，并冻结文件命名和 Prompt Index 的单一数据源职责。PR-009 执行后，`prompts/archive/` 同时保存未通过旧稿和已被替代的 Prompt，但尚未区分归档原因；Prompt Index 也混合使用中文执行状态与 Prompt 生命周期状态，容易与执行结果的人工 Review 状态混淆。

Phase 0 冻结规则要求，修改 Prompt 治理结构或生命周期前必须新增 ADR 并取得用户明确授权。用户已于 2026-07-22 批准采用“保留审计记录的分类清理”方案。

## 决策内容

### 归档分类

`prompts/archive/` 使用以下结构：

```text
prompts/archive/
├── README.md
├── draft/
├── superseded/
└── obsolete/
```

- `draft/`：保存未通过或未成为正式执行版本的旧稿。
- `superseded/`：保存已被新版本或新 Prompt 明确取代的版本。
- `obsolete/`：保存不再适用、但仍需保留审计价值的 Prompt。

PR-009 V0.9 旧稿迁入 `draft/`；PR-003 V1.0 迁入 `superseded/`；`obsolete/` 暂无文件，以 `.gitkeep` 保留目录。

### 状态模型

`prompts/prompt-index.md` 的 `Status` 只记录 Prompt 生命周期：

- `Draft`：已存在实际 Prompt 草案文件，正在设计且尚未进入试运行。
- `Testing`：正在执行、验证或等待执行结果 Review。
- `Approved`：Prompt 当前版本已确认可用。
- `Reserved`：历史编号已占用或被预留，但当前不存在有效 Prompt 文件；该编号不得重新使用。
- `Archived`：历史版本已归档，但其当前 PR 仍有有效版本。
- `Deprecated`：该 PR 已整体停止使用，不再作为任务入口。

`docs/00-project/prompt-history.md` 的 `Review 状态` 继续单独记录执行结果是否通过人工审核。Prompt 生命周期与执行结果 Review 状态不得混用。

### 当前映射

- PR-001、PR-002、PR-007、PR-008、PR-009：`Approved`
- PR-003：`Deprecated`
- PR-004、PR-005、PR-006：`Reserved`，编号保留但不存在有效 Prompt 文件
- PR-009 V0.9：`Archived`
- PR-010 V1.0：`Archived`，由 V1.1 取代
- PR-010 V1.1：`Approved`

### 命名清理

PR-009 正式文件名为：

`PR-009_第一卷章节架构设计_V1.0.md`

PR-009 V0.9 历史草稿文件名为：

`PR-009_第一卷章节架构设计_V0.9.md`

PR-010 当前正式文件名为：

`PR-010_第一卷章节架构整理与工程清理_V1.1.md`

PR-010 V1.0 归档至 `archive/superseded/`。

有效 Prompt 文件不得使用工具名称前缀或独立的 Phase/Milestone 编排前缀。历史执行记录、迁移源路径、ADR 背景和禁止规则可以保留旧名称文本，以维持审计真实性；这些文本不属于有效文件名或有效入口。

## 选择原因

- 区分不同归档原因，便于判断历史文件是否仍可参考。
- 将 Prompt 生命周期与执行结果 Review 解耦，避免“已执行”等于“已批准”的误解。
- 保留历史文件和旧路径记录，不损害 Prompt 到文件的审计链。
- 以最小范围完成工程清理，不触碰第一卷章节内容或 Phase 0 其他冻结结构。

## 影响

- 新增三个 archive 分类目录，并更新相关导航和索引路径。
- Prompt Index 使用 `Current Version`、`Previous Version` 和 `Status` 表达版本关系与生命周期。
- 当前 PR-009 V1.0 与历史 V0.9 建立明确版本关系。
- 没有实际 Prompt 文件的 PR-004、PR-005、PR-006 使用 `Reserved`，不虚构版本或 Draft 文件。
- PR-010 V1.1 通过验收后成为 `Approved`，V1.0 作为 `Archived` 历史版本保留。
- `docs/01-late-pregnancy/`、`docs/02` 至 `docs/08`、`templates/` 和发布目录均不受影响。

## 相关文件

- `prompts/README.md`
- `prompts/prompt-index.md`
- `prompts/archive/README.md`
- `docs/00-project/prompt-history.md`
- `docs/00-project/project-context.md`
- `STATUS.md`

## 回退方式

如分类目录或状态模型导致工具兼容问题，可将归档文件移回 `prompts/archive/` 根目录，并恢复 ADR-006 前的 Prompt Index 表头与状态值。回退必须新增 ADR，说明受影响路径和审计记录处理方式。

## 备注

本 ADR 仅授权 PR-010 所述的 Prompt 归档分类、状态模型和自身命名清理，不授权修改业务章节、通用模板、发布目录或 Phase 0 其他治理结构。
