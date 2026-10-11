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
| [aio-libs/aioga](https://github.com/repolex-forx/aio-libs--aioga) | `dbc0cbdae3` | 2026-10-11 |
| [aio-libs/aioneo4j](https://github.com/repolex-forx/aio-libs--aioneo4j) | `ac72fc7704` | 2026-10-11 |
| [aio-libs/aiohttp-flashbag](https://github.com/repolex-forx/aio-libs--aiohttp-flashbag) | `705b31cca6` | 2026-10-11 |
| [aio-libs/aiosparql](https://github.com/repolex-forx/aio-libs--aiosparql) | `f90ed49df5` | 2026-10-11 |
| [aio-libs/aiolibs-executor](https://github.com/repolex-forx/aio-libs--aiolibs-executor) | `a215e91a81` | 2026-10-11 |
| [aio-libs/sphinxcontrib-asyncio](https://github.com/repolex-forx/aio-libs--sphinxcontrib-asyncio) | `0cef4f21ae` | 2026-10-11 |
| [aio-libs/aiohttp-bot](https://github.com/repolex-forx/aio-libs--aiohttp-bot) | `e5585fcd4f` | 2026-10-11 |
| [aio-libs/create-release](https://github.com/repolex-forx/aio-libs--create-release) | `90f4215e01` | 2026-10-11 |
| [aio-libs/dynoname](https://github.com/repolex-forx/aio-libs--dynoname) | `92a80b5ad5` | 2026-10-11 |
| [aio-libs/triagers](https://github.com/repolex-forx/aio-libs--triagers) | `0cfed58bb6` | 2026-10-11 |
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
