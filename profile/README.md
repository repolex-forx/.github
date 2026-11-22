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
| [eliben/pycparser](https://github.com/repolex-forx/eliben--pycparser) | release_2.01 | 2026-11-22 |
| [businho/pytest-ruff](https://github.com/repolex-forx/businho--pytest-ruff) | v0.5 | 2026-11-22 |
| [zopefoundation/zope.tales](https://github.com/repolex-forx/zopefoundation--zope.tales) | backups/nikhil_n-py25@78055 | 2026-11-22 |
| [zopefoundation/zope.location](https://github.com/repolex-forx/zopefoundation--zope.location) | 6.0 | 2026-11-22 |
| [zopefoundation/zope.event](https://github.com/repolex-forx/zopefoundation--zope.event) | 6.1 | 2026-11-22 |
| [rbarrois/python-semanticversion](https://github.com/repolex-forx/rbarrois--python-semanticversion) | v2.6.0 | 2026-11-22 |
| [explosion/preshed](https://github.com/repolex-forx/explosion--preshed) | v4.0.0 | 2026-11-22 |
| [explosion/catalogue](https://github.com/repolex-forx/explosion--catalogue) | v2.1.0 | 2026-11-22 |
| [pytest-dev/pytest-env](https://github.com/repolex-forx/pytest-dev--pytest-env) | 1.6.0 | 2026-11-22 |
| [jamielennox/requests-mock](https://github.com/repolex-forx/jamielennox--requests-mock) | 1.12.1 | 2026-11-22 |
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
