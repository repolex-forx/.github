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
| [agronholm/graphql-core](https://github.com/repolex-forx/agronholm--graphql-core) | `fa8f9b509d` | 2026-10-11 |
| [pydantic/logfire-js](https://github.com/repolex-forx/pydantic--logfire-js) | `95eca241f7` | 2026-10-11 |
| [tiangolo/odmantic](https://github.com/repolex-forx/tiangolo--odmantic) | `a99a2588cd` | 2026-10-11 |
| [agronholm/websockets](https://github.com/repolex-forx/agronholm--websockets) | `1c8032acb1` | 2026-10-11 |
| [agronholm/aiokafka](https://github.com/repolex-forx/agronholm--aiokafka) | `1855cdefa8` | 2026-10-11 |
| [agronholm/aiobotocore](https://github.com/repolex-forx/agronholm--aiobotocore) | `29b97290dc` | 2026-10-11 |
| [agronholm/llama-cpp-python](https://github.com/repolex-forx/agronholm--llama-cpp-python) | `803924b02c` | 2026-10-11 |
| [tiangolo/uvicorn](https://github.com/repolex-forx/tiangolo--uvicorn) | `3dd0d44445` | 2026-10-11 |
| [pydantic/logfire-helm-chart](https://github.com/repolex-forx/pydantic--logfire-helm-chart) | `5ac371653e` | 2026-10-11 |
| [pydantic/perses-shared](https://github.com/repolex-forx/pydantic--perses-shared) | `bcb5f0209a` | 2026-10-11 |
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
