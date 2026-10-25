<p align="center">
  <img src="https://avatars.githubusercontent.com/u/346242954?s=224&amp;v=4" width="112" height="112" alt="nostosx — 海浪环抱归帆" />
</p>

<h1 align="center">nostosx</h1>

<p align="center"><strong>向外探索，回归本质。</strong></p>

<p align="center"><a href="https://github.com/nostosx/.github/blob/main/profile/README.md">English</a> · 简体中文</p>

我们为 AI Agent 与后端服务构建可组合的 Go 开源库。
通过小接口、显式组合和按需依赖，让应用的行为容易理解，也让开发者掌握控制权。

## 从这里开始

| 项目 | 用来构建什么 | 开始使用 |
| --- | --- | --- |
| [**agentx**](https://github.com/nostosx/agentx) | 构建能够调用工具、流式响应、维护会话并恢复中断任务的 Agent。 | [快速开始](https://github.com/nostosx/agentx#quick-start) · [可运行示例](https://github.com/nostosx/agentx-examples) |
| [**servex**](https://github.com/nostosx/servex) | 构建具有显式生命周期、协议无关 Endpoint 与可替换基础设施的后端服务。 | [接入指南](https://github.com/nostosx/servex#getting-started) · [HTTP 与 gRPC 示例](https://github.com/nostosx/servex-examples) |
| [**kitx**](https://github.com/nostosx/kitx) | 按需解决重试、受限并发、缓存、限流、熔断与 I/O 问题。 | [使用示例](https://github.com/nostosx/kitx#usage) · [批处理、缓存与流水线](https://github.com/nostosx/kitx-examples) |

从需要的项目或包开始，在应用中按需组合。
agentx 与 servex 核心只依赖 Go 标准库和 kitx；kitx 本身只依赖标准库。

### 按需接入扩展

- [**agentx-contrib**](https://github.com/nostosx/agentx-contrib)：模型 Provider、文件与 SQL 存储、OpenTelemetry、日志与重试。
- [**servex-contrib**](https://github.com/nostosx/servex-contrib)：gRPC、消息、缓存、数据库集成、配置、服务发现、可观测性与中间件。

Contrib 模块独立安装、独立版本化。只引入应用需要的模块，具体安装方式见对应扩展仓库的 README。

## 为什么叫 nostosx？

*Nostos* 意为归来、归乡。对我们而言，它把探索与回归本质联系在一起：
清晰的代码、有用的抽象，以及让开发者掌握控制权的工具。

归帆与环抱它的海浪承载着这个想法：向外探索，也有归处。
我们把探索中的收获，带回小而可复用的组件中。

## 我们如何构建

- **保持核心精简。** 将核心契约、参考实现与可选扩展分开，通过 kitx 复用通用基础组件。
- **让行为显式可见。** 使用构造函数、普通函数与清晰的状态和资源归属，由应用决定如何组合。
- **让示例便于使用。** 在可运行的正常流程之外，也说明预期行为、取消、失败与资源清理。

## 发布与贡献

agentx、servex、kitx 均已发布 v1.0.0。变更请分别查看
[agentx 发布记录](https://github.com/nostosx/agentx/releases)、
[servex 发布记录](https://github.com/nostosx/servex/releases) 与
[kitx 发布记录](https://github.com/nostosx/kitx/releases)。
示例项目的版本标识源码快照及其依赖；各仓库分别说明兼容性与发布策略。

欢迎提交带有复现步骤的问题、文档改进和范围明确的 Pull Request。
请先阅读对应仓库的 README 与 CONTRIBUTING.md；较大的改动先通过 Issue 讨论。
安全问题请按对应仓库的 SECURITY.md 私下报告。
