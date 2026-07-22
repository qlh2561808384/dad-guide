# 项目上下文（Project Context）

## 1. 项目基本信息

项目名称：

家庭迎新生命操作手册（Family New Life Handbook）

当前版本：

v0.1.0-engineering（Phase 0 工程冻结版）

项目类型：

Markdown 驱动的家庭知识库项目

维护方式：

Git + AI 协作

## 2. 项目目标

本项目目标：

帮助第一次迎接新生命的家庭，在缺少长期老人陪护情况下，通过流程化、标准化手册完成：

-   孕晚期准备
-   生产陪护
-   医院流程处理
-   新生儿护理
-   妈妈产后恢复
-   宝宝0-1岁成长管理

## 3. 家庭背景

当前定制场景：

-   第一胎
-   爸爸第一次成为父亲
-   妈妈第一次生产
-   家庭主要成员为夫妻两人
-   生产期间计划请护工
-   护工模式：一对多
-   爸爸承担主要协调、学习、护理和记录职责
-   当前城市：杭州

## 4. 项目设计原则

已确认：

### Markdown作为源文件

原因：

-   方便Git管理
-   方便持续修改
-   支持导出PDF、Word

### 细粒度章节设计

原因：

-   方便维护
-   降低修改影响范围
-   支持长期更新

### Prompt驱动开发

所有AI生成和修改行为必须记录。

## 5. 当前阶段

当前有效阶段：Phase 0 已完成并冻结。Phase 1 为下一阶段，尚未开始。

| 阶段 | 状态 | 说明 |
| --- | --- | --- |
| Phase 0：项目工程骨架初始化 | 已完成并冻结 | 已建立根入口、八个模块、通用模板、资源目录和发布目录 |
| Phase 0.1：AI 文档工程治理升级 | 已完成 | 已建立 Prompt 管理、执行历史、项目上下文和 ADR 机制 |
| Phase 0.2：工程完善 | 已完成 | 已建立状态入口、路线图、术语模板、Prompt 分层和扩展元数据 |
| Phase 1：第一卷章节设计 | 下一阶段 | 等待执行第一卷章节骨架 Prompt |

## 6. 已完成内容

- 项目工程骨架和八个业务模块入口
- 月子 42 天逐日空模板
- 0–1 岁逐月空模板
- 通用记录模板
- Prompt 分类目录与索引
- Prompt 执行历史记录
- 项目上下文恢复入口
- Markdown 源文件、细粒度结构、Prompt 分离和上下文恢复 ADR
- 根目录 `STATUS.md` 当前状态入口
- Phase 路线图和术语登记模板
- 第一卷 Prompt 的骨架、内容、审核和发布四阶段目录
- Prompt 索引与执行历史扩展元数据

## 7. 已确认设计决策

-   使用Markdown作为唯一源文件
-   使用Git管理版本
-   使用细粒度章节
-   月子42天拆分day-01至day-42
-   0-1岁拆分month-01至month-12
-   AI生成采用先结构、后正文流程
-   大范围修改需要人工Review
-   Prompt、最终结果和治理信息分目录维护
-   阶段切换或重大任务完成后更新项目上下文

## 8. 当前任务

第一卷《孕晚期准备（32周～生产）》章节骨架设计。

## 9. 下一步

执行 `prompts/volume-01/01-outline/Codex_Prompt_第一卷章节骨架_V1.0.md`。

## 10. 上下文恢复顺序

新AI接手项目时，应按以下顺序读取：

1. `README.md`
2. `STATUS.md`
3. `docs/00-project/project-context.md`
4. `docs/00-project/roadmap.md`
5. `prompts/README.md`
6. `prompts/prompt-index.md`
7. `docs/00-project/prompt-history.md`
8. `docs/00-project/project-overview.md`
9. `docs/00-project/writing-standard.md`
10. `docs/00-project/glossary.md`
11. `docs/00-project/module-overview.md`
12. `AGENTS.md`
13. `CLAUDE.md`
14. `docs/00-project/decision-records/`

## 11. 工程冻结声明

Phase 0 已完成，工程结构自 2026-07-22 起正式冻结。

后续仅允许：

- 新增 Prompt
- 新增内容
- 修复 Bug

后续禁止：

- 随意调整目录
- 修改治理体系
- 修改 Prompt 生命周期

如果重大设计缺陷确实要求改变冻结结构，必须先新增 ADR，说明背景、方案、影响和回退方式，并取得用户明确授权。
