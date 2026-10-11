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
| [pypa/pipx](https://github.com/repolex-forx/pypa--pipx) | 1.17.13 | 2026-10-11 |
| [pypa/setuptools-scm](https://github.com/repolex-forx/pypa--setuptools-scm) | `6146a26063` | 2026-10-11 |
| [python-trio/flake8-async](https://github.com/repolex-forx/python-trio--flake8-async) | 26.8.1 | 2026-10-11 |
| [pypa/pip-audit](https://github.com/repolex-forx/pypa--pip-audit) | `828e77a4d4` | 2026-10-11 |
| [pypa/wheel](https://github.com/repolex-forx/pypa--wheel) | `4ae6d07d38` | 2026-10-11 |
| [python-trio/trio-asyncio](https://github.com/repolex-forx/python-trio--trio-asyncio) | `4b0074272e` | 2026-10-11 |
| [python-trio/trio-websocket](https://github.com/repolex-forx/python-trio--trio-websocket) | `e828e54cfc` | 2026-10-11 |
| [python-trio/hypothesis-trio](https://github.com/repolex-forx/python-trio--hypothesis-trio) | `84250f4e35` | 2026-10-11 |
| [python-trio/sphinxcontrib-trio](https://github.com/repolex-forx/python-trio--sphinxcontrib-trio) | `cfd44c1658` | 2026-10-11 |
| [python-trio/pytest-trio](https://github.com/repolex-forx/python-trio--pytest-trio) | `f0168502bc` | 2026-10-11 |
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
