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
Draft → Testing → Approved → Archived
```

| 生命周期状态 | 含义 | 对应索引状态 |
| --- | --- | --- |
| Draft | Prompt 正在设计，尚未具备执行条件 | 草稿 |
| Testing | Prompt 正在试运行或等待执行结果 Review | 执行中、已执行 |
| Approved | Prompt 及其执行结果已通过人工 Review | 已审核 |
| Archived | Prompt 已被替代或停止使用 | 已废弃 |

生命周期变化必须同步更新 `prompt-index.md`。归档只改变 Prompt 的使用状态，不删除历史执行记录。

## Prompt 分类

| 目录 | 分类 | 用途 |
| --- | --- | --- |
| `initialization/` | 初始化与治理 | 初始化工程、升级治理规则 |
| `volume-01/` 至 `volume-08/` | 分卷任务 | 设计章节、生成或修订对应分卷内容 |
| `release/` | 发布任务 | 设计和执行发布流程 |
| `archive/` | 归档 | 保存已废弃或被替代的 Prompt |

## 命名规范

统一格式：

```text
<工具>_Prompt_<模块>_<用途>_V<版本>.md
```

示例：

- `Codex_Prompt_项目初始化_V2.0.md`
- `Codex_Prompt_已有项目增加AI文档工程治理_V1.0.md`
- `Codex_Prompt_第一卷章节骨架_V1.0.md`

同一 Prompt 的重大范围变化提升主版本，兼容性调整提升次版本。旧版本不直接覆盖，应迁移至 `archive/` 或保留并标记状态。

## 维护规则

1. 执行前先在 `prompt-index.md` 登记用途、输入、输出、依赖和状态。
2. 执行期间将状态标记为“执行中”，完成后改为“已执行”，人工确认后改为“已审核”。
3. 每次执行后更新 `docs/00-project/prompt-history.md`，记录具体文件路径。
4. 阶段切换或重大任务完成后更新 `docs/00-project/project-context.md`。
5. 不覆盖同名 Prompt；同名文件先比较内容，无法确认时保留原文件并报告。
6. 废弃 Prompt 不直接删除，迁移到 `archive/` 并在索引中标记“已废弃”。
7. Prompt 只修改任务授权范围内的文件，不重新初始化既有项目。
