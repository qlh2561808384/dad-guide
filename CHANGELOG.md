# Changelog

本文件记录项目的重要版本演进，格式参考 Keep a Changelog。项目版本不等同于单个 Prompt 的版本。

## [Unreleased]

### Planned

- 设计 PR-011 第一卷正文生成规范，并建立正文来源核验方案。

## [v0.1.1-engineering] - 2026-07-22

### Added

- 新增 ADR-005，记录冻结后的 Prompt 命名治理升级。
- 启动 Phase 1，并创建第一卷七个章节空模板及模块导航。

### Changed

- 统一 Prompt 命名规范为 `PR-XXXX_<名称>_V<版本>.md`。
- 去除 Prompt 文件的工具名称前缀。
- 去除文件名中的独立 Phase/Milestone 编排前缀。
- 将 PR 编号确立为 Prompt 唯一身份标识。
- 将 Phase、Milestone、Volume、Stage 和文件路径集中到 Prompt Index 维护。

## [v2.0.0] - 规划中

- 预留第二个重大版本，范围将在后续阶段通过 ADR 确认。

## [v1.1.0] - 规划中

- 预留首个兼容性迭代版本，范围将在 v1.0.0 发布后确认。

## [v1.0.0] - 规划中

- 预留第一版正式内容发布。

## [v0.1.0-engineering] - 2026-07-22

### Added

- 完成项目工程骨架初始化。
- 完成 AI 文档工程治理。
- 完成 Prompt 生命周期设计。
- 完成 Prompt Index 和 Prompt History。
- 完成架构决策记录 ADR。
- 完成根目录 STATUS 状态入口。
- 完成项目 Roadmap。
- 完成 Glossary 术语模板。
- 完成版本化 release 目录。

### Changed

- 将第一卷 Prompt 按骨架、内容、审核和发布阶段分层管理。
- 将项目当前阶段切换为 Phase 1 待开始。

### Frozen

- Phase 0 工程结构于 2026-07-22 正式冻结。
- 除重大设计缺陷或新增 ADR 外，不再调整工程结构与治理体系。
