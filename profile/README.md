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
| [ratatui/line-clipping](https://github.com/repolex-forx/ratatui--line-clipping) | v0.3.7 | 2026-11-22 |
| [dtolnay/async-trait](https://github.com/repolex-forx/dtolnay--async-trait) | 0.1.89 | 2026-11-22 |
| [Nullus157/bs58-rs](https://github.com/repolex-forx/Nullus157--bs58-rs) | cli-0.1.2 | 2026-11-22 |
| [gyscos/zstd-rs](https://github.com/repolex-forx/gyscos--zstd-rs) | zstd-sys-2.0.15 | 2026-11-22 |
| [bytecodealliance/rustix](https://github.com/repolex-forx/bytecodealliance--rustix) | v1.1.4 | 2026-11-22 |
| [near/near-abi-rs](https://github.com/repolex-forx/near--near-abi-rs) | v0.3.0 | 2026-11-22 |
| [near/near-jsonrpc-client-rs](https://github.com/repolex-forx/near--near-jsonrpc-client-rs) | v0.21.0 | 2026-11-22 |
| [near/near-sdk-rs](https://github.com/repolex-forx/near--near-sdk-rs) | v2.0.1 | 2026-11-22 |
| [khorolets/near-ledger-rs](https://github.com/repolex-forx/khorolets--near-ledger-rs) | v0.9.3 | 2026-11-22 |
| [near/near-workspaces-rs](https://github.com/repolex-forx/near--near-workspaces-rs) | near-workspaces-v0.22.1 | 2026-11-22 |
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
