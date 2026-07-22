# Codex Prompt：Phase 0 最终收尾（Freeze）V1.0

## 任务定位

本次任务是 Phase 0 的最终收尾。

目标：

- 完善最后两项工程能力
- 正式宣布 Phase 0 完成
- 冻结工程结构
- 为 Phase 1 内容生产做好准备

注意：

本次不是初始化项目。
本次不是治理升级。
本次不是生成任何业务正文。

---

# 一、执行原则

必须遵守：

1. 不修改 docs/01～08 的业务内容。
2. 不修改模板正文。
3. 不生成医学内容。
4. 不调整目录结构（仅新增本 Prompt 指定文件）。
5. 不执行 Git Commit / Git Push。
6. 所有修改采用增量方式。

---

# 二、本轮新增内容

## 1. 新建 CHANGELOG.md（根目录）

用途：

记录项目版本演进。

采用 Keep a Changelog 风格。

至少包含：

- v0.1.0-engineering
  - 完成项目初始化
  - 完成 AI 文档工程治理
  - 完成 Prompt 生命周期
  - 完成 Prompt Index / History
  - 完成 ADR
  - 完成 STATUS
  - 完成 Roadmap
  - 完成 Glossary
  - Phase 0 冻结

保留后续：

- v1.0.0
- v1.1.0
- v2.0.0

作为占位。

---

## 2. 优化 release 结构

调整为：

release/
├── README.md
├── v0.1.0-engineering/
│   ├── pdf/
│   └── docx/
├── v1.0.0/
│   ├── pdf/
│   └── docx/
└── latest/

空目录保留 .gitkeep。

README 说明：

- latest 永远保存最新发布版
- vX.Y.Z 保存历史版本

---

## 3. 宣布 Phase 0 完成

更新 STATUS.md：

新增：

Phase Status：

Frozen

Freeze Date：

2026-07-22

说明：

除重大设计缺陷外，不再修改工程结构。

当前阶段：

Phase 1（待开始）

当前任务：

第一卷章节骨架设计。

---

## 4. 更新 project-context.md

增加：

# 工程冻结声明

Phase 0 已完成。

工程结构冻结。

后续：

仅允许：

- Prompt 新增
- 内容新增
- Bug 修复

禁止：

- 随意调整目录
- 修改治理体系
- 修改 Prompt 生命周期

除非新增 ADR。

---

## 5. 更新 roadmap.md

标记：

Phase 0：Completed

Phase 1：Next

增加里程碑：

Milestone 1：

第一卷

Milestone 2：

第二卷

……

Milestone 8：

第一年

---

## 6. 更新 prompts/prompt-index.md

新增：

PR-008

Codex_Prompt_Phase0_最终收尾_Freeze_V1.0.md

状态：

已执行。

---

## 7. 更新 prompt-history.md

追加：

EXEC-0004

记录：

本次所有新增、修改文件。

---

## 8. 更新 AGENTS.md

增加规则：

如果 STATUS.md 显示：

Phase Status = Frozen

则：

禁止主动修改工程结构。

除非用户明确要求。

---

## 9. 更新 CLAUDE.md

增加同样规则。

---

# 三、完成后检查

确认：

- CHANGELOG.md 已创建
- release 新结构已建立
- STATUS 为 Frozen
- project-context 写明冻结
- roadmap 更新完成
- prompt-index 新增 PR-008
- prompt-history 新增 EXEC-0004

---

# 四、完成后输出

输出：

1. 创建文件
2. 修改文件
3. 新目录树
4. Phase 0 是否达到冻结条件
5. 后续建议

如果全部完成，最后必须输出：

**"Phase 0（AI Documentation Engineering）已正式完成并冻结。建议从下一次任务开始进入 Phase 1：第一卷《孕晚期准备（32周～生产）》内容生产。"**
