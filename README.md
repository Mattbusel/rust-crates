# Mattbusel Rust crates

My Rust crates for LLM agents and market data.

## Agents

- [llm-budget](https://github.com/Mattbusel/llm-budget): hard dollar caps per agent. `cargo add llm-budget`
- [tokio-agent-memory](https://github.com/Mattbusel/tokio-agent-memory): agent memory with decay. `cargo add tokio-agent-memory`
- [tokio-memory](https://github.com/Mattbusel/tokio-memory): episodic and semantic stores. `cargo add tokio-memory`
- [mem-graph](https://github.com/Mattbusel/mem-graph): in-memory knowledge graph. Git only.
- [llm-sync](https://github.com/Mattbusel/llm-sync): shared state between agents. `cargo add llm-sync`
- [llm-diff](https://github.com/Mattbusel/llm-diff): diffs of LLM outputs. `cargo add llm-diff`
- [wasm-agent](https://github.com/Mattbusel/wasm-agent): ReAct loop for `wasm32`. `cargo add wasm-agent`
- [llm-wasm](https://github.com/Mattbusel/llm-wasm): cache, retry and guards for LLM calls on `wasm32`. `cargo add llm-wasm`
- [llm_affector](https://github.com/Mattbusel/llm_affector): LLM-as-judge checks. `cargo add llm_affector`

## Clients and runtimes

- [tokio-llm](https://github.com/Mattbusel/tokio-llm): async OpenAI and Anthropic client. Git only.
- [agent-runtime](https://github.com/Mattbusel/agent-runtime): full agent runtime. `cargo add llm-agent-runtime`
- [tokio-prompt-orchestrator](https://github.com/Mattbusel/tokio-prompt-orchestrator): LLM serving pipeline. `cargo add tokio-prompt-orchestrator`
- [HelixRouter](https://github.com/Mattbusel/HelixRouter-adaptive-async-compute-router-): adaptive Tokio job router. `cargo add helixrouter`

## Tools

- [llm-cost-dashboard](https://github.com/Mattbusel/llm-cost-dashboard): terminal dashboard for LLM spend. `cargo install llm-cost-dashboard`
- [llm-bench](https://github.com/Mattbusel/llm-bench): benchmark models on your prompts. `cargo install --git https://github.com/Mattbusel/llm-bench`
- [Every-Other-Token](https://github.com/Mattbusel/Every-Other-Token): watch an LLM token stream live. `cargo install every-other-token`

## Market data

- [fin-primitives](https://github.com/Mattbusel/fin-primitives): exact decimal trading basics. `cargo add fin-primitives`
- [fin-stream](https://github.com/Mattbusel/fin-stream): real-time market data streaming. `cargo add fin-stream`

[crates.io](https://crates.io/users/mattbusel) · [tensorust.com/open-source](https://tensorust.com/open-source/)

License: MIT for this index. Each crate sets its own.

More: [docs/DETAILS.md](docs/DETAILS.md)
