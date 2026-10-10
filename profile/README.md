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
| [jazzband/geojson](https://github.com/repolex-forx/jazzband--geojson) | `82055e8679` | 2026-10-10 |
| [jazzband/django-formtools](https://github.com/repolex-forx/jazzband--django-formtools) | `472d9887be` | 2026-10-10 |
| [jazzband/django-two-factor-auth](https://github.com/repolex-forx/jazzband--django-two-factor-auth) | `a718bc7b82` | 2026-10-10 |
| [jazzband/django-auditlog](https://github.com/repolex-forx/jazzband--django-auditlog) | `607000d814` | 2026-10-10 |
| [jazzband/django-widget-tweaks](https://github.com/repolex-forx/jazzband--django-widget-tweaks) | `483b594c87` | 2026-10-10 |
| [jazzband/django-pipeline](https://github.com/repolex-forx/jazzband--django-pipeline) | 4.1.0 | 2026-10-10 |
| [jazzband/django-model-utils](https://github.com/repolex-forx/jazzband--django-model-utils) | `9d2edee6d6` | 2026-10-10 |
| [jazzband/django-taggit](https://github.com/repolex-forx/jazzband--django-taggit) | `e7a53796c9` | 2026-10-10 |
| [jazzband/django-redis](https://github.com/repolex-forx/jazzband--django-redis) | `d646a755e1` | 2026-10-10 |
| [jazzband/djangorestframework-simplejwt](https://github.com/repolex-forx/jazzband--djangorestframework-simplejwt) | `a7cb077ea0` | 2026-10-10 |
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
