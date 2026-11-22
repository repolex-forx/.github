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
| [zopefoundation/ExtensionClass](https://github.com/repolex-forx/zopefoundation--ExtensionClass) | backups/zope2@96245 | 2026-11-22 |
| [jaraco/jaraco.context](https://github.com/repolex-forx/jaraco--jaraco.context) | v6.1.2 | 2026-11-22 |
| [jaraco/pytest-checkdocs](https://github.com/repolex-forx/jaraco--pytest-checkdocs) | v2.14.0 | 2026-11-22 |
| [Delgan/loguru](https://github.com/repolex-forx/Delgan--loguru) | 0.7.3 | 2026-11-22 |
| [jaraco/rst.linker](https://github.com/repolex-forx/jaraco--rst.linker) | v2.6.0 | 2026-11-22 |
| [akubera/bigdecimal-rs](https://github.com/repolex-forx/akubera--bigdecimal-rs) | v0.4.10 | 2026-11-22 |
| [zopefoundation/zope.tal](https://github.com/repolex-forx/zopefoundation--zope.tal) | backups/monolithic-zope3@75193 | 2026-11-22 |
| [davidhalter/parso](https://github.com/repolex-forx/davidhalter--parso) | v0.8.6 | 2026-11-22 |
| [sphinx-contrib/sphinx-lint](https://github.com/repolex-forx/sphinx-contrib--sphinx-lint) | v1.0.2 | 2026-11-22 |
| [tox-dev/pyproject-api](https://github.com/repolex-forx/tox-dev--pyproject-api) | 1.10.0 | 2026-11-22 |
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
