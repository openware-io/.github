# openware-io

开源即时通讯（IM）与协作平台。我们以完全开源、免费、可自部署的方式开放 GV Chat 全栈工程。

## 仓库地图

| 仓库 | 说明 | 技术栈 |
| --- | --- | --- |
| [gv-im-server](https://github.com/openware-io/gv-im-server) | IM 服务端：认证 / 消息 / 会话 / 群组 / 管理 / 支付渠道等微服务 | Java (Spring Boot) + Maven |
| [gv-chat-app](https://github.com/openware-io/gv-chat-app) | 移动客户端（Android / iOS） | Flutter |
| [gv-chat-desktop](https://github.com/openware-io/gv-chat-desktop) | 桌面客户端（Windows / macOS） | Electron + Vue 3 |
| [gv-chat-admin](https://github.com/openware-io/gv-chat-admin) | 平台 PC 管理后台 | Vue 3 + Element Plus |
| [gv-saas-admin](https://github.com/openware-io/gv-saas-admin) | SaaS 管理后台（平台运营 / 租户） | Vue 3 + Element Plus |
| [gv-saas-mobile](https://github.com/openware-io/gv-saas-mobile) | SaaS 移动端（C 端 / B 端 H5） | Vue 3 + Vite |
| [gv-chat-turn](https://github.com/openware-io/gv-chat-turn) | TURN 信令转发服务 | Node.js |
| [meta-cogni-cms](https://github.com/openware-io/meta-cogni-cms) | 官网及静态内容站点 | HTML + Nginx |

## 项目定位

- **完全开源免费**：所有仓库采用 Apache License 2.0，可自由使用、修改、商用与再分发。
- **可自部署**：服务端支持 Docker Compose / Kubernetes 部署。
- **全栈完整**：从服务端到移动端、桌面端、管理后台一应俱全。

## 参与贡献

欢迎提交 Issue、PR 或参与讨论，请先阅读 [CONTRIBUTING.md](../CONTRIBUTING.md) 与 [CODE_OF_CONDUCT.md](../CODE_OF_CONDUCT.md)。

安全漏洞请通过 [SECURITY.md](../SECURITY.md) 中的渠道私下报告。
