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
| [pydantic/pydantic-extra-types](https://github.com/repolex-forx/pydantic--pydantic-extra-types) | `27cca0ebf5` | 2026-10-10 |
| [litestar-org/litestar-saq](https://github.com/repolex-forx/litestar-org--litestar-saq) | `95619b5f74` | 2026-10-10 |
| [litestar-org/polyfactory](https://github.com/repolex-forx/litestar-org--polyfactory) | `6234cf0af8` | 2026-10-10 |
| [litestar-org/litestar-asyncpg](https://github.com/repolex-forx/litestar-org--litestar-asyncpg) | `23fd93d733` | 2026-10-10 |
| [pydantic/pytest-examples](https://github.com/repolex-forx/pydantic--pytest-examples) | `df945f7043` | 2026-10-10 |
| [litestar-org/litestar-email](https://github.com/repolex-forx/litestar-org--litestar-email) | `270f3d370e` | 2026-10-10 |
| [litestar-org/litestar-htmx](https://github.com/repolex-forx/litestar-org--litestar-htmx) | `e5c4e2fcdb` | 2026-10-10 |
| [jazzband/django-hosts](https://github.com/repolex-forx/jazzband--django-hosts) | `ef571d4d39` | 2026-10-10 |
| [jazzband/django-voting](https://github.com/repolex-forx/jazzband--django-voting) | `5721fb6647` | 2026-10-10 |
| [jazzband/django-fsm-log](https://github.com/repolex-forx/jazzband--django-fsm-log) | `27d6437d08` | 2026-10-10 |
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
