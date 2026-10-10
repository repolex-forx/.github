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
| [jazzband/django-hosts](https://github.com/repolex-forx/jazzband--django-hosts) | `ef571d4d39` | 2026-10-10 |
| [jazzband/django-voting](https://github.com/repolex-forx/jazzband--django-voting) | `5721fb6647` | 2026-10-10 |
| [jazzband/django-fsm-log](https://github.com/repolex-forx/jazzband--django-fsm-log) | `27d6437d08` | 2026-10-10 |
| [jazzband/django-invitations](https://github.com/repolex-forx/jazzband--django-invitations) | `378b2f59ef` | 2026-10-10 |
| [jazzband/icalevents](https://github.com/repolex-forx/jazzband--icalevents) | `9794b29e9d` | 2026-10-10 |
| [jazzband/sorl-thumbnail](https://github.com/repolex-forx/jazzband--sorl-thumbnail) | `2c0b550cd7` | 2026-10-10 |
| [jazzband/django-categories](https://github.com/repolex-forx/jazzband--django-categories) | `3964ba4b78` | 2026-10-10 |
| [jazzband/django-user-sessions](https://github.com/repolex-forx/jazzband--django-user-sessions) | `527f91e83e` | 2026-10-10 |
| [jazzband/geojson](https://github.com/repolex-forx/jazzband--geojson) | `82055e8679` | 2026-10-10 |
| [jazzband/django-formtools](https://github.com/repolex-forx/jazzband--django-formtools) | `472d9887be` | 2026-10-10 |
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
