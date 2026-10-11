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
| [aio-libs/aioloop-proxy](https://github.com/repolex-forx/aio-libs--aioloop-proxy) | `ab9a19d098` | 2026-10-11 |
| [aio-libs/aiohttp-benchmarks](https://github.com/repolex-forx/aio-libs--aiohttp-benchmarks) | `018d6a3dd9` | 2026-10-11 |
| [aio-libs/aioppspp](https://github.com/repolex-forx/aio-libs--aioppspp) | `08cda4c4b1` | 2026-10-11 |
| [aio-libs/aiocouchdb](https://github.com/repolex-forx/aio-libs--aiocouchdb) | `84a08cc339` | 2026-10-11 |
| [aio-libs/aioamqp_consumer](https://github.com/repolex-forx/aio-libs--aioamqp_consumer) | `c687211e38` | 2026-10-11 |
| [aio-libs/idna-ssl](https://github.com/repolex-forx/aio-libs--idna-ssl) | `24f5451418` | 2026-10-11 |
| [aio-libs/aiocassandra](https://github.com/repolex-forx/aio-libs--aiocassandra) | `023dd429e1` | 2026-10-11 |
| [aio-libs/aioelasticsearch](https://github.com/repolex-forx/aio-libs--aioelasticsearch) | `81b6ae3434` | 2026-10-11 |
| [aio-libs/aiologstash](https://github.com/repolex-forx/aio-libs--aiologstash) | `61c8f784c5` | 2026-10-11 |
| [aio-libs/aioodbc](https://github.com/repolex-forx/aio-libs--aioodbc) | `62069a2ecb` | 2026-10-11 |
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
