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
| [fastapi/sqlmodel](https://github.com/repolex-forx/fastapi--sqlmodel) | 0.0.48 | 2026-10-10 |
| [fastapi/typer](https://github.com/repolex-forx/fastapi--typer) | 0.27.3 | 2026-10-10 |
| [aio-libs/aioftp](https://github.com/repolex-forx/aio-libs--aioftp) | `11d8dd916d` | 2026-10-10 |
| [encode/mkdocs](https://github.com/repolex-forx/encode--mkdocs) | `c03ca093c7` | 2026-10-10 |
| [fastapi/fastapi-cli](https://github.com/repolex-forx/fastapi--fastapi-cli) | `093be9ca19` | 2026-10-10 |
| [fastapi/asyncer](https://github.com/repolex-forx/fastapi--asyncer) | `de024c755c` | 2026-10-10 |
| [aio-libs/sort-all](https://github.com/repolex-forx/aio-libs--sort-all) | `0caa98df16` | 2026-10-10 |
| [fastapi/annotated-doc](https://github.com/repolex-forx/fastapi--annotated-doc) | `e6e7324ff5` | 2026-10-10 |
| [aio-libs/aiohttp-apischema](https://github.com/repolex-forx/aio-libs--aiohttp-apischema) | `25d10ce623` | 2026-10-10 |
| [fastapi/fastapi-new](https://github.com/repolex-forx/fastapi--fastapi-new) | `6902db31d1` | 2026-10-10 |
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
