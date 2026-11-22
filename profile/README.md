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
| [explosion/weasel](https://github.com/repolex-forx/explosion--weasel) | v0.4.1 | 2026-11-22 |
| [zopefoundation/zope.browsermenu](https://github.com/repolex-forx/zopefoundation--zope.browsermenu) | 6.0 | 2026-11-22 |
| [zopefoundation/zExceptions](https://github.com/repolex-forx/zopefoundation--zExceptions) | 6.0 | 2026-11-22 |
| [python-trio/pytest-trio](https://github.com/repolex-forx/python-trio--pytest-trio) | v0.8.0 | 2026-11-22 |
| [dtolnay/serde-untagged](https://github.com/repolex-forx/dtolnay--serde-untagged) | 0.1.9 | 2026-11-22 |
| [Peternator7/strum](https://github.com/repolex-forx/Peternator7--strum) | v0.28.0 | 2026-11-22 |
| [sphinx-doc/sphinxcontrib-serializinghtml](https://github.com/repolex-forx/sphinx-doc--sphinxcontrib-serializinghtml) | 2.0.0 | 2026-11-22 |
| [shibukawa/imagesize_py](https://github.com/repolex-forx/shibukawa--imagesize_py) | 2.0.0 | 2026-11-22 |
| [sphinx-doc/sphinxcontrib-htmlhelp](https://github.com/repolex-forx/sphinx-doc--sphinxcontrib-htmlhelp) | 2.1.0 | 2026-11-22 |
| [lixxu/flask-paginate](https://github.com/repolex-forx/lixxu--flask-paginate) | v2024.4.12 | 2026-11-22 |
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
