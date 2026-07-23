# 项目路线图

## 路线图目标

本路线图用于记录项目阶段、阶段出口和下一步顺序。阶段状态以 `project-context.md` 和根目录 `STATUS.md` 为当前有效信息来源。

## 阶段总览

| 阶段 | 目标 | 主要交付物 | 状态 |
| --- | --- | --- | --- |
| Phase 0 | 初始化并冻结 Markdown 工程结构 | 根入口、八个业务模块、模板、资源与发布目录 | Completed（Frozen） |
| Phase 0.1 | 建立 AI 文档工程治理 | Prompt 管理、执行历史、项目上下文、ADR | Completed |
| Phase 0.2 | 完善工程入口和 Prompt 分层 | `STATUS.md`、术语表、路线图、Prompt 元数据与第一卷分层目录 | Completed |
| Phase 1 | 设计第一卷章节骨架 | 第一卷章节清单、文件边界、空模板与模块导航 | Ready for Content Specification |
| Phase 2 | 编写和审核第一卷内容 | 经来源核验和人工 Review 的第一卷 Markdown | 规划中 |
| Phase 3 | 推进第二卷至第六卷 | 各卷章节骨架及经审核内容 | 规划中 |
| Phase 4 | 完善第七卷和第八卷 | 逐日、逐月内容与跨模块导航 | 规划中 |
| Phase 5 | 全局审核与发布 | 一致性检查、医学内容审核、PDF 与 Word 发布流程 | 规划中 |

## 当前阶段出口

Phase 0.2 完成需满足：

- [x] 历史 `doc/` 中的 Prompt 已迁移。
- [x] Prompt 分类目录包含维护说明。
- [x] 第一卷 Prompt 使用 `01-outline` 至 `04-release` 分层。
- [x] 项目状态、路线图和术语模板已建立。
- [x] Prompt 索引与执行历史包含扩展元数据。
- [x] 项目上下文已切换到 Phase 0.2 完成状态。
- [x] 人工确认 Phase 0 最终冻结方案。

## Phase 1 入口条件

- [x] Phase 0 工程结构已冻结。
- [x] 用户已批准 ADR-005 所记录的一次性 Prompt 命名治理升级。
- [x] PR-009 已批准执行，范围和输出边界保持“不生成正文”。

## Phase 1 当前出口

- [x] Prompt 命名和标题规范完成统一。
- [x] Prompt Index 已集中维护 Phase、Milestone、Volume、Stage 和文件路径。
- [x] 第一卷 README、七个章节空模板和跨卷边界已建立。
- [x] 第一卷章节架构通过人工 Review。
- [x] Prompt 命名、归档和状态模型整理完成。
- [ ] 正文信息来源与医学核验方案获得确认。

第一卷章节架构工程清理已完成，下一步进入 PR-011：第一卷正文生成规范设计；这不表示第一卷业务内容已完成。

## 内容里程碑

| 里程碑 | 对应范围 | 当前状态 |
| --- | --- | --- |
| Milestone 1 | 第一卷：孕晚期准备 | Ready for Content Specification |
| Milestone 2 | 第二卷：生产当天 | 规划中 |
| Milestone 3 | 第三卷：医院住院 | 规划中 |
| Milestone 4 | 第四卷：妈妈恢复 | 规划中 |
| Milestone 5 | 第五卷：新生儿护理 | 规划中 |
| Milestone 6 | 第六卷：爸爸指南 | 规划中 |
| Milestone 7 | 第七卷：月子 42 天 | 规划中 |
| Milestone 8 | 第八卷：0–1 岁（第一年） | 规划中 |
