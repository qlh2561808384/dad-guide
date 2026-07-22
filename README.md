# 家庭迎新生命操作手册

家庭迎新生命操作手册（Family New Life Handbook）是一个面向中国新手父母、以爸爸协作视角为重点的长期家庭知识库。

项目以 Markdown 作为唯一源文件，通过 Git 管理版本，并为后续生成 PDF、Word 等交付格式预留结构。

## 当前状态

当前处于项目工程骨架初始化阶段：

- 已规划八个内容模块
- 已建立项目管理文档
- 已预留业务章节空模板
- 尚未编写医学知识、育儿经验或其他业务正文

## 项目结构

| 目录 | 用途 |
| --- | --- |
| `docs/00-project/` | 项目定位、版本、写作规范与模块关系 |
| `docs/01-late-pregnancy/` 至 `docs/08-first-year/` | 八个业务模块 |
| `templates/` | 日常 Checklist 与记录模板 |
| `assets/` | 图片、图表和流程图源文件 |
| `release/` | 后续生成的 PDF、DOCX 文件 |

## 开始使用

1. 阅读 [项目概览](docs/00-project/project-overview.md)。
2. 阅读 [写作规范](docs/00-project/writing-standard.md)。
3. 通过 [模块总览](docs/00-project/module-overview.md) 选择需要维护的模块。
4. 编写内容时复制对应章节或记录模板，并通过 Git 提交变更。

## 内容导航

1. [第一卷：孕晚期准备](docs/01-late-pregnancy/README.md)
2. [第二卷：生产当天](docs/02-labor-day/README.md)
3. [第三卷：医院住院](docs/03-hospital-stay/README.md)
4. [第四卷：妈妈恢复](docs/04-mother-recovery/README.md)
5. [第五卷：新生儿护理](docs/05-newborn-care/README.md)
6. [第六卷：爸爸指南](docs/06-dad-guide/README.md)
7. [第七卷：月子 42 天](docs/07-postpartum-42-days/README.md)
8. [第八卷：0–1 岁](docs/08-first-year/README.md)

## 维护原则

- 内容以实用、操作化、流程化和 Checklist 化为目标。
- 业务内容须经过可靠来源核验，不以本项目替代专业医疗建议。
- 未经确认不新增章节，不在生成目录中直接修改可回溯的源内容。
