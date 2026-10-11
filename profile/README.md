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
| [cherrypy/oauth-client-example](https://github.com/repolex-forx/cherrypy--oauth-client-example) | `84d882ad60` | 2026-10-10 |
| [cherrypy/zappa-cherrypy](https://github.com/repolex-forx/cherrypy--zappa-cherrypy) | `ae2e6da5e7` | 2026-10-10 |
| [psf/strategy](https://github.com/repolex-forx/psf--strategy) | `dc011d930c` | 2026-10-10 |
| [pallets/actions](https://github.com/repolex-forx/pallets--actions) | `3255f16f0e` | 2026-10-10 |
| [agronholm/asyncbis](https://github.com/repolex-forx/agronholm--asyncbis) | `592cc0b683` | 2026-10-10 |
| [python-trio/snekomatic](https://github.com/repolex-forx/python-trio--snekomatic) | `43e8e6d260` | 2026-10-10 |
| [python-trio/trio-owfs](https://github.com/repolex-forx/python-trio--trio-owfs) | `694a7d8926` | 2026-10-10 |
| [python-trio/cookiecutter-trio](https://github.com/repolex-forx/python-trio--cookiecutter-trio) | `17f560a4aa` | 2026-10-10 |
| [bottlepy/bottlepy.org](https://github.com/repolex-forx/bottlepy--bottlepy.org) | `28d8d09387` | 2026-10-10 |
| [bottlepy/bottle-mongo](https://github.com/repolex-forx/bottlepy--bottle-mongo) | `5f359898fb` | 2026-10-10 |
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
