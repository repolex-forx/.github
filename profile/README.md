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
| [pallets/.github](https://github.com/repolex-forx/pallets--.github) | `06702680f5` | 2026-10-11 |
| [pypa/setuptools-issue-900](https://github.com/repolex-forx/pypa--setuptools-issue-900) | `4025ff7c93` | 2026-10-11 |
| [pypa/python-manylinux-demo](https://github.com/repolex-forx/pypa--python-manylinux-demo) | `8247a02cc6` | 2026-10-11 |
| [pypa/pypa.io](https://github.com/repolex-forx/pypa--pypa.io) | `ed988856b2` | 2026-10-11 |
| [pypa/browntruck](https://github.com/repolex-forx/pypa--browntruck) | `8c6db1bb2d` | 2026-10-11 |
| [pypa/pipfile](https://github.com/repolex-forx/pypa--pipfile) | `4706d2cbd3` | 2026-10-11 |
| [pypa/sample-namespace-packages](https://github.com/repolex-forx/pypa--sample-namespace-packages) | `134414420e` | 2026-10-11 |
| [pypa/.github](https://github.com/repolex-forx/pypa--.github) | `d2d8249a55` | 2026-10-11 |
| [tiangolo/python-multipart](https://github.com/repolex-forx/tiangolo--python-multipart) | `d3d16dae4b` | 2026-10-11 |
| [tiangolo/.github](https://github.com/repolex-forx/tiangolo--.github) | `d2f19734f3` | 2026-10-11 |
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
