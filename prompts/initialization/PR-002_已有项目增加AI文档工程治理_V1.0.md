# PR-002：已有项目增加 AI 文档工程治理

Version：V1.0

## 项目背景

当前项目“家庭迎新生命操作手册”已经完成基础初始化，现有内容包括：

- README.md
- AGENTS.md
- CLAUDE.md
- docs/
- templates/
- assets/
- release/

本轮任务是“增量治理升级”，不是重新初始化项目。

## 核心要求

1. 不删除已有业务文件。
2. 不重新创建 docs/01 至 docs/08。
3. 不覆盖已有正文和模板。
4. 目标文件已存在时，先读取，再增量合并。
5. 不执行 Git commit、Git push。
6. 不生成 PDF、Word。
7. 本轮不生成任何孕期、生产、月子或育儿正文。

## 执行前必须阅读

- README.md
- AGENTS.md
- CLAUDE.md
- docs/00-project/project-overview.md
- docs/00-project/version-history.md
- docs/00-project/writing-standard.md
- docs/00-project/module-overview.md
- docs/00-project/project-context.md（如存在）
- docs/00-project/prompt-history.md（如存在）
- prompts/prompt-index.md（如存在）

## 一、新增 Prompt 管理目录

在根目录创建：

```text
prompts/
├── README.md
├── prompt-index.md
├── initialization/
├── volume-01/
├── volume-02/
├── volume-03/
├── volume-04/
├── volume-05/
├── volume-06/
├── volume-07/
├── volume-08/
├── release/
└── archive/
```

空目录使用 `.gitkeep` 保留。

`prompts/` 只存 Prompt，不存最终文档、图片、PDF、Word。

## 二、创建 prompts/README.md

至少写明：

- prompts 目录作用
- Prompt 与结果必须分离
- Prompt 生命周期
- Prompt 分类
- 命名规范
- 维护规则

Prompt 生命周期：

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

命名规范以 `prompts/README.md` 和 ADR-005 为准：

```text
PR-XXXX_<名称>_V<版本>.md
```

示例：

- PR-001_项目初始化_V2.0.md
- PR-002_已有项目增加AI文档工程治理_V1.0.md
- PR-003_第一卷章节骨架_V1.0.md

## 三、创建 prompts/prompt-index.md

作用：

说明每个 Prompt 是干什么的、什么时候使用、输入是什么、会输出什么。

必须使用 Markdown 表格，表头：

| 编号 | Prompt 文件 | 当前版本 | 作用 | 使用时机 | 输入 | 预期输出 | 依赖 | 状态 | 备注 |
|------|-------------|---------|------|----------|------|----------|------|------|------|

至少登记：

### PR-001

- Prompt：PR-001_家庭迎新生命操作手册初始化_V2.0.md
- 作用：初始化项目工程骨架
- 输出：README.md、docs/、templates/、assets/、release/
- 状态：已执行

### PR-002

- Prompt：PR-002_已有项目增加AI文档工程治理_V1.0.md
- 作用：增加 Prompt 管理、执行历史、项目上下文和 ADR
- 状态：本次执行

### PR-003

- Prompt：PR-003_第一卷章节骨架_V1.0.md
- 作用：设计第一卷《孕晚期准备（32周～生产）》章节骨架
- 状态：待执行

状态统一使用：

- 草稿
- 待执行
- 执行中
- 已执行
- 已审核
- 已废弃

## 四、创建或更新 docs/00-project/prompt-history.md

作用：

记录每次 Prompt 实际做了哪些操作、生成了哪些文件、修改了哪些文件。

不能只写数量，必须记录具体文件路径。

### 执行摘要表

| 执行编号 | 日期 | Agent | Prompt 文件 | Prompt 版本 | 执行动作 | Git Commit | Review 状态 | 备注 |
|----------|------|-------|-------------|-------------|----------|------------|-------------|------|

### 每次执行的文件映射

```markdown
## EXEC-0001

### Prompt

Prompt 文件名

### 新增文件

| 序号 | 文件路径 | 操作 | 说明 |
|------|----------|------|------|

### 修改文件

| 序号 | 文件路径 | 操作 | 说明 |
|------|----------|------|------|

### 删除文件

| 序号 | 文件路径 | 操作 | 说明 |
|------|----------|------|------|
```

