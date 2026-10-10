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
| [encode/starlette](https://github.com/repolex-forx/encode--starlette) | `96d5023c55` | 2026-10-10 |
| [pallets-eco/flask-alembic](https://github.com/repolex-forx/pallets-eco--flask-alembic) | `9425c61473` | 2026-10-10 |
| [pallets-eco/secure-cookie](https://github.com/repolex-forx/pallets-eco--secure-cookie) | `e06d58d068` | 2026-10-10 |
| [pallets-eco/flask-caching](https://github.com/repolex-forx/pallets-eco--flask-caching) | `0d131e699e` | 2026-10-10 |
| [pallets-eco/flask-mail](https://github.com/repolex-forx/pallets-eco--flask-mail) | `98203358d8` | 2026-10-10 |
| [pallets-eco/wtforms](https://github.com/repolex-forx/pallets-eco--wtforms) | `ae8f4b4133` | 2026-10-10 |
| [pallets-eco/flask-wtf](https://github.com/repolex-forx/pallets-eco--flask-wtf) | `63e2d71269` | 2026-10-10 |
| [pallets-eco/cachelib](https://github.com/repolex-forx/pallets-eco--cachelib) | `34140b8e54` | 2026-10-10 |
| [pydantic/pydantic-extra-types](https://github.com/repolex-forx/pydantic--pydantic-extra-types) | `27cca0ebf5` | 2026-10-10 |
| [litestar-org/litestar-saq](https://github.com/repolex-forx/litestar-org--litestar-saq) | `95619b5f74` | 2026-10-10 |
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
