<p align="center">
  <img src="https://avatars.githubusercontent.com/u/346242954?s=224&amp;v=4" width="112" height="112" alt="nostosx — a homeward sail embraced by an ocean wave" />
</p>

<h1 align="center">nostosx</h1>

<p align="center"><strong>Explore further. Return to the essentials.</strong></p>

<p align="center">English · <a href="https://github.com/nostosx/.github/blob/main/profile/README.zh-CN.md">简体中文</a></p>

We build composable Go libraries for AI agents and backend services.
Small interfaces, explicit composition, and focused dependencies help you
build applications whose behavior you can understand and control.

## Find your starting point

| Project | What you can build | Try it |
| --- | --- | --- |
| [**agentx**](https://github.com/nostosx/agentx) | Agents that call tools, stream responses, maintain conversations, and resume interrupted work. | [Quick start](https://github.com/nostosx/agentx#quick-start) · [Runnable examples](https://github.com/nostosx/agentx-examples) |
| [**servex**](https://github.com/nostosx/servex) | Backend services with explicit lifecycles, protocol-independent endpoints, and pluggable infrastructure. | [Getting started](https://github.com/nostosx/servex#getting-started) · [HTTP and gRPC examples](https://github.com/nostosx/servex-examples) |
| [**kitx**](https://github.com/nostosx/kitx) | Focused solutions for retries, bounded concurrency, caching, rate limiting, circuit breaking, and I/O. | [Usage](https://github.com/nostosx/kitx#usage) · [Batch, cache, and pipeline examples](https://github.com/nostosx/kitx-examples) |

Start with the project or package you need and compose it in your application.
The agentx and servex cores depend only on the Go standard library and kitx;
kitx itself depends only on the standard library.

### Add the integrations you need

- [**agentx-contrib**](https://github.com/nostosx/agentx-contrib) provides
  model providers, file and SQL stores, OpenTelemetry, logging, and retries.
- [**servex-contrib**](https://github.com/nostosx/servex-contrib) provides
  gRPC, messaging, caching, database integrations, configuration, discovery,
  observability, and middleware.

Contrib modules are installed and versioned independently. Choose the modules
you need; installation instructions live in each contrib repository's README.

## Why nostosx?

*Nostos* means homecoming. For us, it connects exploration with a return to
the essentials: clear code, useful abstractions, and tools that leave
developers in control.

The homeward sail and surrounding wave carry that idea: room to explore,
and a way home. We bring what we learn back into small, reusable pieces.

## How we build

- **Keep the core focused.** Separate core contracts and reference
  implementations from optional integrations. Share general-purpose
  primitives through kitx.
- **Make behavior explicit.** Use constructors, ordinary functions, and
  clear ownership of state and resources. Let applications choose how the
  pieces fit together.
- **Make examples useful.** Show expected behavior, cancellation, failures,
  and cleanup alongside a working happy path.

## Releases and contributions

agentx, servex, and kitx have released v1.0.0. Follow the
[agentx releases](https://github.com/nostosx/agentx/releases),
[servex releases](https://github.com/nostosx/servex/releases), and
[kitx releases](https://github.com/nostosx/kitx/releases) for changes.
Example versions identify source snapshots and their dependencies.
Each repository documents its own compatibility and release policy.

Bug reports with reproductions, documentation improvements, and focused pull
requests are welcome. Start with the relevant repository's README and
CONTRIBUTING.md. Discuss larger changes in an issue first, and follow that
repository's SECURITY.md for private vulnerability reports.
