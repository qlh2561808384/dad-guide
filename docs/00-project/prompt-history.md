# Prompt 执行历史（prompt-history.md）

> 本文件用于记录每一次 AI Prompt 对仓库产生的实际影响，实现 **Prompt →
> 文件** 的可追溯关系。

## 使用原则

-   每执行一个 Prompt，新增一条记录。
-   必须记录**具体文件**，不能只写数量。
-   一个 Prompt 可对应多个文件。
-   一个文件可在后续被多个 Prompt 修改，每次都追加记录。
-   与 Git Commit 配合使用，形成完整审计链。

## 执行摘要表

| 执行编号 | 日期 | Agent | AI 工具 | AI 模型 | Prompt 文件 | Prompt 版本 | 执行动作 | 执行耗时 | Git Commit | Review 人 | Review 状态 | 备注 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| EXEC-0001 | 2026-07-22 | Codex | 未记录 | 未记录 | `PR-001_家庭迎新生命操作手册初始化_V2.0.md` | V2.0 | 初始化项目工程骨架 | 未精确记录 | 未执行 | 用户 | 已审核 | 原记录编号为 P-0001；路径由 EXEC-0006 规范化 |
| EXEC-0002 | 2026-07-22 | Codex | 未记录 | 未记录 | `PR-002_已有项目增加AI文档工程治理_V1.0.md` | V1.0 | 增量增加 AI 文档工程治理 | 未精确记录 | 未执行 | 待指定 | 待审核 | 不涉及业务正文；路径由 EXEC-0006 规范化 |
| EXEC-0003 | 2026-07-22 | Codex | Codex | GPT-5 | `PR-007_工程完善_V1.0.md` | V1.0 | 完善工程入口、Prompt 分层和治理元数据 | 未精确记录 | 未执行 | 待指定 | 待审核 | 不涉及业务正文；路径由 EXEC-0006 规范化 |
| EXEC-0004 | 2026-07-22 | Codex | Codex | GPT-5 | `PR-008_Phase0最终收尾_Freeze_V1.0.md` | V1.0 | 完成 Phase 0 最终收尾并冻结工程结构 | 未精确记录 | 未执行 | 待指定 | 待审核 | 不涉及业务正文；路径由 EXEC-0006 规范化 |
| EXEC-0006 | 2026-07-22 | Codex | Codex | GPT-5 | `PR-009_第一卷章节架构设计_V1.0.md` | V1.0 | 统一 Prompt 命名并创建第一卷章节架构 | 未精确记录 | 未执行 | 待指定 | 待审核 | EXEC-0005 未使用；不生成正文；文件最终名称由 EXEC-0008 修正 |
| EXEC-0007 | 2026-07-22 | Codex | Codex | GPT-5 | `PR-010_第一卷章节架构整理与工程清理_V1.0.md` | V1.0 | 整理 Prompt 归档、版本关系和状态模型 | 未精确记录 | 未执行 | 待指定 | 待审核 | 不修改第一卷章节；不生成正文 |
| EXEC-0008 | 2026-07-22 | Codex | Codex | GPT-5 | `PR-010_第一卷章节架构整理与工程清理_V1.1.md` | V1.1 | 修正第一卷 Prompt 命名、归档与阶段状态 | 未精确记录 | 未执行 | 用户 | 已审核 | 第一卷工程治理收尾；下一步进入 PR-011 |
| EXEC-0009 | 2026-07-23 | Codex | Codex | GPT-5 | `PR-011_Content_Production_Framework_V1.0.md` | V1.0 | 建立八卷统一 Content Production Framework | 未精确记录 | 未执行 | 用户 | 已审核 | 项目最后一个架构类 Prompt；不生成业务正文 |

------------------------------------------------------------------------

## Prompt 执行记录

  -----------------------------------------------------------------------------------------------------------------------------------------------------
  编号     日期         Agent   Prompt 文件                                       Prompt 版本 操作类型         Git Commit   Review   备注
  -------- ------------ ------- ------------------------------------------------- ----------- ---------------- ------------ -------- ------------------
  P-0001   2026-07-22   Codex   PR-001_家庭迎新生命操作手册初始化_V2.0.md   V2.0        初始化工程骨架   （待填写）   已审核   创建项目基础结构

  -----------------------------------------------------------------------------------------------------------------------------------------------------

### P-0001 文件映射

