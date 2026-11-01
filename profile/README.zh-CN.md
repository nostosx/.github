<p align="center">
  <img src="https://avatars.githubusercontent.com/u/346242954?s=224&amp;v=4" width="112" height="112" alt="nostosx — 海浪环抱归帆" />
</p>

<h1 align="center">nostosx</h1>

<p align="center"><strong>向外探索，回归本质。</strong></p>

<p align="center"><a href="https://github.com/nostosx/.github/blob/main/profile/README.md">English</a> · 简体中文</p>

我们为 AI Agent 与后端服务构建可组合的 Go 开源库、工程工具和基础设施。
通过小契约、显式应用装配和独立版本的扩展，让行为与资源归属掌握在开发者手中。

## 从这里开始

| 项目 | 用来构建什么 | 开始使用 |
| --- | --- | --- |
| [**agentx**](https://github.com/nostosx/agentx) | 工具调用、多模态、流式响应、可恢复会话、工作流、检索与评测；独立图片、产物、搜索、网页与浏览器契约扩展工具能力。 | [快速开始](https://github.com/nostosx/agentx#quick-start) · [可运行应用](https://github.com/nostosx/agentx-examples) |
| [**servex**](https://github.com/nostosx/servex) | 显式启动与关闭、健康与就绪检查、类型化 CQRS，以及协议和基础设施契约。 | [接入指南](https://github.com/nostosx/servex#getting-started) · [HTTP/gRPC 应用](https://github.com/nostosx/servex-examples) |
| [**kitx**](https://github.com/nostosx/kitx) | 退避、受限并发、共享执行、缓存、限流、熔断与 I/O 等通用基础组件。 | [使用示例](https://github.com/nostosx/kitx#usage) · [批处理、缓存与流水线](https://github.com/nostosx/kitx-examples) |
| [**nostosx-cli**](https://github.com/nostosx/nostosx-cli) | 单体或微服务骨架，独立的服务和业务上下文，类型化 Command/Query 装配、TOML 配置和可选 HTTP/gRPC 契约。 | [安装与生成](https://github.com/nostosx/nostosx-cli#readme) · [发布与二进制](https://github.com/nostosx/nostosx-cli/releases) |
| [**infrax**](https://github.com/nostosx/infrax) | 数据、身份、网关、存储与可观测组件的 Compose 开发组合和 Kubernetes/K3s 清单。 | [本地启动](https://github.com/nostosx/infrax/blob/main/README.zh-CN.md#本地启动) · [运维说明](https://github.com/nostosx/infrax/blob/main/docs/operations.md) |

从需要的包开始，把构造和生命周期管理留在应用装配层，让领域与应用代码独立于协议和具体基础设施。
kitx 只依赖 Go 标准库；agentx 核心使用标准库和选定的 kitx 包；
servex 保留契约与精简应用运行时，不引入外部模块依赖。

## 运行应用所需的基础设施

[infrax](https://github.com/nostosx/infrax) 默认提供 PostgreSQL、Redis、NATS，
按需选择 MySQL、Consul、Vault、APISIX/etcd、Zitadel、Cerbos、兼容 S3 的 RustFS
和完整遥测链路。Docker Compose 与 Kubernetes/K3s 共用组件配置；Kustomize
部署组合选择能力，环境 overlay 提供凭据和部署设置。

应用选择 contrib 适配器，负责客户端、迁移、账号和业务策略；infrax 负责服务部署与持久数据。
单副本本地基线提供隔离验收；生产环境仍需独立验证隔离、TLS、容量与备份恢复。

## 按需组合扩展

- [**agentx-contrib**](https://github.com/nostosx/agentx-contrib)：模型 Provider、OpenAI/Gemini 图片生成、文件/SQL 状态与文件/S3 产物、Embedding 与缓存、模型 fallback、网页正文与隔离 Chromium 会话、GitHub/Notion/飞书数据连接器、可写 Qdrant/Elasticsearch 索引、通用 Servex 向量与全文检索和搜索适配、文档/OCR 解析、OpenTelemetry，以及 trace/评测开发查看页。
- [**servex-contrib**](https://github.com/nostosx/servex-contrib)：HTTP/gRPC 与 SSE/WebSocket/RPC 适配、认证和浏览器会话、SQL/GORM 与迁移、PostgreSQL 向量与全文检索、事务 PGMQ 与持久 SQL 调度、Redis、消息、调度、S3 与协调、配置、服务发现、日志、遥测和资源生命周期。

Contrib 模块独立安装、独立版本化。agentx-contrib 可通过显式适配复用 servex 基础设施；
核心不反向依赖 contrib。凭据、客户端、存储后端和资源关闭归属由应用决定。

## 从完整应用学习

[agentx-examples](https://github.com/nostosx/agentx-examples) 演示 HTTP Agent 服务、应用自有工具与审批边界、持久状态，以及显式装配的 CQRS 命令；PostgreSQL RAG 示例复用 Servex 后端，通过知识工具返回引用。
[servex-examples](https://github.com/nostosx/servex-examples) 在 HTTP/gRPC 间复用类型化用例，并组合带认证的笔记应用、会话、可选数据库、缓存、对象存储和后台任务。
默认使用内存，外部服务按需选择；PostgreSQL 索引示例演示业务写入与入队、向量与全文更新的事务边界。两个项目都说明配置、启动、验证与清理，让装配过程清晰可见。

## 为什么叫 nostosx？

*Nostos* 意为归来、归乡。我们向外探索新能力，把有用的收获带回清晰的接口、容易理解的代码，以及开发者的控制权。
归帆与环抱它的海浪承载着这个想法：向外探索，也有归处。

## 发布与贡献

各仓库有独立的版本与兼容策略。具体版本以对应安装指南和 CHANGELOG 为准；
contrib 标签带模块路径，CLI 发布包含各平台二进制，示例版本标识源码快照及其依赖。
infrax 版本标识部署清单、配置与镜像基线快照。

查看 [Agent 发布](https://github.com/nostosx/agentx/releases)、
[服务扩展](https://github.com/nostosx/servex-contrib/releases)、
[Agent 扩展](https://github.com/nostosx/agentx-contrib/releases) 和
[CLI 发布](https://github.com/nostosx/nostosx-cli/releases)。

请先阅读对应仓库的 README 与 CONTRIBUTING.md，再提交范围明确的 Pull Request。
欢迎提供复现、文档改进与集成测试。安全问题请按对应仓库的 SECURITY.md 私下报告。
