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
| EXEC-0001 | 2026-07-22 | Codex | 未记录 | 未记录 | `Codex_Prompt_家庭迎新生命操作手册初始化_V2.0.md` | V2.0 | 初始化项目工程骨架 | 未精确记录 | 未执行 | 用户 | 已审核 | 原记录编号为 P-0001 |
| EXEC-0002 | 2026-07-22 | Codex | 未记录 | 未记录 | `Codex_Prompt_已有项目增加AI文档工程治理_V1.0.md` | V1.0 | 增量增加 AI 文档工程治理 | 未精确记录 | 未执行 | 待指定 | 待审核 | 不涉及业务正文 |
| EXEC-0003 | 2026-07-22 | Codex | Codex | GPT-5 | `Codex_Prompt_Phase0.2_工程完善_V1.0.md` | V1.0 | 完善工程入口、Prompt 分层和治理元数据 | 未精确记录 | 未执行 | 待指定 | 待审核 | 不涉及业务正文 |
| EXEC-0004 | 2026-07-22 | Codex | Codex | GPT-5 | `Codex_Prompt_Phase0_最终收尾_Freeze_V1.0.md` | V1.0 | 完成 Phase 0 最终收尾并冻结工程结构 | 未精确记录 | 未执行 | 待指定 | 待审核 | 不涉及业务正文 |

------------------------------------------------------------------------

## Prompt 执行记录

  -----------------------------------------------------------------------------------------------------------------------------------------------------
  编号     日期         Agent   Prompt 文件                                       Prompt 版本 操作类型         Git Commit   Review   备注
  -------- ------------ ------- ------------------------------------------------- ----------- ---------------- ------------ -------- ------------------
  P-0001   2026-07-22   Codex   Codex_Prompt_家庭迎新生命操作手册初始化_V2.0.md   V2.0        初始化工程骨架   （待填写）   已审核   创建项目基础结构

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

`prompts/initialization/Codex_Prompt_已有项目增加AI文档工程治理_V1.0.md`

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
| 1 | `doc/prompt/Codex_Prompt_家庭迎新生命操作手册初始化_V2.0.md` | `prompts/initialization/Codex_Prompt_家庭迎新生命操作手册初始化_V2.0.md` | Move | 初始化 Prompt 归入初始化分类 |
| 2 | `doc/prompt/Codex_Prompt_已有项目增加AI文档工程治理_V1.0.md` | `prompts/initialization/Codex_Prompt_已有项目增加AI文档工程治理_V1.0.md` | Move | 本次治理 Prompt 归入初始化分类 |
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

`prompts/initialization/Codex_Prompt_Phase0.2_工程完善_V1.0.md`

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
| 1 | `doc/prompt/第一卷《孕晚期准备（32周～生产）》章节骨架设计 V1.0.md` | `prompts/volume-01/01-outline/Codex_Prompt_第一卷章节骨架_V1.0.md` | Move + Rename | 迁入第一卷骨架层并采用规范文件名 |

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

`prompts/initialization/4_Codex_Prompt_Phase0_最终收尾_Freeze_V1.0.md`

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