#### 新增文件

  --------------------------------------------------------------------------------------
  序号            文件路径                               操作            说明
  --------------- -------------------------------------- --------------- ---------------
  1               README.md                              Create          项目入口

  2               docs/00-project/project-overview.md    Create          项目说明

  3               docs/00-project/version-history.md     Create          版本历史

  4               docs/00-project/writing-standard.md    Create          写作规范

  5               docs/00-project/module-overview.md     Create          模块说明

  6               docs/01-late-pregnancy/README.md       Create          模块入口

  7               docs/02-labor-day/README.md            Create          模块入口

  8               docs/03-hospital-stay/README.md        Create          模块入口

  9               docs/04-mother-recovery/README.md      Create          模块入口

  10              docs/05-newborn-care/README.md         Create          模块入口

  11              docs/06-dad-guide/README.md            Create          模块入口

  12              docs/07-postpartum-42-days/README.md   Create          模块入口

  13              docs/08-first-year/README.md           Create          模块入口

  14              docs/07-postpartum-42-days/day-01.md   Create          42个逐日模板
                  \~ day-42.md

  15              docs/08-first-year/month-01.md \~      Create          12个逐月模板
                  month-12.md

  16              templates/daily-checklist.md           Create          模板

  17              templates/hospital-record.md           Create          模板

  18              templates/mother-record.md             Create          模板

  19              templates/baby-record.md               Create          模板

  20              assets/\*\*/.gitkeep                   Create          保留空目录

  21              release/\*\*/.gitkeep                  Create          保留空目录
  --------------------------------------------------------------------------------------

#### 修改文件

  文件路径   操作   说明
  ---------- ------ ------
  无         \-     \-

#### 删除文件

  文件路径   操作   说明
  ---------- ------ ------
  无         \-     \-

------------------------------------------------------------------------

## 推荐规范

每个 Prompt 都保持以下结构：

1.  Prompt 基本信息（表格）
2.  文件映射（新增/修改/删除）
3.  Git Commit
4.  Review 结果
5.  后续影响
6.  AI 工具、AI 模型与执行耗时
7.  Review 人与 Review 状态

> 建议始终采用**Markdown
> 表格**，而不是纯文字罗列。表格更适合排序、搜索、Diff、导出
> Excel，也方便 AI 自动维护。

---

## EXEC-0002

### Prompt

`prompts/initialization/PR-002_已有项目增加AI文档工程治理_V1.0.md`

### 新增文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| 1 | `docs/00-project/decision-records/ADR-003-prompt-result-separation.md` | Create | 记录 Prompt 与结果分离决策 |
| 2 | `docs/00-project/decision-records/ADR-004-project-context-recovery.md` | Create | 记录项目上下文恢复决策 |
| 3 | `prompts/volume-01/.gitkeep` | Create | 保留第一卷 Prompt 空目录 |
| 4 | `prompts/volume-02/.gitkeep` | Create | 保留第二卷 Prompt 空目录 |
| 5 | `prompts/volume-03/.gitkeep` | Create | 保留第三卷 Prompt 空目录 |
| 6 | `prompts/volume-04/.gitkeep` | Create | 保留第四卷 Prompt 空目录 |
| 7 | `prompts/volume-05/.gitkeep` | Create | 保留第五卷 Prompt 空目录 |
| 8 | `prompts/volume-06/.gitkeep` | Create | 保留第六卷 Prompt 空目录 |
| 9 | `prompts/volume-07/.gitkeep` | Create | 保留第七卷 Prompt 空目录 |
| 10 | `prompts/volume-08/.gitkeep` | Create | 保留第八卷 Prompt 空目录 |
| 11 | `prompts/release/.gitkeep` | Create | 保留发布 Prompt 空目录 |
| 12 | `prompts/archive/.gitkeep` | Create | 保留归档 Prompt 空目录 |

### 修改文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| 1 | `AGENTS.md` | Update | 增加执行前阅读、Prompt 分离、执行记录和阶段维护规则 |
| 2 | `CLAUDE.md` | Update | 增加上下文恢复、修改范围和任务闭环规则 |
| 3 | `docs/00-project/project-context.md` | Update | 更新当前阶段、当前任务、下一步和恢复顺序 |
| 4 | `docs/00-project/prompt-history.md` | Update | 追加 EXEC-0002 执行摘要与具体文件映射 |
| 5 | `prompts/README.md` | Update | 补充 Prompt 生命周期、分类、命名与维护规则 |
| 6 | `prompts/prompt-index.md` | Move + Update | 迁移旧索引并按统一表头登记 PR-001 至 PR-006 |

