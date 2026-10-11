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
| [celery/bootsteps](https://github.com/repolex-forx/celery--bootsteps) | `f2e788edb1` | 2026-10-10 |
| [celery/case](https://github.com/repolex-forx/celery--case) | `e0ba875515` | 2026-10-10 |
| [celery/jumpstarter](https://github.com/repolex-forx/celery--jumpstarter) | `43dbf34e5e` | 2026-10-10 |
| [celery/sphinx_celery](https://github.com/repolex-forx/celery--sphinx_celery) | `715a76ddbb` | 2026-10-10 |
| [celery/django-celery-results](https://github.com/repolex-forx/celery--django-celery-results) | `7f41f97b43` | 2026-10-10 |
| [celery/py-amqp](https://github.com/repolex-forx/celery--py-amqp) | `15fb95f7a8` | 2026-10-10 |
| [celery/django-celery-beat](https://github.com/repolex-forx/celery--django-celery-beat) | `dfe16f2edc` | 2026-10-10 |
| [celery/vine](https://github.com/repolex-forx/celery--vine) | `ef33151cbb` | 2026-10-10 |
| [celery/pytest-celery](https://github.com/repolex-forx/celery--pytest-celery) | `fdbdccf378` | 2026-10-10 |
| [celery/billiard](https://github.com/repolex-forx/celery--billiard) | `40a82b1533` | 2026-10-10 |
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
