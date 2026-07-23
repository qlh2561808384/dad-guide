# Prompt 管理

## 目录作用

`prompts/` 集中保存项目使用的 AI Prompt，用于设计、登记、执行和追踪文档工程任务。

本目录只存放 Prompt，不存放最终文档、图片、PDF 或 Word 文件。最终 Markdown 成果存放在 `docs/`，治理记录存放在 `docs/00-project/`，发布产物存放在 `release/`。

## Prompt 与结果分离

- `prompts/`：说明 AI 应执行什么任务。
- `docs/`：保存 Prompt 执行后形成的最终 Markdown 结果。
- `docs/00-project/`：保存项目上下文、执行历史和设计决策。
- `assets/`：保存图片、图表和流程图源文件。
- `release/`：保存后续生成的发布文件。

Prompt 文件不得与生成结果混放。修改 Prompt 不等于修改结果；重新执行 Prompt 前必须确认影响范围。

## Prompt 生命周期

```text
设计 Prompt
→ 登记 prompt-index.md
→ 执行 Prompt
→ 生成或修改 docs 文件
→ 人工 Review
→ 更新 prompt-history.md
→ Git Commit
→ 更新 project-context.md
```

本生命周期描述完整协作流程。具体任务明确禁止提交时，只更新历史中的 Git Commit 状态，不执行提交。

### 状态生命周期

```text
Draft → Testing → Approved
                 ├→ Archived
                 └→ Deprecated

Reserved（仅占用 PR 编号，无实际 Prompt 文件）
```

| Status | 含义 |
| --- | --- |
| Draft | 已有实际 Prompt 草案文件，正在设计且尚未进入试运行 |
| Testing | Prompt 正在执行、验证或等待执行结果 Review |
| Approved | Prompt 当前版本已确认可用 |
| Reserved | 仅保留 PR 编号，尚无实际 Prompt 文件；该编号不得复用 |
| Archived | 历史版本已归档，但对应 PR 仍有有效版本 |
| Deprecated | 对应 PR 已整体停止使用，不再作为任务入口 |

生命周期变化必须同步更新 `prompt-index.md`。Prompt 生命周期只说明 Prompt 是否可用；执行结果是否通过人工审核，单独记录在 `docs/00-project/prompt-history.md` 的 `Review 状态` 中。

## Prompt 分类

| 目录 | 分类 | 用途 |
| --- | --- | --- |
| `initialization/` | 初始化与治理 | 初始化工程、升级治理规则 |
| `volume-01/` 至 `volume-08/` | 分卷任务 | 设计章节、生成或修订对应分卷内容 |
| `release/` | 发布任务 | 设计和执行发布流程 |
| `archive/draft/` | 未通过旧稿 | 保存未成为正式执行版本的 Prompt |
| `archive/superseded/` | 被替代版本 | 保存已被新版本或新 Prompt 取代的 Prompt |
| `archive/obsolete/` | 停用历史 | 保存不再适用但仍需保留审计价值的 Prompt |

## Prompt 命名规范

### 文件命名

统一格式：

```text
PR-XXXX_<名称>_V<版本>.md
```

示例：

- `PR-001_项目初始化_V2.0.md`
- `PR-008_Phase0最终收尾_Freeze_V1.0.md`
- `PR-009_第一卷章节架构设计_V1.0.md`

`PR-XXXX` 是 Prompt 的唯一身份标识。文件名不使用工具名称前缀，也不使用独立的 Phase/Milestone 编排前缀；目录负责表达 Prompt 分类。

### 标题规范

Prompt 文档统一使用：

```markdown
# PR-XXXX：名称

Version：Vx.x
```

标题不包含文件扩展名，版本号单独登记在标题下一行。

### Prompt Index 单一数据源

`prompt-index.md` 是 Prompt 项目管理信息的唯一数据源（Single Source of Truth）。以下字段只在索引中维护，不写入文件名：

- Phase
- Milestone
- Volume
- Stage
- 文件路径

同一 Prompt 的重大范围变化提升主版本，兼容性调整提升次版本。旧版本不直接覆盖，应迁移至 `archive/` 并在索引中标记状态。

## 维护规则

1. 执行前先在 `prompt-index.md` 登记用途、输入、输出、依赖和状态。
2. 已创建实际草案文件时使用 `Draft`；仅占用编号、尚无实际文件时使用 `Reserved`；执行和结果 Review 期间使用 `Testing`，确认可用后使用 `Approved`。
3. 每次执行后更新 `docs/00-project/prompt-history.md`，记录具体文件路径。
4. 阶段切换或重大任务完成后更新 `docs/00-project/project-context.md`。
5. 不覆盖同名 Prompt；同名文件先比较内容，无法确认时保留原文件并报告。
6. 历史 Prompt 不直接删除，按原因迁移到 `archive/draft/`、`archive/superseded/` 或 `archive/obsolete/`，并更新索引状态。
7. Prompt 只修改任务授权范围内的文件，不重新初始化既有项目。
8. 修改 Prompt 身份、命名格式或索引职责前必须新增 ADR 并取得用户明确授权。
