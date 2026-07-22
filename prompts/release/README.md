# 项目发布 Prompt

## 目录用途

本目录保存全项目级别的审核、构建和发布 Prompt。Prompt 本身存放在这里，生成的 PDF、Word 等发布产物必须写入根目录 `release/`。

## 内容范围

- 全项目一致性检查
- 医学内容审核流程
- Markdown 发布前检查
- PDF、Word 构建与发布说明

## 维护规则

1. 仅在相应内容通过人工 Review 后执行发布 Prompt。
2. 发布 Prompt 必须写明输入版本、输出位置和失败处理方式。
3. 不在本目录保存生成结果。
4. 执行结果登记到 `../../docs/00-project/prompt-history.md`。

当前尚未创建可执行的发布 Prompt。
