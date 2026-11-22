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
| [hyperium/h2](https://github.com/repolex-forx/hyperium--h2) | v0.4.19 | 2026-11-22 |
| [alexcrichton/curl-rust](https://github.com/repolex-forx/alexcrichton--curl-rust) | curl-sys-0.4.90 | 2026-11-22 |
| [TeXitoi/structopt](https://github.com/repolex-forx/TeXitoi--structopt) | v0.3.26 | 2026-11-22 |
| [ruuda/thread-id](https://github.com/repolex-forx/ruuda--thread-id) | v5.1.0 | 2026-11-22 |
| [alexcrichton/ssh2-rs](https://github.com/repolex-forx/alexcrichton--ssh2-rs) | libssh2-sys-0.3.2 | 2026-11-22 |
| [rustls/openssl-probe](https://github.com/repolex-forx/rustls--openssl-probe) | 0.2.1 | 2026-11-22 |
| [trifectatechfoundation/zlib-rs](https://github.com/repolex-forx/trifectatechfoundation--zlib-rs) | v0.6.7 | 2026-11-22 |
| [timothee-haudebourg/json-ld](https://github.com/repolex-forx/timothee-haudebourg--json-ld) | v0.21.4 | 2026-11-22 |
| [cloudflare/zlib](https://github.com/repolex-forx/cloudflare--zlib) | v1.2.7.3 | 2026-11-22 |
| [rust-lang/pkg-config-rs](https://github.com/repolex-forx/rust-lang--pkg-config-rs) | 0.3.34 | 2026-11-22 |
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