### 删除文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| — | 无 | — | 本次没有独立删除文件；迁移后的原路径见下表 |

### 迁移文件

| 序号 | 原路径 | 新路径 | 操作 | 说明 |
| --- | --- | --- | --- | --- |
| 1 | 历史初始化 Prompt 路径 | `prompts/initialization/PR-001_家庭迎新生命操作手册初始化_V2.0.md` | Move | 初始化 Prompt 归入初始化分类；最终路径由 EXEC-0006 规范化 |
| 2 | 历史治理 Prompt 路径 | `prompts/initialization/PR-002_已有项目增加AI文档工程治理_V1.0.md` | Move | 本次治理 Prompt 归入初始化分类；最终路径由 EXEC-0006 规范化 |
| 3 | `docs/00-project/prompt-index.md` | `prompts/prompt-index.md` | Move + Update | 删除旧位置并将索引迁入 Prompt 管理目录 |

### Git Commit

未执行。当前 Prompt 明确禁止执行 Git commit 和 Git push。

### Review 状态

待人工审核。

### 备注

- 未修改 `docs/01-late-pregnancy/` 至 `docs/08-first-year/` 的业务文件。
- 未修改 `templates/` 下的模板。
- 未生成孕期、生产、月子、育儿正文或发布文件。

---

## EXEC-0003

### Prompt

`prompts/initialization/PR-007_工程完善_V1.0.md`

### 执行元数据

| 字段 | 值 |
| --- | --- |
| Agent | Codex |
| AI 工具 | Codex |
| AI 模型 | GPT-5 |
| 执行耗时 | 未精确记录 |
| Review 人 | 待指定 |
| Review 状态 | 待审核 |

### 新增文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| 1 | `STATUS.md` | Create | 提供根目录当前状态入口 |
| 2 | `docs/00-project/glossary.md` | Create | 建立术语登记与审核模板 |
| 3 | `docs/00-project/roadmap.md` | Create | 记录 Phase 路线图与阶段出口 |
| 4 | `prompts/initialization/README.md` | Create | 说明初始化和工程治理 Prompt 的范围 |
| 5 | `prompts/volume-01/README.md` | Create | 说明第一卷 Prompt 分层与执行顺序 |
| 6 | `prompts/release/README.md` | Create | 说明项目发布 Prompt 的范围 |
| 7 | `prompts/archive/README.md` | Create | 说明 Prompt 归档规则 |
| 8 | `prompts/volume-01/02-content/.gitkeep` | Create | 保留第一卷内容 Prompt 空目录 |
| 9 | `prompts/volume-01/03-review/.gitkeep` | Create | 保留第一卷审核 Prompt 空目录 |
| 10 | `prompts/volume-01/04-release/.gitkeep` | Create | 保留第一卷发布 Prompt 空目录 |

### 修改文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| 1 | `prompts/README.md` | Update | 增加 Draft、Testing、Approved、Archived 生命周期 |
| 2 | `prompts/prompt-index.md` | Update | 增加输出数量、创建人、Review 人和时间元数据 |
| 3 | `docs/00-project/prompt-history.md` | Update | 扩展执行元数据并追加 EXEC-0003 |
| 4 | `docs/00-project/project-context.md` | Update | 将当前阶段更新为 Phase 0.2 已完成 |

### 删除文件与目录

| 序号 | 文件或目录路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| 1 | `prompts/volume-01/.gitkeep` | Delete | 第一卷目录已包含 README 和分层子目录 |
| 2 | `prompts/release/.gitkeep` | Delete | 发布 Prompt 目录已包含 README |
| 3 | `prompts/archive/.gitkeep` | Delete | 归档 Prompt 目录已包含 README |
| 4 | `doc/prompt/` | Remove directory | Prompt 迁移后删除空目录 |
| 5 | `doc/` | Remove directory | 历史 Prompt 根目录清理完成 |

### 迁移文件

| 序号 | 原路径 | 新路径 | 操作 | 说明 |
| --- | --- | --- | --- | --- |
| 1 | `doc/prompt/第一卷《孕晚期准备（32周～生产）》章节骨架设计 V1.0.md` | `prompts/archive/PR-003_第一卷章节骨架_V1.0.md` | Move + Rename | 迁入第一卷骨架层后由 EXEC-0006 归档 |

### Git Commit

未执行。当前 Prompt 明确禁止执行 Git commit 和 Git push。

### Review 状态

待人工审核。

### 备注

