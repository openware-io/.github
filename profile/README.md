# openware-io

> 开源 · 可自部署 · 面向真实工程交付

openware-io 长期维护两个工程：**Open IM** 是即时通讯与多租户 SaaS 的全栈产品底座；**GreenPass** 是面向软件工程测试阶段的质量治理平台。

我们不仅开放可运行的产品，也开放支撑这些产品的工程方法：微服务边界、多租户权限、数据隔离、质量门禁、可观测性和可复现部署。

[Open IM](#open-im) · [GreenPass](#greenpass) · [共同原则](#共同工程原则) · [仓库入口](#仓库与入口) · [参与贡献](#参与贡献)

---

## 两大工程总览

| 工程 | 一句话定位 | 核心能力 | 主要技术栈 |
| --- | --- | --- | --- |
| **Open IM** | 开源即时通讯 + 多租户 SaaS 一体化平台 | IM、租户/门店权限、C/B 端、运营后台、多业态经营、一键部署 | Java / Spring Boot、Flutter、Vue 3、Kubernetes |
| **GreenPass** | 软件工程测试治理平台 | 测试闭环、质量门禁、契约测试、可信审计、多租户团队、AI 模型配置 | Go / Temporal、React 19 / TypeScript、PostgreSQL、TimescaleDB |

两个工程独立演进，但共享同一条工程原则：**边界清晰、权限在服务端、数据可隔离、质量可验证、部署可复现。**

---

## Open IM

开源的即时通讯与多租户 SaaS 一体化平台。它把 IM 开放平台、SaaS 经营后台、C 端/B 端、移动端与桌面端、以及本地一键部署放在同一套工程体系里，既可以作为可运行的产品底座，也可以作为微服务、长连接消息和多租户权限设计的参考实现。

### 核心能力

- **IM 基础能力**：账号、会话、消息、群组、好友关系、长连接接入；
- **多租户 SaaS**：租户、组织、门店、角色、权限、数据作用域；
- **经营业务**：订单、支付、会员、库存、报表，以及酒店、KTV 等多业态经营；
- **多端覆盖**：移动 App、桌面端、平台管理后台、SaaS 管理后台、C/B 端 H5；
- **工程化交付**：Docker Compose / Kubernetes / Kind 本地一键部署，统一工程门禁。

### 核心仓库

| 仓库 | 说明 | 技术栈 |
| --- | --- | --- |
| [open-im-server](https://github.com/openware-io/open-im-server) | IM 服务端与 SaaS 平台微服务 | Java (Spring Boot) + Maven |
| [open-chat-app](https://github.com/openware-io/open-chat-app) | 移动客户端（Android / iOS） | Flutter |
| [open-chat-desktop](https://github.com/openware-io/open-chat-desktop) | 桌面客户端（Windows / macOS） | Electron + Vue 3 |
| [open-chat-admin](https://github.com/openware-io/open-chat-admin) | IM 平台 PC 管理后台 | Vue 3 + Element Plus |
| [open-saas-admin](https://github.com/openware-io/open-saas-admin) | SaaS 管理后台（平台运营 / 租户 / 门店） | Vue 3 + Element Plus |
| [open-saas-mobile](https://github.com/openware-io/open-saas-mobile) | SaaS 移动端（C 端 / B 端 H5） | Vue 3 + Vite |
| [open-chat-turn](https://github.com/openware-io/open-chat-turn) | TURN 信令转发服务 | Node.js |

### 从这里开始

- 产品与部署入口：[open-im-server](https://github.com/openware-io/open-im-server)
- 文档中心：[open-im-server/docs](https://github.com/openware-io/open-im-server/tree/main/docs)
- 工程拓扑：[TOPOLOGY](https://github.com/openware-io/open-im-server/blob/main/docs/20-architecture/TOPOLOGY.zh.md)
- 本地一键部署：[README · 一键部署](https://github.com/openware-io/open-im-server#一键部署推荐)

---

## GreenPass

**GreenPass（绿牌放行）** 是面向中大型技术团队的软件工程测试治理平台。它站在软件工程“测试阶段”的位置，对 AI 生成或人编写的被测工程与系统做**质量量化、测试管控与可信治理**；平台自身的用例生成、质量判定、契约分析和篡改检测由 AI 驱动。

GreenPass 不是“只测 AI 产物”的工具：AI 生成的系统能测，人开发的软件系统同样能测；每个工程可以独立选择所用的 AI 模型。

### 核心能力

- **测试闭环**：被测对象画像 → 上游源与生成 → 用例库 → 测试执行 → 契约测试 → 质量门禁；
- **质量治理**：策略即代码、AI 判定、断言强度、变异分数、篡改检测；
- **可信审计**：哈希链、仅追加审计日志、需求追溯矩阵；
- **多租户团队**：团队即租户、成员与角色权限矩阵、团队级数据隔离；
- **模型即配置**：模型池、每个工程独立绑定 AI 模型；
- **执行资源**：调度、隔离、并发与资源池，覆盖浏览器、真机和 K8s 沙箱等测试形态。

### 技术构成

| 层 | 技术 |
| --- | --- |
| 前端 | React 19 + TypeScript + Vite + Tailwind CSS v4 + shadcn/ui |
| 后端 | Go + Temporal |
| 数据 | PostgreSQL（RLS 多租户）+ TimescaleDB + Redis + S3 兼容对象存储 |
| 交付 | Kind / Kubernetes、OpenAPI 契约、可独立打开的单文件原型 |

### 从这里开始

- 工程入口：[open-green-pass](https://github.com/openware-io/open-green-pass)
- 产品定位：[README · 产品定位](https://github.com/openware-io/open-green-pass#产品定位)
- 文档目录：[GreenPass docs](https://github.com/openware-io/open-green-pass/tree/main/docs)
- 技术设计：[TECH-DESIGN](https://github.com/openware-io/open-green-pass/blob/main/docs/architecture/TECH-DESIGN.md)

---

## 共同工程原则

- **开源可自部署**：许可证以各仓库为准；Open IM 使用 Apache License 2.0，GreenPass 使用 MIT License。
- **服务端授权**：菜单隐藏不是权限；接口必须有权限码、数据作用域和业态边界。
- **数据可隔离**：租户、门店、团队的数据边界由签名上下文和服务端查询共同保证。
- **质量可验证**：不把“构建成功”当作“功能正确”；关键链路需要测试、证据和门禁。
- **部署可复现**：固定依赖版本，提供本地、容器和 Kubernetes 的可重复路径。
- **文档随代码维护**：架构、权限、迁移和发布变更必须同步对应文档。

---

## 仓库与入口

### Open IM 与客户端

见上方 [Open IM · 核心仓库](#open-im)。

### GreenPass

见上方 [GreenPass](#greenpass)。

### 组织与共享

| 仓库 | 说明 |
| --- | --- |
| [open-website](https://github.com/openware-io/open-website) | 组织官网与静态内容站点 |
| [.github](https://github.com/openware-io/.github) | 组织主页、贡献指南、安全政策与社区健康文件 |

---

## 参与贡献

欢迎提交 Issue、Pull Request 或参与讨论。

- 贡献指南：[CONTRIBUTING.md](../CONTRIBUTING.md)
- 行为准则：[CODE_OF_CONDUCT.md](../CODE_OF_CONDUCT.md)
- 安全漏洞：请按 [SECURITY.md](../SECURITY.md) 私下报告，不要公开提交 Issue。

提交前请优先阅读目标仓库的 README、工程规范和测试说明；各仓库可能有不同的技术栈、门禁和许可证要求。
