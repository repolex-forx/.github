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
| [agronholm/aionursery](https://github.com/repolex-forx/agronholm--aionursery) | `c8f5636c65` | 2026-10-11 |
| [agronholm/dummyproject](https://github.com/repolex-forx/agronholm--dummyproject) | `91b440ff13` | 2026-10-11 |
| [agronholm/ep2018demo](https://github.com/repolex-forx/agronholm--ep2018demo) | `4dbda56eab` | 2026-10-11 |
| [agronholm/pyproject-flake8](https://github.com/repolex-forx/agronholm--pyproject-flake8) | `b340fbc92c` | 2026-10-11 |
| [pydantic/pydantic-core-feedstock](https://github.com/repolex-forx/pydantic--pydantic-core-feedstock) | `1f47ffb686` | 2026-10-11 |
| [pydantic/logfire-vercel-ai-demo](https://github.com/repolex-forx/pydantic--logfire-vercel-ai-demo) | `0623404cc3` | 2026-10-11 |
| [pydantic/pydantic-who](https://github.com/repolex-forx/pydantic--pydantic-who) | `b8e36eb767` | 2026-10-11 |
| [pydantic/logfire-claude-plugin](https://github.com/repolex-forx/pydantic--logfire-claude-plugin) | `3da608785d` | 2026-10-11 |
| [python-trio/ahip](https://github.com/repolex-forx/python-trio--ahip) | `a0085fd9a7` | 2026-10-11 |
| [python-trio/.github](https://github.com/repolex-forx/python-trio--.github) | `840f9da893` | 2026-10-11 |
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
