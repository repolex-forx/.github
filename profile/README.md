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
| [aio-libs/get-releasenote](https://github.com/repolex-forx/aio-libs--get-releasenote) | `ad89ff3bd6` | 2026-10-10 |
| [cherrypy/magicbus](https://github.com/repolex-forx/cherrypy--magicbus) | `030c66688f` | 2026-10-10 |
| [agronholm/apscheduler](https://github.com/repolex-forx/agronholm--apscheduler) | `a660860d84` | 2026-10-10 |
| [pallets-eco/flask-security](https://github.com/repolex-forx/pallets-eco--flask-security) | `4cb3a45c45` | 2026-10-10 |
| [pallets-eco/flask-debugtoolbar](https://github.com/repolex-forx/pallets-eco--flask-debugtoolbar) | `5751c9ddac` | 2026-10-10 |
| [tortoise/django-tortoise-objects](https://github.com/repolex-forx/tortoise--django-tortoise-objects) | `8d47497fed` | 2026-10-10 |
| [tortoise/asyncodbc](https://github.com/repolex-forx/tortoise--asyncodbc) | `efcfa715a2` | 2026-10-10 |
| [tortoise/tortoise-cli](https://github.com/repolex-forx/tortoise--tortoise-cli) | `f46c230048` | 2026-10-10 |
| [tortoise/aerich](https://github.com/repolex-forx/tortoise--aerich) | `6333068e09` | 2026-10-10 |
| [tortoise/pypika-tortoise](https://github.com/repolex-forx/tortoise--pypika-tortoise) | `e175c9c1a6` | 2026-10-10 |
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
