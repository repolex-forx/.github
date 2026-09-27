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
| [asimov-platform/asimov-chrome-extesion](https://github.com/repolex-forx/asimov-platform--asimov-chrome-extesion) | master | 2026-09-27 |
| [asimov-platform/asimov.sh](https://github.com/repolex-forx/asimov-platform--asimov.sh) | master | 2026-09-27 |
| [asimov-platform/package-metrics](https://github.com/repolex-forx/asimov-platform--package-metrics) | master | 2026-09-27 |
| [asimov-platform/kestra-asimov-plugin](https://github.com/repolex-forx/asimov-platform--kestra-asimov-plugin) | master | 2026-09-27 |
| [asimov-protocol/asimov-graph-widget](https://github.com/repolex-forx/asimov-protocol--asimov-graph-widget) | main | 2026-09-27 |
| [asimov-platform/actions](https://github.com/repolex-forx/asimov-platform--actions) | master | 2026-09-27 |
| [asimov-platform/scoop-bucket](https://github.com/repolex-forx/asimov-platform--scoop-bucket) | master | 2026-09-27 |
| [materialsproject/fireworks](https://github.com/repolex-forx/materialsproject--fireworks) | v2.1.2 | 2026-09-27 |
| [hhatto/autopep8](https://github.com/repolex-forx/hhatto--autopep8) | ver1.2.2 | 2026-09-27 |
| [sysid/sse-starlette](https://github.com/repolex-forx/sysid--sse-starlette) | 0.2.1 | 2026-09-27 |
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
