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
| [jupyter/jupyter-sphinx](https://github.com/repolex-forx/jupyter--jupyter-sphinx) | v0.5.3 | 2026-11-22 |
| [taiki-e/pin-project-lite](https://github.com/repolex-forx/taiki-e--pin-project-lite) | v0.2.17 | 2026-11-22 |
| [Amanieu/thread_local-rs](https://github.com/repolex-forx/Amanieu--thread_local-rs) | v1.1.9 | 2026-11-22 |
| [ratatui/ansi-to-tui](https://github.com/repolex-forx/ratatui--ansi-to-tui) | v8.0.1 | 2026-11-22 |
| [oconnor663/duct.rs](https://github.com/repolex-forx/oconnor663--duct.rs) | 1.1.1 | 2026-11-22 |
| [googleapis/python-bigquery](https://github.com/repolex-forx/googleapis--python-bigquery) | v3.40.1 | 2026-11-22 |
| [ratatui/line-clipping](https://github.com/repolex-forx/ratatui--line-clipping) | v0.3.7 | 2026-11-22 |
| [dtolnay/async-trait](https://github.com/repolex-forx/dtolnay--async-trait) | 0.1.89 | 2026-11-22 |
| [Nullus157/bs58-rs](https://github.com/repolex-forx/Nullus157--bs58-rs) | cli-0.1.2 | 2026-11-22 |
| [gyscos/zstd-rs](https://github.com/repolex-forx/gyscos--zstd-rs) | zstd-sys-2.0.15 | 2026-11-22 |
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