- 未修改 `docs/01-late-pregnancy/` 至 `docs/08-first-year/` 的业务文件。
- 未修改 `templates/` 下的模板正文。
- 未生成医学内容、PDF 或 Word。

---

## EXEC-0004

### Prompt

`prompts/initialization/PR-008_Phase0最终收尾_Freeze_V1.0.md`

### 执行元数据

| 字段 | 值 |
| --- | --- |
| Agent | Codex |
| AI 工具 | Codex |
| AI 模型 | GPT-5 |
| 执行耗时 | 未精确记录 |
| Review 人 | 待指定 |
| Review 状态 | 待审核 |

### 新增文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| 1 | `CHANGELOG.md` | Create | 记录 v0.1.0-engineering 及后续版本占位 |
| 2 | `release/README.md` | Create | 说明 latest 与历史版本目录规则 |
| 3 | `release/v1.0.0/pdf/.gitkeep` | Create | 保留 v1.0.0 PDF 空目录 |
| 4 | `release/v1.0.0/docx/.gitkeep` | Create | 保留 v1.0.0 DOCX 空目录 |
| 5 | `release/latest/.gitkeep` | Create | 保留最新发布版空目录 |

### 修改文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| 1 | `STATUS.md` | Update | 将 Phase Status 更新为 Frozen 并切换到 Phase 1 待开始 |
| 2 | `docs/00-project/project-context.md` | Update | 增加工程冻结声明和允许、禁止事项 |
| 3 | `docs/00-project/roadmap.md` | Update | 标记 Phase 0 Completed、Phase 1 Next 并增加八个里程碑 |
| 4 | `prompts/initialization/README.md` | Update | 登记 Phase 0 Freeze Prompt |
| 5 | `prompts/prompt-index.md` | Update | 新增 PR-008 并同步编号后的 initialization Prompt 路径 |
| 6 | `docs/00-project/prompt-history.md` | Update | 追加 EXEC-0004 及具体文件映射 |
| 7 | `AGENTS.md` | Update | 增加 Frozen 状态下的工程结构保护规则 |
| 8 | `CLAUDE.md` | Update | 增加 Frozen 状态下的工程结构保护规则 |

### 删除文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| — | 无 | — | 本次没有独立删除文件；旧 release 占位文件采用无损迁移 |

### 迁移文件

| 序号 | 原路径 | 新路径 | 操作 | 说明 |
| --- | --- | --- | --- | --- |
| 1 | `release/pdf/.gitkeep` | `release/v0.1.0-engineering/pdf/.gitkeep` | Move | 将原 PDF 占位目录纳入工程冻结版本 |
| 2 | `release/docx/.gitkeep` | `release/v0.1.0-engineering/docx/.gitkeep` | Move | 将原 DOCX 占位目录纳入工程冻结版本 |

### Git Commit

未执行。当前 Prompt 明确禁止执行 Git commit 和 Git push。

### Review 状态

待人工审核。

### 备注

- 未修改 `docs/01-late-pregnancy/` 至 `docs/08-first-year/` 的业务文件。
- 未修改 `templates/` 下的模板正文。
- 未生成医学内容、PDF 或 Word。
- Phase 0 工程结构已进入 Frozen 状态。

---

## EXEC-0006

### Prompt

`prompts/volume-01/01-outline/PR-009_第一卷章节架构设计_V1.0.md`

### 执行元数据

| 字段 | 值 |
| --- | --- |
| Agent | Codex |
| AI 工具 | Codex |
| AI 模型 | GPT-5 |
| 执行耗时 | 未精确记录 |
| Review 人 | 待指定 |
| Review 状态 | 待审核 |

EXEC-0005 未使用。本次按 PR-009 的明确要求登记为 EXEC-0006，不补造不存在的执行记录。

### 新增文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| 1 | `docs/00-project/decision-records/ADR-005-prompt-naming-standard.md` | Create | 记录冻结后的 Prompt 命名治理升级及用户授权 |
| 2 | `docs/01-late-pregnancy/third-trimester-overview.md` | Create | 孕晚期概览空模板 |
| 3 | `docs/01-late-pregnancy/prenatal-checkup-management.md` | Create | 产检管理空模板 |
| 4 | `docs/01-late-pregnancy/hospital-preparation.md` | Create | 医院准备空模板 |
| 5 | `docs/01-late-pregnancy/hospital-bag.md` | Create | 待产包空模板 |
| 6 | `docs/01-late-pregnancy/father-skills-training.md` | Create | 爸爸能力训练空模板 |
| 7 | `docs/01-late-pregnancy/labor-signs-and-actions.md` | Create | 临产信号与行动空模板 |
| 8 | `docs/01-late-pregnancy/family-coordination-plan.md` | Create | 家庭协作计划空模板 |

