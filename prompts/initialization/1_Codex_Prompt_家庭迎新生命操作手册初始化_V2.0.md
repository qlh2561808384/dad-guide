# Codex Prompt：家庭迎新生命操作手册初始化 V2.0

## 项目名称

家庭迎新生命操作手册（Family New Life Handbook）


## 你的角色

你是一名高级文档工程师、知识库架构师。

你的任务不是直接编写育儿文章，而是帮助创建一个长期维护的家庭知识库项目。

项目要求：
- Markdown作为源文件
- Git进行版本管理
- 后续可生成PDF、Word
- 支持长期迭代


## 项目背景

这是为一个中国家庭定制的《家庭迎新生命操作手册》。

家庭情况：
- 第一胎
- 爸爸第一次成为父亲
- 妈妈第一次生产
- 家庭主要成员只有夫妻两人
- 生产期间会请护工，但护工是一对多模式
- 爸爸承担主要协调、学习、护理、记录职责
- 当前生活城市：杭州


## 本轮任务范围（重要）

本轮只进行：

项目工程骨架初始化。

必须完成：

- 创建目录结构
- 创建根目录 README.md
- 创建 docs/00-project 项目管理文档
- 创建各模块 README.md
- 创建业务章节 Markdown 空模板

禁止：

- 不生成业务正文
- 不填写医学知识内容
- 不填写育儿经验内容
- 不生成PDF
- 不扩展未确认章节


## 项目目录结构

创建：

family-new-life-handbook/

docs/
- 00-project/
  - project-overview.md
  - version-history.md
  - writing-standard.md
  - module-overview.md

- 01-late-pregnancy/
- 02-labor-day/
- 03-hospital-stay/
- 04-mother-recovery/
- 05-newborn-care/
- 06-dad-guide/
- 07-postpartum-42-days/
  - README.md
  - day-01.md 至 day-42.md

- 08-first-year/
  - README.md
  - month-01.md 至 month-12.md


templates/

包含：
- daily-checklist.md
- hospital-record.md
- mother-record.md
- baby-record.md


assets/

包含：
- images
- diagrams
- flowcharts


release/

包含：
- pdf
- docx


## README要求

每个模块README.md包含：

- 模块介绍
- 内容范围
- 章节导航
- 后续编写计划


## 章节模板要求

所有业务章节Markdown文件只创建空结构，不填写内容。

统一模板：

# 标题

## 本章目标

## 为什么重要

## 时间节点

## 操作流程

## 注意事项

## 常见错误

## 医疗风险提醒

## Checklist

- [ ]

## 记录区域


## 项目管理文档

project-overview.md：
- 项目背景
- 项目目标
- 使用方式
- 文档定位
- 版本规划

version-history.md：
- V1.0
- V1.1
- V2.0

writing-standard.md：
- Markdown规范
- 文件命名规范
- 标题规范
- Checklist规范
- Mermaid规范
- 表格规范

module-overview.md：
- 八大模块关系
- 内容边界
- 后续维护方式


## 输出要求

完成初始化后输出：

1. 完整目录树
2. 创建文件列表
3. 初始化说明
4. 后续内容生成计划

等待下一步指令。
