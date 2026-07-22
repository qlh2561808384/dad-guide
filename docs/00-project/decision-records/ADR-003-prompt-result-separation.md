# ADR-003：Prompt 与结果分离

## 日期

2026-07-22

## 状态

已确认

## 背景

项目由多个 AI 工具和人工协作者长期维护。如果 Prompt、最终文档和执行记录混放，容易出现来源不明、误把指令当成果、重复执行或无法审计的问题。

## 决策

- `prompts/` 只存放 Prompt。
- `docs/` 存放最终 Markdown 结果。
- `docs/00-project/` 存放项目上下文、执行历史、写作规范和设计决策等治理信息。
- 图片、图表和流程图源文件存放在 `assets/`。
- PDF、Word 等发布产物存放在 `release/`。

## 选择原因

- 明确指令、结果和治理记录的职责边界。
- 便于通过 Git Diff 判断一次变更影响了哪一层。
- 降低错误覆盖业务正文或重复执行 Prompt 的风险。
- 支持按 Prompt 追踪每次文件变更。

## 影响

- 新 Prompt 必须先进入 `prompts/` 的对应分类目录并登记索引。
- Prompt 执行结果不得写入 `prompts/`。
- 每次执行后必须更新 `docs/00-project/prompt-history.md`。
- 历史 Prompt 迁移时需要记录原路径与新路径。

## 相关文件

- `prompts/README.md`
- `prompts/prompt-index.md`
- `docs/00-project/prompt-history.md`
- `docs/00-project/project-context.md`
