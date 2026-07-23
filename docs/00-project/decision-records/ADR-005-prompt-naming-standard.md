# ADR-005：统一 Prompt 命名规范

## ADR编号

ADR-005

## 日期

2026-07-22

## 状态

已确认

## 背景

Phase 0 冻结时，Prompt 文件同时存在数字前缀、`Codex_Prompt_` 前缀和 Phase/Milestone 前缀，文件身份依赖目录与名称组合判断，索引也未独立维护 Phase、Milestone、Volume 和 Stage。继续沿用会增加重命名、检索和审计成本。

Phase 0 的冻结规则要求治理体系调整必须先新增 ADR 并取得用户明确授权。用户已于 2026-07-22 确认本次一次性命名治理升级。

## 决策内容

- Prompt 文件统一命名为 `PR-XXXX_<名称>_V<版本>.md`。
- `PR-XXXX` 是 Prompt 的唯一身份标识。
- Prompt 标题统一使用 `# PR-XXXX：名称`，并在标题后单独记录 `Version：Vx.x`。
- 文件名不再使用工具名称前缀，也不使用独立的 Phase/Milestone 编排前缀。
- Phase、Milestone、Volume、Stage 和文件路径统一由 `prompts/prompt-index.md` 维护。
- 目录继续承担初始化、分卷、审核、发布和归档等分类职责。
- PR-003 旧章节骨架和 PR-009 V0.9 旧稿转入归档；PR-009 V1.0 是本轮唯一执行版本。

## 选择原因

- 通过 PR 编号稳定关联 Prompt、执行历史与输出文件。
- 避免工具名称、项目阶段或目录调整导致 Prompt 身份变化。
- 将项目管理元数据集中到单一数据源，降低多处维护产生的不一致。
- 保留旧稿和废弃 Prompt，确保历史可追溯。

## 影响

- 现有 Prompt 文件将一次性批量重命名，并更新仓库内有效引用。
- `prompts/prompt-index.md` 增加 Phase、Milestone、Volume、Stage 和文件路径字段。
- 本次迁移完成后，新的命名规范进入 Frozen 状态。
- 后续若再次修改 Prompt 身份、命名格式或索引职责，必须新增 ADR 并取得用户明确授权。
- 本决策不改变 Prompt 生命周期、业务模块目录、章节模板或发布目录结构。

## 相关文件

- `prompts/README.md`
- `prompts/prompt-index.md`
- `docs/00-project/project-context.md`
- `docs/00-project/prompt-history.md`
- `CHANGELOG.md`

## 回退方式

如新规范导致无法恢复的工具兼容问题，可依据 Git 历史恢复迁移前路径，并通过新的 ADR 说明回退原因、引用修复范围和后续命名方案。

## 备注

本 ADR 仅授权 PR-009 所述的一次性 Prompt 命名治理升级，不授权修改 Phase 0 的其他冻结结构。