### 修改文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| 1 | `AGENTS.md` | Update | 更新 Prompt 示例名称 |
| 2 | `CHANGELOG.md` | Update | 新增 v0.1.1-engineering 记录 |
| 3 | `STATUS.md` | Update | 将当前阶段切换为 Phase 1 架构待 Review |
| 4 | `docs/00-project/project-context.md` | Update | 更新当前阶段并冻结 Prompt 命名规范 |
| 5 | `docs/00-project/prompt-history.md` | Update | 规范化历史 Prompt 引用并追加 EXEC-0006 |
| 6 | `docs/00-project/roadmap.md` | Update | 标记 Phase 1 和 Milestone 1 进行中 |
| 7 | `docs/01-late-pregnancy/README.md` | Update | 增加七章导航、章节职责和跨卷边界 |
| 8 | `prompts/README.md` | Update | 增加 Prompt 命名、标题和单一数据源规范 |
| 9 | `prompts/archive/README.md` | Update | 登记 PR-003 与 PR-009 V0.9 归档状态 |
| 10 | `prompts/initialization/README.md` | Update | 更新初始化 Prompt 路径 |
| 11 | `prompts/prompt-index.md` | Update | 增加项目管理字段并登记 PR-009 |
| 12 | `prompts/volume-01/README.md` | Update | 更新第一卷当前 Prompt 和执行状态 |

### 迁移文件

| 序号 | 原路径 | 新路径 | 操作 | 说明 |
| --- | --- | --- | --- | --- |
| 1 | `prompts/initialization/1_Codex_Prompt_家庭迎新生命操作手册初始化_V2.0.md` | `prompts/initialization/PR-001_家庭迎新生命操作手册初始化_V2.0.md` | Move + Update | 统一文件名与标题 |
| 2 | `prompts/initialization/2_Codex_Prompt_已有项目增加AI文档工程治理_V1.0.md` | `prompts/initialization/PR-002_已有项目增加AI文档工程治理_V1.0.md` | Move + Update | 统一文件名、标题和旧示例 |
| 3 | `prompts/initialization/3_Codex_Prompt_Phase0.2_工程完善_V1.0.md` | `prompts/initialization/PR-007_工程完善_V1.0.md` | Move + Update | 统一文件名与标题 |
| 4 | `prompts/initialization/4_Codex_Prompt_Phase0_最终收尾_Freeze_V1.0.md` | `prompts/initialization/PR-008_Phase0最终收尾_Freeze_V1.0.md` | Move + Update | 统一文件名、标题和索引示例 |
| 5 | `prompts/volume-01/01-outline/Codex_Prompt_第一卷章节骨架_V1.0.md` | `prompts/archive/PR-003_第一卷章节骨架_V1.0.md` | Move + Update | 归档已被 PR-009 取代的旧骨架 Prompt |
| 6 | `prompts/volume-01/01-outline/Codex_Prompt_Phase1_M1_第一卷章节架构设计_V1.0.md` | `prompts/archive/PR-009_Phase1启动及第一卷章节架构设计_V0.9.md`（历史旧名称） | Move + Update | 将未登记旧稿规范为 V0.9 并归档；最终名称由 EXEC-0008 修正 |
| 7 | `prompts/initialization/PR-009_Phase1启动及第一卷章节架构设计_V1.0.md`（历史旧名称） | `prompts/volume-01/01-outline/PR-009_Phase1启动及第一卷章节架构设计_V1.0.md`（历史旧名称） | Move + Update | 将唯一执行版本迁入第一卷章节设计目录并规范标题；最终名称由 EXEC-0008 修正 |

### 删除文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| — | 无 | — | 没有独立删除文件；原路径变化均记录为迁移 |

### Git Commit

未执行。PR-009 明确禁止执行 Git commit 和 Git push。

### Review 状态

待人工审核。

### 备注

- 本轮只创建章节空模板，没有生成业务正文或医学建议。
- 未修改第二卷至第八卷、通用模板或发布产物。
- Phase 0 其他冻结结构保持不变。

---

## EXEC-0007

### Prompt

`prompts/archive/superseded/PR-010_第一卷章节架构整理与工程清理_V1.0.md`

### 执行元数据

