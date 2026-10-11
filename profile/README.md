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
| [pydantic/datafusion-table-providers](https://github.com/repolex-forx/pydantic--datafusion-table-providers) | `2064c60b06` | 2026-10-11 |
| [pydantic/ai-chat-ui](https://github.com/repolex-forx/pydantic--ai-chat-ui) | `8014d57f8f` | 2026-10-11 |
| [pydantic/provider-upjet-logfire](https://github.com/repolex-forx/pydantic--provider-upjet-logfire) | `5cf470dcbd` | 2026-10-11 |
| [pydantic/tracing-opentelemetry-instrumentation-sdk](https://github.com/repolex-forx/pydantic--tracing-opentelemetry-instrumentation-sdk) | `08ef24d98c` | 2026-10-11 |
| [agronholm/asks](https://github.com/repolex-forx/agronholm--asks) | `e3f2b097fa` | 2026-10-11 |
| [pydantic/datafusion-federation](https://github.com/repolex-forx/pydantic--datafusion-federation) | `36b0d03a08` | 2026-10-11 |
| [pydantic/tracing-opentelemetry](https://github.com/repolex-forx/pydantic--tracing-opentelemetry) | `13f7ca2c0a` | 2026-10-11 |
| [agronholm/docker-atlassian-confluence](https://github.com/repolex-forx/agronholm--docker-atlassian-confluence) | `573b616b9a` | 2026-10-11 |
| [agronholm/action-general-autotag](https://github.com/repolex-forx/agronholm--action-general-autotag) | `7d2ae9fb80` | 2026-10-11 |
| [agronholm/pusher-http-python](https://github.com/repolex-forx/agronholm--pusher-http-python) | `57dd636c13` | 2026-10-11 |
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