连续批量文件允许按明确范围记录，例如：

- docs/07-postpartum-42-days/day-01.md ～ day-42.md（42个）
- docs/08-first-year/month-01.md ～ month-12.md（12个）

禁止只写“生成42个文件”。

本次治理升级必须追加一条执行记录，列出所有实际创建、修改、迁移文件。

## 五、创建或更新 docs/00-project/project-context.md

它是新终端、新 Agent 恢复上下文的第一入口。

必须包含：

1. 项目基本信息
2. 项目目标
3. 家庭背景
4. 当前阶段
5. 已完成内容
6. 当前任务
7. 下一步
8. 上下文恢复顺序

阶段状态：

```text
Phase 0：项目工程骨架初始化 —— 已完成
Phase 0.1：AI 文档工程治理升级 —— 进行中/完成
Phase 1：第一卷章节设计 —— 待开始
```

本次完成后，当前任务写为：

```text
第一卷《孕晚期准备（32周～生产）》章节骨架设计。
```

恢复上下文顺序：

1. README.md
2. docs/00-project/project-context.md
3. prompts/README.md
4. prompts/prompt-index.md
5. docs/00-project/prompt-history.md
6. docs/00-project/project-overview.md
7. docs/00-project/writing-standard.md
8. docs/00-project/module-overview.md
9. AGENTS.md
10. CLAUDE.md
11. docs/00-project/decision-records/

## 六、创建设计决策目录

创建：

```text
docs/00-project/decision-records/
```

至少包含：

- ADR-template.md
- ADR-001-markdown-as-source.md
- ADR-002-fine-grained-structure.md
- ADR-003-prompt-result-separation.md
- ADR-004-project-context-recovery.md

ADR-003 必须说明：

- prompts/ 存放 Prompt
- docs/ 存放最终结果
- docs/00-project/ 存放治理信息

ADR-004 必须说明：

每次阶段切换、重大任务完成后更新 project-context.md。

## 七、更新 AGENTS.md

只能增量修改，增加：

- 执行前阅读顺序
- Prompt 与结果分离
- Prompt 执行后更新 prompt-history.md
- 必须记录具体文件，不能只记录数量
- 阶段完成后更新 project-context.md

## 八、更新 CLAUDE.md

只能增量修改，增加：

- 新终端恢复规则
- 修改范围控制
- 不重新初始化项目
- 不批量覆盖已有文件
- 任务完成后输出具体创建、修改、删除、迁移文件
- 输出待人工确认项和下一步建议

## 九、迁移已有 Prompt

搜索项目中的 Prompt 文件。

如果找到：

```text
PR-001_家庭迎新生命操作手册初始化_V2.0.md
```

移动到：

```text
prompts/initialization/
```

将本次 Prompt 也放到：

```text
prompts/initialization/
```

要求：

- 不覆盖同名文件
- 同名时比较内容
- 无法确认时保留原文件并报告
- 记录原路径和新路径

## 十、禁止事项

禁止：

- 重建项目
- 修改 docs/01 至 docs/08 的业务内容
- 修改 day-01 至 day-42 模板内容
- 修改 month-01 至 month-12 模板内容
- 删除已有 README
- 重命名业务模块目录
- 生成业务正文
- Git commit
- Git push
- 生成 PDF 或 Word

## 十一、完成后检查

确认：

1. prompts/ 已创建
2. prompts/README.md 已创建
3. prompts/prompt-index.md 已登记已知 Prompt
4. prompt-history.md 记录了具体文件
5. project-context.md 写明当前阶段
6. decision-records/ 已创建
7. AGENTS.md 已增量更新
8. CLAUDE.md 已增量更新
9. 原业务文件未被破坏
10. Git diff 仅包含本次治理升级

## 十二、完成后输出

必须输出：

1. 本次任务摘要
2. 新增目录树
3. 创建文件清单
4. 修改文件清单
5. 删除文件清单
6. 迁移文件清单（原路径 → 新路径）
7. 风险与待确认项
8. 下一步建议

创建、修改、删除和迁移文件必须逐个列出具体路径。

下一步只建议：

执行第一卷《孕晚期准备（32周～生产）》章节骨架 Prompt。

等待下一步指令。
