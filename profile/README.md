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
| [jazzband/django-waffle](https://github.com/repolex-forx/jazzband--django-waffle) | `76f880d804` | 2026-10-10 |
| [scrapy/itemadapter](https://github.com/repolex-forx/scrapy--itemadapter) | `ef0b748c57` | 2026-10-10 |
| [scrapy/cssselect](https://github.com/repolex-forx/scrapy--cssselect) | `805705c5a2` | 2026-10-10 |
| [scrapy/parsel](https://github.com/repolex-forx/scrapy--parsel) | `8ee96b7239` | 2026-10-10 |
| [scrapy/w3lib](https://github.com/repolex-forx/scrapy--w3lib) | `ade4b62e55` | 2026-10-10 |
| [pytest-dev/pytest-rerunfailures](https://github.com/repolex-forx/pytest-dev--pytest-rerunfailures) | `01fd226bd5` | 2026-10-10 |
| [pytest-dev/pytest-print](https://github.com/repolex-forx/pytest-dev--pytest-print) | `514e2bcfc3` | 2026-10-10 |
| [pytest-dev/pytest-env](https://github.com/repolex-forx/pytest-dev--pytest-env) | `484cdaed62` | 2026-10-10 |
| [pytest-dev/execnet](https://github.com/repolex-forx/pytest-dev--execnet) | `5844b41f94` | 2026-10-10 |
| [pytest-dev/pluggy](https://github.com/repolex-forx/pytest-dev--pluggy) | `87f130aa18` | 2026-10-10 |
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
