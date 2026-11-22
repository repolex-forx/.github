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
| [mkdocstrings/autorefs](https://github.com/repolex-forx/mkdocstrings--autorefs) | 1.4.4 | 2026-11-22 |
| [rayon-rs/either](https://github.com/repolex-forx/rayon-rs--either) | 1.15.0 | 2026-11-22 |
| [zopefoundation/zope.browserresource](https://github.com/repolex-forx/zopefoundation--zope.browserresource) | backups/mgedmin-etag-support@115668 | 2026-11-22 |
| [explosion/confection](https://github.com/repolex-forx/explosion--confection) | v0.1.5 | 2026-11-22 |
| [jaraco/jaraco.classes](https://github.com/repolex-forx/jaraco--jaraco.classes) | v3.4.0 | 2026-11-22 |
| [google/python-subprocess32](https://github.com/repolex-forx/google--python-subprocess32) | test_travis_deploy_006 | 2026-11-22 |
| [python-distro/distro](https://github.com/repolex-forx/python-distro--distro) | v1.9.0 | 2026-11-22 |
| [oprypin/mkdocs-literate-nav](https://github.com/repolex-forx/oprypin--mkdocs-literate-nav) | v0.6.3 | 2026-11-22 |
| [sphinx-doc/sphinxcontrib-websupport](https://github.com/repolex-forx/sphinx-doc--sphinxcontrib-websupport) | 2.0.0 | 2026-11-22 |
| [pytest-dev/pytest-timeout](https://github.com/repolex-forx/pytest-dev--pytest-timeout) | 2.4.0 | 2026-11-22 |
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
