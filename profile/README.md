<p align="center">
  <img src="https://avatars.githubusercontent.com/u/346242954?s=224&amp;v=4" width="112" height="112" alt="nostosx — a homeward sail embraced by an ocean wave" />
</p>

<h1 align="center">nostosx</h1>

<p align="center"><strong>Explore further. Return to the essentials.</strong></p>

<p align="center">English · <a href="https://github.com/nostosx/.github/blob/main/profile/README.zh-CN.md">简体中文</a></p>

We build composable Go libraries, tooling and infrastructure for AI agents and backend services.
Small contracts, explicit application assembly, and independently versioned
integrations keep behavior and resource ownership in your hands.

## Choose your starting point

| Project | Build with it | Start here |
| --- | --- | --- |
| [**agentx**](https://github.com/nostosx/agentx) | Tool-using and multimodal agents, streaming, resumable conversations, workflows, retrieval and evaluation. Independent image generation, artifacts, search, readable web and browser contracts extend its tool capabilities. | [Quick start](https://github.com/nostosx/agentx#quick-start) · [Runnable application](https://github.com/nostosx/agentx-examples) |
| [**servex**](https://github.com/nostosx/servex) | Backend services with explicit startup/shutdown, health and readiness, typed CQRS, and transport/infrastructure contracts. | [Getting started](https://github.com/nostosx/servex#getting-started) · [HTTP/gRPC application](https://github.com/nostosx/servex-examples) |
| [**kitx**](https://github.com/nostosx/kitx) | Focused building blocks for backoff, bounded concurrency, shared work, caching, rate limiting, circuit breaking and I/O. | [Usage](https://github.com/nostosx/kitx#usage) · [Batch, cache and pipeline examples](https://github.com/nostosx/kitx-examples) |
| [**nostosx-cli**](https://github.com/nostosx/nostosx-cli) | Clean monolith or microservice layouts, independent services and business contexts, typed Command/Query wiring, TOML configuration and optional HTTP/gRPC contracts. | [Install and generate](https://github.com/nostosx/nostosx-cli#readme) · [Releases and binaries](https://github.com/nostosx/nostosx-cli/releases) |
| [**infrax**](https://github.com/nostosx/infrax) | Compose development stacks and Kubernetes/K3s manifests for data, identity, gateways, storage and observability. | [Start locally](https://github.com/nostosx/infrax#start-locally) · [Operations](https://github.com/nostosx/infrax/blob/main/docs/operations.md) |

Start with the package you need. Keep constructors and lifecycle ownership in
application assembly; keep domain and application code independent of transport
and concrete infrastructure. Kitx depends only on the Go standard library.
Agentx core uses the standard library and selected kitx packages; servex keeps
contracts and a small application runtime without external module dependencies.

## Run the infrastructure your application chooses

[infrax](https://github.com/nostosx/infrax) starts PostgreSQL, Redis and NATS by
default, with optional MySQL, Consul, Vault, APISIX/etcd, Zitadel, Cerbos,
S3-compatible RustFS and a complete telemetry pipeline. Component-owned
configuration is shared by Docker Compose and Kubernetes/K3s; Kustomize stacks
select capabilities and environment overlays supply credentials and deployment
settings.

Applications choose their contrib adapters and own clients, migrations, accounts
and business policies. Infrax owns service deployment and persistent data. Its
single-replica local baseline includes isolated acceptance checks; production
environments need their own isolation, TLS, capacity and backup/restore validation.

## Add integrations deliberately

- [**agentx-contrib**](https://github.com/nostosx/agentx-contrib): model providers,
  OpenAI/Gemini image generation, file/SQL state and file/S3 artifacts, embeddings and
  caching, model fallback, readable web and isolated Chromium sessions, scoped
  GitHub/Notion/Feishu loaders, writable Qdrant/Elasticsearch indexes, generic Servex vector/text retrieval, search adapters, document/OCR parsers,
  OpenTelemetry, and a trace/evaluation development viewer.
- [**servex-contrib**](https://github.com/nostosx/servex-contrib): HTTP/gRPC and
  SSE/WebSocket/RPC adapters; PostgreSQL vector/text retrieval, transactional PGMQ
  and persistent SQL schedules; authentication and browser sessions; SQL/GORM and
  migrations; Redis, messaging, scheduling, S3 and coordination; configuration,
  discovery, logging, telemetry and lifecycle integration.

Each contrib module is installed and versioned independently. Agentx-contrib can
reuse servex infrastructure through explicit adapters; neither core depends on
contrib. Applications choose credentials, clients, storage and shutdown ownership.

## Learn from complete applications

[agentx-examples](https://github.com/nostosx/agentx-examples) demonstrates an
HTTP Agent service, application-owned tools and approval boundaries, persistent
state and an explicitly assembled CQRS command. Its PostgreSQL RAG example
reuses Servex backends and returns citations through a knowledge tool.
[servex-examples](https://github.com/nostosx/servex-examples) shares typed use cases
across HTTP/gRPC and composes authenticated notes, sessions, optional databases,
caches, object storage and background work. Memory is the default; external
services are explicit choices. A PostgreSQL indexing example demonstrates
business write/enqueue and vector/text update transactions. Both projects document configuration, startup,
verification and cleanup instead of hiding application assembly in a framework.

## Why nostosx?

*Nostos* means homecoming. We explore new capabilities and bring the useful
parts home to clear interfaces, understandable code and developer control.
The homeward sail and surrounding wave carry that idea: room to explore,
and a way home.

## Releases and contributions

Repositories have independent release and compatibility policies. Use each
repository's installation instructions and changelog for concrete versions;
contrib tags include their module path. CLI releases include platform binaries,
and example versions identify source snapshots and their dependencies.
Infrax versions identify manifest/configuration snapshots and their image baseline.

Follow the [Agent releases](https://github.com/nostosx/agentx/releases),
[service integrations](https://github.com/nostosx/servex-contrib/releases),
[Agent integrations](https://github.com/nostosx/agentx-contrib/releases) and
[CLI releases](https://github.com/nostosx/nostosx-cli/releases).

Read the relevant README and CONTRIBUTING.md before opening a focused pull
request. Reproductions, documentation and integration tests are welcome.
Report security issues privately through that repository's SECURITY.md.
