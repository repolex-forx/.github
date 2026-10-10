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
| [agronholm/sqlacodegen](https://github.com/repolex-forx/agronholm--sqlacodegen) | `c7eef1f533` | 2026-10-10 |
| [tox-dev/python-discovery](https://github.com/repolex-forx/tox-dev--python-discovery) | 1.6.2 | 2026-10-10 |
| [mkdocstrings/griffe-pydantic](https://github.com/repolex-forx/mkdocstrings--griffe-pydantic) | 1.3.2 | 2026-10-10 |
| [mkdocstrings/griffe-typingdoc](https://github.com/repolex-forx/mkdocstrings--griffe-typingdoc) | 0.3.2 | 2026-10-10 |
| [agronholm/fetchling](https://github.com/repolex-forx/agronholm--fetchling) | `0389e6766c` | 2026-10-10 |
| [mkdocstrings/griffe-inherited-docstrings](https://github.com/repolex-forx/mkdocstrings--griffe-inherited-docstrings) | 1.1.4 | 2026-10-10 |
| [tox-dev/tox-toml-fmt](https://github.com/repolex-forx/tox-dev--tox-toml-fmt) | v1.11.1 | 2026-10-10 |
| [tox-dev/pre-commit-uv](https://github.com/repolex-forx/tox-dev--pre-commit-uv) | `edc4fbece3` | 2026-10-10 |
| [tox-dev/tox-ini-fmt](https://github.com/repolex-forx/tox-dev--tox-ini-fmt) | `862ac086ad` | 2026-10-10 |
| [tox-dev/devpi-process](https://github.com/repolex-forx/tox-dev--devpi-process) | `b4d09adc26` | 2026-10-10 |
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
