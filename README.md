# Mattbusel Rust crates

An index of Rust libraries and tools for LLM agents, LLM infrastructure and market data, each in its own repository. This repository holds no code; it is the catalogue.

Every entry links to its repository. "crates.io" means the crate is published there under that name; otherwise use the git dependency shown.

## Agent building blocks

Small, focused libraries you can drop into any agent.

| Crate | What it does | Install |
|---|---|---|
| [llm-budget](https://github.com/Mattbusel/llm-budget) | Hard USD spend caps per agent and per fleet, kill switches, automatic model downgrade as budget runs low | [crates.io](https://crates.io/crates/llm-budget) `cargo add llm-budget` |
| [tokio-agent-memory](https://github.com/Mattbusel/tokio-agent-memory) | Episodic events with causal links, semantic fact graph, prioritized working memory, decay, fuzzy retrieval, multi-agent bus | [crates.io](https://crates.io/crates/tokio-agent-memory) `cargo add tokio-agent-memory` |
| [tokio-memory](https://github.com/Mattbusel/tokio-memory) | Trait-based episodic and semantic stores, query builder, Ebbinghaus decay, consolidation pipeline, binary snapshots | [crates.io](https://crates.io/crates/tokio-memory) `cargo add tokio-memory` |
| [mem-graph](https://github.com/Mattbusel/mem-graph) | In-memory knowledge graph: typed entities and relationships, BFS/DFS, shortest path, transitive closure, JSON snapshots | git only (the `mem-graph` name on crates.io is another project) |
| [llm-sync](https://github.com/Mattbusel/llm-sync) | CRDTs (GCounter, PNCounter, GSet, LWW register, LWW map) and vector clocks for sharing state between agents | [crates.io](https://crates.io/crates/llm-sync) `cargo add llm-sync` |
| [llm-diff](https://github.com/Mattbusel/llm-diff) | Line and JSON diffs of LLM outputs, content-addressed version store with branches and lineage, audit log | [crates.io](https://crates.io/crates/llm-diff) `cargo add llm-diff` |
| [wasm-agent](https://github.com/Mattbusel/wasm-agent) | Synchronous ReAct loop with tool registry and token-limited history; builds for `wasm32` | [crates.io](https://crates.io/crates/wasm-agent) `cargo add wasm-agent` |
| [llm-wasm](https://github.com/Mattbusel/llm-wasm) | The logic around an LLM call for `wasm32`: TTL cache, retry policy, guards, routing, cost ledger, templates, JSON extraction | [crates.io](https://crates.io/crates/llm-wasm) `cargo add llm-wasm` |
| [llm_affector](https://github.com/Mattbusel/llm_affector) | LLM-as-judge checks: hallucination detection and Rust code critique with typed results (prototype) | git only |

Git dependency form, for crates that are not on crates.io:

```toml
mem-graph = { git = "https://github.com/Mattbusel/mem-graph" }
llm_affector = { git = "https://github.com/Mattbusel/llm_affector" }
```

## Clients, runtimes and orchestration

| Crate | What it does | Install |
|---|---|---|
| [tokio-llm](https://github.com/Mattbusel/tokio-llm) | Async OpenAI and Anthropic client with retry, circuit breaker, USD budget cap and SSE streaming | git only: `tokio-llm = { git = "https://github.com/Mattbusel/tokio-llm" }` |
| [agent-runtime](https://github.com/Mattbusel/agent-runtime) | Full agent runtime: ReAct and plan-execute loops, memory, knowledge graph, circuit breakers, providers, multi-agent bus | [crates.io](https://crates.io/crates/llm-agent-runtime) `cargo add llm-agent-runtime` |
| [tokio-prompt-orchestrator](https://github.com/Mattbusel/tokio-prompt-orchestrator) | Five-stage LLM serving pipeline with dedup, circuit breakers, rate limits and a dead-letter queue; REST, SSE, MCP and TUI | [crates.io](https://crates.io/crates/tokio-prompt-orchestrator) `cargo add tokio-prompt-orchestrator` |
| [HelixRouter](https://github.com/Mattbusel/HelixRouter-adaptive-async-compute-router-) | Adaptive Tokio job router: inline, spawn, CPU pool, batch or drop per job, with a live dashboard | [crates.io](https://crates.io/crates/helixrouter) `cargo add helixrouter` |

## Command-line tools

| Tool | What it does | Install |
|---|---|---|
| [llm-cost-dashboard](https://github.com/Mattbusel/llm-cost-dashboard) | Terminal dashboard for LLM spend from a JSON request log, 83 priced models | `cargo install llm-cost-dashboard` (binary `llm-dash`) |
| [llm-bench](https://github.com/Mattbusel/llm-bench) | Benchmark OpenAI and Anthropic models on your prompts: p50/p99 latency, tokens/s, cost | `cargo install --git https://github.com/Mattbusel/llm-bench` |
| [Every-Other-Token](https://github.com/Mattbusel/Every-Other-Token) | Intercept an LLM token stream live: per-token confidence, token mutation, A/B and provider comparison | `cargo install every-other-token` |

## Market data

| Crate | What it does | Install |
|---|---|---|
| [fin-primitives](https://github.com/Mattbusel/fin-primitives) | Decimal-precise trading building blocks: price types, order book, OHLCV aggregation, indicators, position ledger, risk rules | [crates.io](https://crates.io/crates/fin-primitives) `cargo add fin-primitives` |
| [fin-stream](https://github.com/Mattbusel/fin-stream) | Real-time market data streaming primitives and tick ingestion pipeline | [crates.io](https://crates.io/crates/fin-stream) `cargo add fin-stream` |

## Shared conventions

Most of these crates follow the same habits: typed error enums (`thiserror`), Clippy lints that deny `unwrap`, `expect` and `panic` in library code, and unit plus integration tests. Maturity varies; each README has a status section saying what works and what does not yet.

## Related, not Rust

- [llm-cpp](https://github.com/Mattbusel/llm-cpp): single-header C++17 libraries for LLM features (streaming, retries, caching, RAG, agents).
- [Special-Relativity-in-Financial-Modeling](https://github.com/Mattbusel/Special-Relativity-in-Financial-Modeling): C++20 research code applying special-relativistic geometry to OHLCV data.
- [awesome-llm-infra](https://github.com/Mattbusel/awesome-llm-infra): curated list of LLM infrastructure projects.

## License

The index itself is MIT licensed, see [LICENSE](LICENSE). Licensing of each crate is set in its own repository.


## Hire the author

**Need this kind of engineering on your product?** I take on a small number of client builds: LLM features, iOS apps and performance work, fixed price. [Services and pricing](https://mattbusel.github.io/) · [Email](mailto:mattbusel@gmail.com) · [LinkedIn](https://www.linkedin.com/in/matthewbusel/)
