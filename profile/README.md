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
| [danielfm/pybreaker](https://github.com/repolex-forx/danielfm--pybreaker) | v1.4.1 | 2026-11-22 |
| [epage/toml-test-rs](https://github.com/repolex-forx/epage--toml-test-rs) | v1.0.4 | 2026-11-22 |
| [zen-xu/pyarrow-stubs](https://github.com/repolex-forx/zen-xu--pyarrow-stubs) | 20.0.0.20251215 | 2026-11-22 |
| [pydantic/pydantic-extra-types](https://github.com/repolex-forx/pydantic--pydantic-extra-types) | v2.11.2 | 2026-11-22 |
| [dtolnay/no-panic](https://github.com/repolex-forx/dtolnay--no-panic) | 0.1.36 | 2026-11-22 |
| [purpleprotocol/mimalloc_rust](https://github.com/repolex-forx/purpleprotocol--mimalloc_rust) | v0.1.48 | 2026-11-22 |
| [fastapi/fastapi-cli](https://github.com/repolex-forx/fastapi--fastapi-cli) | 0.0.24 | 2026-11-22 |
| [webpack/copy-webpack-plugin](https://github.com/repolex-forx/webpack--copy-webpack-plugin) | v14.0.0 | 2026-11-22 |
| [trentm/python-markdown2](https://github.com/repolex-forx/trentm--python-markdown2) | v1.0.1.17 | 2026-11-22 |
| [pypa/trove-classifiers](https://github.com/repolex-forx/pypa--trove-classifiers) | 2026.1.14.14 | 2026-11-22 |
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
