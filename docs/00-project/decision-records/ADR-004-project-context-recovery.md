# ADR-004：使用项目上下文恢复协作状态

## 日期

2026-07-22

## 状态

已确认

## 背景

项目会跨终端、跨会话并由不同 Agent 持续维护。仅依赖对话历史无法可靠恢复当前阶段、已完成内容、任务边界和下一步计划。

## 决策

将 `docs/00-project/project-context.md` 设为新终端和新 Agent 恢复上下文的第一入口之一。

每次阶段切换或重大任务完成后，必须更新 `project-context.md`，至少同步：

- 当前阶段及状态
- 已完成内容
- 当前任务
- 下一步
- 上下文恢复顺序

## 选择原因

- 降低协作交接对单次会话的依赖。
- 防止新 Agent 重新初始化项目或重复执行已完成任务。
- 让任务边界和下一步在 Git 中持续可见。
- 为 Prompt 执行历史提供当前状态入口。

## 影响

- 阶段完成但未更新 `project-context.md` 时，该阶段不视为治理闭环。
- 新 Agent 应按文件中规定的顺序恢复上下文后再修改项目。
- `prompt-history.md` 记录实际执行，`project-context.md` 记录当前有效状态，两者不得相互替代。

## 相关文件

- `docs/00-project/project-context.md`
- `docs/00-project/prompt-history.md`
- `AGENTS.md`
- `CLAUDE.md`
