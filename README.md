# Mattbusel Rust Crates

[![Star History Chart](https://api.star-history.com/svg?repos=Mattbusel/rust-crates&type=Date)](https://star-history.com/#Mattbusel/rust-crates)


A collection of production-grade Rust libraries for AI agents, LLM infrastructure, and financial market systems. Each crate is independently usable, zero-panic, and ships with extensive test coverage.

---

## AI Agent & LLM Libraries

### [tokio-agent-memory](https://github.com/Mattbusel/tokio-agent-memory)
Tokio-native agent memory system — episodic, semantic, and working memory with decay scheduling, persistence, and a shared memory bus for multi-agent coordination.

```toml
tokio-agent-memory = { git = "https://github.com/Mattbusel/tokio-agent-memory", tag = "v0.1.0" }
```

---

### [tokio-memory](https://github.com/Mattbusel/tokio-memory)
Agent memory primitives with the Ebbinghaus forgetting curve, consolidation pipelines, and pluggable persistence. Full async Tokio runtime integration.

```toml
tokio-memory = { git = "https://github.com/Mattbusel/tokio-memory", tag = "v0.1.0" }
```

---

### [llm-wasm](https://github.com/Mattbusel/llm-wasm)
LLM inference primitives for WebAssembly and edge environments — FNV-1a cache, TTL cache, retry with backoff, guard chain, model router, cost ledger, template engine, JSON/Markdown formatters.

```toml
llm-wasm = { git = "https://github.com/Mattbusel/llm-wasm", tag = "v0.1.0" }
```

---

### [llm-budget](https://github.com/Mattbusel/llm-budget)
Autonomous cost governance — hard budget enforcement that blocks requests before they exceed spend limits. Per-model, per-agent, and fleet-wide accounting.

```toml
llm-budget = { git = "https://github.com/Mattbusel/llm-budget", tag = "v0.1.0" }
```

---

### [llm-sync](https://github.com/Mattbusel/llm-sync)
CRDT and vector clock primitives for distributed LLM agent state synchronization — GCounter, PNCounter, LWWRegister, ORSet, and deterministic state merge.

```toml
llm-sync = { git = "https://github.com/Mattbusel/llm-sync", tag = "v0.1.0" }
```

---

### [llm-diff](https://github.com/Mattbusel/llm-diff)
Output diffing and versioning for LLM responses — semantic diff, append-only version store, and lineage tracking for prompt engineering workflows.

```toml
llm-diff = { git = "https://github.com/Mattbusel/llm-diff", tag = "v0.1.0" }
```

---

### [wasm-agent](https://github.com/Mattbusel/wasm-agent)
ReAct agent loop for WASM and edge runtimes — Thought-Action-Observation with tool dispatch, full reasoning traces, and resumable state serialization.

```toml
wasm-agent = { git = "https://github.com/Mattbusel/wasm-agent", tag = "v0.1.0" }
```

---

### [mem-graph](https://github.com/Mattbusel/mem-graph)
Knowledge graph primitives — typed entity nodes, directed relationships, property maps, BFS/DFS traversal, and query by type or property value.

```toml
mem-graph = { git = "https://github.com/Mattbusel/mem-graph", tag = "v0.1.0" }
```

---

## Financial Market Libraries

### [fin-primitives](https://github.com/Mattbusel/fin-primitives)
Financial market primitives — `Price`/`Quantity`/`Symbol` newtypes, BTreeMap order book, OHLCV aggregation, SMA/EMA/RSI indicators, position ledger with PnL, and composable risk monitor.

```toml
fin-primitives = { git = "https://github.com/Mattbusel/fin-primitives", tag = "v0.1.0" }
```

---

### [fin-stream](https://github.com/Mattbusel/fin-stream)
Real-time market data streaming pipeline — lock-free SPSC ring buffer, 100K+ ticks/second ingestion, multi-timeframe OHLCV construction, and Lorentz transforms on financial time series.

```toml
fin-stream = { git = "https://github.com/Mattbusel/fin-stream", tag = "v0.1.0" }
```

---

## Design principles

All crates in this collection follow the same engineering standards:

- **Zero panics** — every fallible operation returns `Result`; `unwrap` and `expect` are banned in production paths
- **Typed errors** — every crate has a domain-specific error enum with `thiserror`
- **Test coverage** — unit, integration, and property-based test suites ship with every crate
- **No unnecessary dependencies** — each crate pulls in only what it needs
- **Composable** — designed to work together or standalone

## Related

- [Special-Relativity-in-Financial-Modeling](https://github.com/Mattbusel/Special-Relativity-in-Financial-Modeling) — C++20 implementation of special-relativistic geometry applied to OHLCV financial data
- [tokio-prompt-orchestrator](https://github.com/Mattbusel/tokio-prompt-orchestrator) — Multi-core Tokio-native orchestration for LLM pipelines
- [llm-cpp](https://github.com/Mattbusel/llm-cpp) — 26 single-header C++ libraries for LLM infrastructure
