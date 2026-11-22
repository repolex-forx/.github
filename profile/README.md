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
| [deadpool-rs/deadpool](https://github.com/repolex-forx/deadpool-rs--deadpool) | deadpool-v0.12.1 | 2026-11-22 |
| [rust-lang-nursery/pin-utils](https://github.com/repolex-forx/rust-lang-nursery--pin-utils) | 0.1.0 | 2026-11-22 |
| [rustls/pki-types](https://github.com/repolex-forx/rustls--pki-types) | v/1.15.1 | 2026-11-22 |
| [Keats/jsonwebtoken](https://github.com/repolex-forx/Keats--jsonwebtoken) | v11.0.0 | 2026-11-22 |
| [rustls/rustls](https://github.com/repolex-forx/rustls--rustls) | v/0.23.45 | 2026-11-22 |
| [rust-native-tls/rust-native-tls](https://github.com/repolex-forx/rust-native-tls--rust-native-tls) | v0.2.18 | 2026-11-22 |
| [askama-rs/askama](https://github.com/repolex-forx/askama-rs--askama) | v0.16.1 | 2026-11-22 |
| [metrics-rs/metrics](https://github.com/repolex-forx/metrics-rs--metrics) | metrics-v0.24.6 | 2026-11-22 |
| [ramosbugs/oauth2-rs](https://github.com/repolex-forx/ramosbugs--oauth2-rs) | oauth2-reqwest-0.1.0-alpha.3 | 2026-11-22 |
| [ibraheemdev/matchit](https://github.com/repolex-forx/ibraheemdev--matchit) | v0.9.2 | 2026-11-22 |
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
