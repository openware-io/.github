# Security Policy

## 报告漏洞

如果你发现安全漏洞（如敏感信息泄露、越权访问、注入、认证绕过等），**请勿在公开 Issue 中报告**。请通过以下渠道私下告知维护者：

- 邮件：security@openware-io.example.com
- 或：直接在 GitHub 上创建 **private vulnerability report**（仓库 → Security → Report a vulnerability）

请尽量包含：

- 漏洞类型与影响范围
- 复现步骤（含环境信息与版本）
- 缓解建议（如有）

## 处理流程

1. 维护者确认漏洞后，会尽快修复并发布补丁版本。
2. 敏感漏洞默认在修复发布后才公开披露。
3. 感谢信将写入发布说明（如报告者同意）。

## 安全约定（对贡献者）

- 禁止在代码、文档、示例与提交历史中提交任何真实密钥、令牌、证书私钥、内网地址与生产环境信息。
- 密钥一律通过环境变量 / Secret 注入，仓库只保留 `.env.example` 形式的占位模板。
- 不要提交构建产物（`dist`、`build`、`target`、`node_modules`、打包安装包等）。
