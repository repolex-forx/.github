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
| [tox-dev/pipdeptree](https://github.com/repolex-forx/tox-dev--pipdeptree) | 4.2.6 | 2026-10-10 |
| [agronholm/cbor2](https://github.com/repolex-forx/agronholm--cbor2) | `6dc0c6b426` | 2026-10-10 |
| [tox-dev/platformdirs](https://github.com/repolex-forx/tox-dev--platformdirs) | `b3174fdd4e` | 2026-10-10 |
| [agronholm/typeguard](https://github.com/repolex-forx/agronholm--typeguard) | `cb8cee7a17` | 2026-10-10 |
| [tox-dev/tox-uv](https://github.com/repolex-forx/tox-dev--tox-uv) | `808fc710f7` | 2026-10-10 |
| [samuelcolvin/pytest-pretty](https://github.com/repolex-forx/samuelcolvin--pytest-pretty) | v1.3.0 | 2026-10-10 |
| [tox-dev/pyproject-api](https://github.com/repolex-forx/tox-dev--pyproject-api) | 1.11.5 | 2026-10-10 |
| [tox-dev/tox-gh](https://github.com/repolex-forx/tox-dev--tox-gh) | `8f3f27176e` | 2026-10-10 |
| [tox-dev/pyproject-fmt](https://github.com/repolex-forx/tox-dev--pyproject-fmt) | v2.30.3 | 2026-10-10 |
| [encode/starlette](https://github.com/repolex-forx/encode--starlette) | `96d5023c55` | 2026-10-10 |
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
