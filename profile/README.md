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
| [python-trio/unasync](https://github.com/repolex-forx/python-trio--unasync) | `3a0a3bee2a` | 2026-10-11 |
| [pypa/flit](https://github.com/repolex-forx/pypa--flit) | 4.1.0 | 2026-10-10 |
| [litestar-org/pytest-databases](https://github.com/repolex-forx/litestar-org--pytest-databases) | `bbefed5477` | 2026-10-10 |
| [pypa/abi3audit](https://github.com/repolex-forx/pypa--abi3audit) | `a33c6e0fe6` | 2026-10-10 |
| [litestar-org/type-lens](https://github.com/repolex-forx/litestar-org--type-lens) | `58fccf85bd` | 2026-10-10 |
| [pypa/pyproject-metadata](https://github.com/repolex-forx/pypa--pyproject-metadata) | `c78be647e3` | 2026-10-10 |
| [pypa/installer](https://github.com/repolex-forx/pypa--installer) | `ba622422bc` | 2026-10-10 |
| [pypa/trove-classifiers](https://github.com/repolex-forx/pypa--trove-classifiers) | 2026.9.21.13 | 2026-10-10 |
| [pypa/dependency-groups](https://github.com/repolex-forx/pypa--dependency-groups) | `facfeaf7f8` | 2026-10-10 |
| [pypa/pyproject-hooks](https://github.com/repolex-forx/pypa--pyproject-hooks) | v1.3.3 | 2026-10-10 |
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