| 字段 | 值 |
| --- | --- |
| Agent | Codex |
| AI 工具 | Codex |
| AI 模型 | GPT-5 |
| 执行耗时 | 未精确记录 |
| Review 人 | 待指定 |
| Review 状态 | 待审核 |

### 新增文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| 1 | `docs/00-project/decision-records/ADR-006-prompt-archive-and-status-model.md` | Create | 记录归档分类、状态模型和用户授权 |
| 2 | `prompts/archive/obsolete/.gitkeep` | Create | 保留暂无归档文件的 obsolete 目录 |

### 修改文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| 1 | `STATUS.md` | Update | 将 Phase 1、M1 状态校正为 Review，并登记下一步 |
| 2 | `docs/00-project/project-context.md` | Update | 更新当前阶段、归档分类、状态模型和下一步 |
| 3 | `docs/00-project/prompt-history.md` | Update | 追加 EXEC-0007 和具体文件映射 |
| 4 | `prompts/README.md` | Update | 统一 Prompt 生命周期并说明与执行结果 Review 的边界 |
| 5 | `prompts/archive/README.md` | Update | 增加 draft、superseded、obsolete 分类说明和导航 |
| 6 | `prompts/prompt-index.md` | Update | 增加 Current Version、Previous Version、Status 和 PR-010 |
| 7 | `prompts/volume-01/README.md` | Update | 更新当前 Prompt、归档路径和 Review 状态 |

### 移动文件

| 序号 | 原路径 | 新路径 | 操作 | 说明 |
| --- | --- | --- | --- | --- |
| 1 | `prompts/volume-01/01-outline/PR-010_Phase1_M1第一卷章节架构整理与工程清理_V1.0.md` | `prompts/volume-01/01-outline/PR-010_第一卷章节架构整理与工程清理_V1.0.md`（历史旧路径） | Move + Update | 去除独立 Phase/Milestone 编排前缀并规范标题；该版本由 EXEC-0008 归档 |
| 2 | `prompts/archive/PR-009_Phase1启动及第一卷章节架构设计_V0.9.md`（历史旧名称） | `prompts/archive/draft/PR-009_Phase1启动及第一卷章节架构设计_V0.9.md`（历史旧名称） | Move + Update | 将未通过旧稿归入 draft并标记 Archived；最终名称由 EXEC-0008 修正 |
| 3 | `prompts/archive/PR-003_第一卷章节骨架_V1.0.md` | `prompts/archive/superseded/PR-003_第一卷章节骨架_V1.0.md` | Move + Update | 将被替代 Prompt 归入 superseded，并标记 Deprecated |

### 删除文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| — | 无 | — | 没有独立删除文件；历史 Prompt 均保留并分类迁移 |

### 版本关系调整

| PR 编号 | Current Version | Previous Version | Status | 说明 |
| --- | --- | --- | --- | --- |
| PR-003 | V1.0 | — | Deprecated | 已由 PR-009 V1.0 取代 |
| PR-009 | V1.0 | V0.9 | Approved | V0.9 已归档为 Archived |
| PR-010 | V1.0 | — | Testing | 执行结果等待人工 Review |

### Git Commit

未执行。PR-010 明确禁止执行 Git commit 和 Git push。

### Review 状态

待人工审核。

### 备注

- 未修改 `docs/01-late-pregnancy/` 下任何文件。
- 未修改第二卷至第八卷或 `templates/`。
- 未生成医学内容、业务正文或发布文件。
- 旧命名文本仅保留在禁止规则、ADR 背景和迁移审计记录中，不作为有效文件名或入口。

---

## EXEC-0008

### Prompt

`prompts/volume-01/01-outline/PR-010_第一卷章节架构整理与工程清理_V1.1.md`

### 执行元数据

| 字段 | 值 |
| --- | --- |
| Agent | Codex |
| AI 工具 | Codex |
| AI 模型 | GPT-5 |
| 执行耗时 | 未精确记录 |
| Review 人 | 用户 |
| Review 状态 | 已审核 |

### 新增文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| — | 无 | — | PR-010 V1.1 为本次执行输入，执行前已位于正式目录 |

