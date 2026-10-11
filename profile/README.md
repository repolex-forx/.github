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
| [pallets-eco/wtforms-dateutil](https://github.com/repolex-forx/pallets-eco--wtforms-dateutil) | `fbd183d4fc` | 2026-10-10 |
| [pallets-eco/wtforms-appengine](https://github.com/repolex-forx/pallets-eco--wtforms-appengine) | `230da3db81` | 2026-10-10 |
| [jazzband/django-polymorphic](https://github.com/repolex-forx/jazzband--django-polymorphic) | `db86c0c0ca` | 2026-10-10 |
| [jazzband/django-simple-history](https://github.com/repolex-forx/jazzband--django-simple-history) | `e71cb9e054` | 2026-10-10 |
| [jazzband/django-rest-knox](https://github.com/repolex-forx/jazzband--django-rest-knox) | `c3522713e0` | 2026-10-10 |
| [jazzband/django-dbbackup](https://github.com/repolex-forx/jazzband--django-dbbackup) | `6714cd0122` | 2026-10-10 |
| [pallets-eco/flask-orjson](https://github.com/repolex-forx/pallets-eco--flask-orjson) | `4e9ee0e46d` | 2026-10-10 |
| [pallets-eco/flask-ujson](https://github.com/repolex-forx/pallets-eco--flask-ujson) | `1ee3a6489e` | 2026-10-10 |
| [encode/sentry-asgi](https://github.com/repolex-forx/encode--sentry-asgi) | `6d4c6353ad` | 2026-10-10 |
| [encode/requests-async](https://github.com/repolex-forx/encode--requests-async) | `1de1b948a0` | 2026-10-10 |
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
