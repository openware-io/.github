# Contributing Guide

感谢你对 openware-io 项目的兴趣！以下是参与贡献的约定。

## 提交 Issue

- 先搜索是否已有相同或相关 Issue，避免重复。
- 报告 Bug 时请包含：复现步骤、预期行为、实际行为、环境信息（OS / 版本 / 浏览器等）。
- 功能建议请说明使用场景与期望效果。

## 提交 Pull Request

1. 从 `main` 新建功能分支，命名如 `feat/xxx`、`fix/xxx`。
2. 提交信息使用清晰的描述，例如 `feat: 支持 xxx` / `fix: 修复 xxx 问题`。
3. 尽量为改动补充或更新测试，并确保既有测试通过。
4. 提交前检查是否引入敏感信息（密钥、内网地址、本机路径等），参考各仓库 `SECURITY` 与 `.gitignore` 约定。
5. PR 描述中说明改动目的、测试方式与影响范围。

## 代码风格

- 遵循各仓库既有风格（EditorConfig / ESLint / Formatter 配置为准）。
- 不在提交中夹带构建产物、IDE 配置文件与依赖锁定文件的无关改动。

## 行为准则

所有互动请遵守 [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)：保持尊重、专业与包容。

## 许可证

提交贡献即表示你同意其按项目 [Apache License 2.0](LICENSE) 授权。
