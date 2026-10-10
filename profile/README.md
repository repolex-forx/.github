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
| [pola-rs/polars-benchmark](https://github.com/repolex-forx/pola-rs--polars-benchmark) | `401908a307` | 2026-10-10 |
| [pola-rs/polars-bigquery-client](https://github.com/repolex-forx/pola-rs--polars-bigquery-client) | `89c737ea68` | 2026-10-10 |
| [pola-rs/polars-2.0-benchmark](https://github.com/repolex-forx/pola-rs--polars-2.0-benchmark) | `2d368574ae` | 2026-10-10 |
| [pola-rs/polars-iceberg](https://github.com/repolex-forx/pola-rs--polars-iceberg) | py-0.1.0 | 2026-10-10 |
| [tiangolo/uvicorn-gunicorn-docker](https://github.com/repolex-forx/tiangolo--uvicorn-gunicorn-docker) | `8858d49c5f` | 2026-10-10 |
| [astral-sh/uv-pre-commit](https://github.com/repolex-forx/astral-sh--uv-pre-commit) | 0.13.0 | 2026-10-10 |
| [pola-rs/geopolars](https://github.com/repolex-forx/pola-rs--geopolars) | `eebad68a3c` | 2026-10-10 |
| [tiangolo/uvicorn-gunicorn-fastapi-docker](https://github.com/repolex-forx/tiangolo--uvicorn-gunicorn-fastapi-docker) | `c93bb25d29` | 2026-10-10 |
| [astral-sh/ruff-pre-commit](https://github.com/repolex-forx/astral-sh--ruff-pre-commit) | v0.17.0 | 2026-10-10 |
| [tiangolo/uvicorn-gunicorn-starlette-docker](https://github.com/repolex-forx/tiangolo--uvicorn-gunicorn-starlette-docker) | `3c5484c582` | 2026-10-10 |
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