### 修改文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| 1 | `CHANGELOG.md` | Update | 将后续计划切换为 PR-011 正文生成规范设计 |
| 2 | `STATUS.md` | Update | 切换为 Ready for Content Specification |
| 3 | `docs/00-project/decision-records/ADR-006-prompt-archive-and-status-model.md` | Update | 增加 Reserved 并校正 PR-009、PR-010 版本关系 |
| 4 | `docs/00-project/project-context.md` | Update | 登记 PR-009、PR-010 审核完成和下一步 |
| 5 | `docs/00-project/prompt-history.md` | Update | 修正有效引用、标记历史旧名称并追加 EXEC-0008 |
| 6 | `docs/00-project/roadmap.md` | Update | 标记章节架构审核与工程清理完成 |
| 7 | `prompts/README.md` | Update | 增加 Reserved 定义并修正命名示例 |
| 8 | `prompts/archive/README.md` | Update | 更新 PR-009 V0.9 与 PR-010 V1.0 归档导航 |
| 9 | `prompts/prompt-index.md` | Update | 校正 PR-001 至 PR-010 状态与版本关系 |
| 10 | `prompts/volume-01/01-outline/PR-010_第一卷章节架构整理与工程清理_V1.1.md` | Update | 明确标注任务中用于迁移与检索的历史旧名称 |
| 11 | `prompts/volume-01/README.md` | Update | 更新第一卷当前 Prompt 和归档说明 |

### 移动文件

| 序号 | 原路径 | 新路径 | 操作 | 说明 |
| --- | --- | --- | --- | --- |
| 1 | `prompts/volume-01/01-outline/PR-009_Phase1启动及第一卷章节架构设计_V1.0.md`（历史旧名称） | `prompts/volume-01/01-outline/PR-009_第一卷章节架构设计_V1.0.md` | Move + Update | 修正正式版名称与标题 |
| 2 | `prompts/archive/draft/PR-009_Phase1启动及第一卷章节架构设计_V0.9.md`（历史旧名称） | `prompts/archive/draft/PR-009_第一卷章节架构设计_V0.9.md` | Move + Update | 修正草案名称与标题，保留历史版本 |
| 3 | `prompts/volume-01/01-outline/PR-010_第一卷章节架构整理与工程清理_V1.0.md`（历史旧路径） | `prompts/archive/superseded/PR-010_第一卷章节架构整理与工程清理_V1.0.md` | Move + Update | V1.0 被 V1.1 取代并归档 |
| 4 | `prompts/volume-01/01-outline/PR-010_第一卷章节架构整理与工程清理_V1.1.md` | `prompts/volume-01/01-outline/PR-010_第一卷章节架构整理与工程清理_V1.1.md` | Keep | 保留为唯一正式 PR-010 当前版本 |

### 删除文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| — | 无 | — | 没有删除 Prompt；旧版本均保留在 archive 中 |

### 版本与状态调整

| PR 编号 | Current Version | Previous Version | Status | 说明 |
| --- | --- | --- | --- | --- |
| PR-001 | V2.0 | — | Approved | 保持不变 |
| PR-002 | V1.0 | — | Approved | 保持不变 |
| PR-003 | V1.0 | — | Deprecated | 已由 PR-009 取代 |
| PR-004 | — | — | Reserved | 无实际 Prompt 文件、无执行记录 |
| PR-005 | — | — | Reserved | 无实际 Prompt 文件、无执行记录 |
| PR-006 | — | — | Reserved | 无实际 Prompt 文件、无执行记录 |
| PR-007 | V1.0 | — | Approved | 保持不变 |
| PR-008 | V1.0 | — | Approved | 保持不变 |
| PR-009 | V1.0 | V0.9 | Approved | V0.9 保留为 Archived |
| PR-010 | V1.1 | V1.0 | Approved | V1.0 保留为 Archived |

### Git Commit

未执行。PR-010 V1.1 明确禁止执行 Git commit 和 Git push。

### Review 状态

已由用户确认 A 方案并授权执行，PR-010 V1.1 按已审核收尾。

### 验收结果

| 检查项 | 结果 | 说明 |
| --- | --- | --- |
| Prompt 文件名 | 通过 | PR-009 V1.0/V0.9 使用新名称；PR-010 V1.1 为唯一正式版本，V1.0 位于 superseded |
| 历史名称引用 | 通过 | 当前有效入口已修正；旧名称仅见于已标记的迁移审计记录和本次 Prompt 的历史名称迁移说明 |
| Prompt 状态 | 通过 | PR-004～PR-006 为 Reserved；PR-009、PR-010 为 Approved |
| 内容保护哈希 | 通过 | `docs/01-late-pregnancy/` 至 `docs/08-first-year/` 与 `templates/` 共 73 个文件均与执行前一致 |
| 发布产物 | 通过 | 未生成 PDF 或 DOCX |
| Git 差异格式 | 通过 | `git diff --check` 与 `git diff --cached --check` 均通过 |
| Git HEAD | 通过 | 保持 `bc0e818e29e6e636f24a6cbf42e522fedadb7a3f` 不变 |
| Commit / Push | 未执行 | 按任务约束保留当前工作区 |

