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
| [jazzband/django-superform](https://github.com/repolex-forx/jazzband--django-superform) | `92b4d9ea2c` | 2026-10-10 |
| [jazzband/django-simple-menu](https://github.com/repolex-forx/jazzband--django-simple-menu) | v2.1.4 | 2026-10-10 |
| [jazzband/django-downloadview](https://github.com/repolex-forx/jazzband--django-downloadview) | `ff0aeb909f` | 2026-10-10 |
| [jazzband/django-eav2](https://github.com/repolex-forx/jazzband--django-eav2) | `3cc8e8fcc0` | 2026-10-10 |
| [jazzband/django-avatar](https://github.com/repolex-forx/jazzband--django-avatar) | v9.0.0 | 2026-10-10 |
| [jazzband/jsonmodels](https://github.com/repolex-forx/jazzband--jsonmodels) | `0770de5380` | 2026-10-10 |
| [jazzband/django-axes](https://github.com/repolex-forx/jazzband--django-axes) | 8.3.2 | 2026-10-10 |
| [jazzband/django-push-notifications](https://github.com/repolex-forx/jazzband--django-push-notifications) | `613e7e9448` | 2026-10-10 |
| [jazzband/django-sortedm2m](https://github.com/repolex-forx/jazzband--django-sortedm2m) | `6c9285dfb8` | 2026-10-10 |
| [jazzband/dj-database-url](https://github.com/repolex-forx/jazzband--dj-database-url) | `5656563adb` | 2026-10-10 |
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
