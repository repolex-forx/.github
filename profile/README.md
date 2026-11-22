# repolex-forx

**Source code as a knowledge graph.** Every repo here contains RDF graph data parsed from an open source project — abstract syntax trees, dependency graphs, LSP-enriched semantic analysis, git history, and more — all queryable with SPARQL.

## [forx-index](https://github.com/repolex-forx/forx-index) — The Catalog

The **[forx-index](https://github.com/repolex-forx/forx-index)** repo is the central catalog of everything we've parsed. It contains JSON-LD manifests that form a lightweight knowledge graph: repositories, parsed commits, and the web of dependencies between projects. Load them into any RDF tool and query with SPARQL.

## Getting Started

Install [rlex](https://github.com/repolex-ai/rlex), the query tool for repolex knowledge graphs:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Download a parsed repo:

```bash
rlex download repolex-ai/rlex
```

**rlex is designed to be used by LLMs in a terminal.** Start your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

```
"Claude, can you check the --help menu of rlex"
"Hermes, can you use the rlex tool to download someorg/somerepo"
"What classes are defined in this codebase?"
"Show me the dependency graph"
```

## Recently Parsed

<!-- AUTO-UPDATED BY FORX - DO NOT EDIT BELOW -->
| Data Source | Tag | Parsed |
|-------------|-----|--------|
| [ibraheemdev/matchit](https://github.com/repolex-forx/ibraheemdev--matchit) | v0.9.2 | 2026-11-22 |
| [programatik29/axum-server](https://github.com/repolex-forx/programatik29--axum-server) | v0.8.0 | 2026-11-22 |
| [djc/bb8](https://github.com/repolex-forx/djc--bb8) | v0.9.1 | 2026-11-22 |
| [hyperium/headers](https://github.com/repolex-forx/hyperium--headers) | headers-v0.4.1 | 2026-11-22 |
| [http-rs/async-session](https://github.com/repolex-forx/http-rs--async-session) | v3.0.0 | 2026-11-22 |
| [nox/serde_urlencoded](https://github.com/repolex-forx/nox--serde_urlencoded) | v0.6.1 | 2026-11-22 |
| [SergioBenitez/cookie-rs](https://github.com/repolex-forx/SergioBenitez--cookie-rs) | 0.18.2 | 2026-11-22 |
| [rust-lang/annotate-snippets-rs](https://github.com/repolex-forx/rust-lang--annotate-snippets-rs) | 0.12.16 | 2026-11-22 |
| [RustCrypto/stream-ciphers](https://github.com/repolex-forx/RustCrypto--stream-ciphers) | salsa20-v0.11.0 | 2026-11-22 |
| [snapview/tokio-tungstenite](https://github.com/repolex-forx/snapview--tokio-tungstenite) | v0.30.0 | 2026-11-22 |
<!-- END AUTO-UPDATED -->

> Browse the full catalog at **[forx-index](https://github.com/repolex-forx/forx-index)**

## What's in each repo?

| Directory | Contents |
|-----------|----------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA |
| `aggregate/ast/` | Combined AST graph per commit — the full codebase structure |
| `aggregate/lsp/` | LSP enrichment: resolved symbols, definitions, references, types |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit |
| `dep/` | Resolved dependency graph with links to other parsed repos |
| `commit/` | Git commit metadata |
| `branch/` `tag/` | Branch and tag metadata |
| `filetree/` | File tree snapshots per commit |

All data is gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), loadable into any triplestore.

---

*Powered by [repolex](https://repolex.ai) · Orchestrated by [forx](https://github.com/repolex-ai/forx) · Queried with [rlex](https://github.com/repolex-ai/rlex)*