### 备注

- 未修改 `docs/01-late-pregnancy/` 至 `docs/08-first-year/` 的业务文件。
- 未修改 `templates/` 或 `release/`。
- 未生成任何业务正文、医学建议或发布产物。
- Phase 0 继续保持 Frozen；第一卷工程治理停止扩展。
- 下一步进入 PR-011：第一卷正文生成规范设计。

---

## EXEC-0009

### Prompt

`prompts/framework/PR-011_Content_Production_Framework_V1.0.md`

### 执行元数据

| 字段 | 值 |
| --- | --- |
| Agent | Codex |
| AI 工具 | Codex |
| AI 模型 | GPT-5 |
| 执行耗时 | 未精确记录 |
| Review 人 | 用户 |
| Review 状态 | 已审核 |

### 新增文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| 1 | `docs/00-project/content-production-framework.md` | Create | 合并建立 Content、Writing、Medical Reference、Style、Review 和 Release 六类项目级规范 |

### 修改文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| 1 | `prompts/prompt-index.md` | Update | 登记 PR-011 V1.0 为 Approved |
| 2 | `docs/00-project/prompt-history.md` | Update | 追加 EXEC-0009、文件映射和验收结果 |

### 移动文件

| 序号 | 原路径 | 新路径 | 操作 | 说明 |
| --- | --- | --- | --- | --- |
| — | 无 | 无 | — | 本次没有移动文件 |

### 删除文件

| 序号 | 文件路径 | 操作 | 说明 |
| --- | --- | --- | --- |
| — | 无 | — | 本次没有删除文件 |

### Framework 交付范围

- Content Flow、Review Flow、Release Flow 和 Volume Flow。
- 固定章节结构、爸爸行动项、妈妈注意事项、医学知识、SOP、Checklist、FAQ、记录、Mermaid、表格和风险提示规范。
- L0～L3 医学风险等级、来源分级、来源 ID、证据矩阵、冲突处理和医学免责声明。
- 面向第一次当爸爸的中国家庭的 Style Guide。
- 结构、医学、引用、Checklist、Mermaid、重复内容、AI 幻觉和可执行性 Review。
- 版本、CHANGELOG、STATUS、Release Note 和发布产物验收规范。
- 20 项包含具体版本、URL 和访问日期的中国及国际权威来源。
- PR-012～PR-090 可直接复用的任务卡和验收模板。

### 验收结果

| 检查项 | 结果 | 说明 |
| --- | --- | --- |
| Framework 完整性 | 通过 | 六类规范合并于一个文件，覆盖 32 个二级规范章节 |
| 医学来源 | 通过 | 20 项具体权威来源均包含版本、官方 URL 和访问日期 |
| 模板与流程 | 通过 | 四类 Flow、固定章节模板、证据矩阵、Review 和 Release 模板完整 |
| 占位与格式 | 通过 | 无未完成标记；模板变量均位于明确的复用模板中；Markdown 代码块闭合 |
| 保护范围 | 通过 | PR-001～PR-010、Roadmap、业务章节、`templates/` 和 `release/` 未被本轮修改 |
| 发布产物 | 通过 | 未生成 PDF 或 DOCX |
| Git 差异格式 | 通过 | `git diff --check` 与 `git diff --cached --check` 均通过 |
| Git HEAD | 通过 | 保持 `bc0e818e29e6e636f24a6cbf42e522fedadb7a3f` 不变 |
| Commit / Push | 未执行 | 按任务边界保留当前工作区 |

### Git Commit

未执行。PR-011 明确禁止执行 Git commit 和 Git push。

### Review 状态

用户已确认单文件合并方案、中国来源优先与具体版本 URL 方案，并完成 Framework 书面规范 Review。

### 备注

- 未修改 PR-001～PR-010 Prompt。
- 未修改 `docs/00-project/roadmap.md`。
- 未修改 `docs/01-late-pregnancy/` 至 `docs/08-first-year/`。
- 未修改 `templates/` 或 `release/`。
- 未生成业务正文、医学诊断、个体化治疗建议或发布产物。
- PR-011 是项目最后一个架构类 Prompt；PR-012～PR-090 进入内容生产。
