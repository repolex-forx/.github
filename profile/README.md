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
| [agronholm/trio-typing](https://github.com/repolex-forx/agronholm--trio-typing) | `2b182b7d78` | 2026-10-11 |
| [agronholm/modoboa-dmarc](https://github.com/repolex-forx/agronholm--modoboa-dmarc) | `47572ed820` | 2026-10-11 |
| [agronholm/redis-specifications](https://github.com/repolex-forx/agronholm--redis-specifications) | `7bd21a0765` | 2026-10-11 |
| [pydantic/pydantic-handlebars](https://github.com/repolex-forx/pydantic--pydantic-handlebars) | `9812951da4` | 2026-10-11 |
| [pydantic/logfire-auth-action](https://github.com/repolex-forx/pydantic--logfire-auth-action) | `5bc43913fd` | 2026-10-11 |
| [pydantic/speedate](https://github.com/repolex-forx/pydantic--speedate) | `a68ce8660d` | 2026-10-11 |
| [pydantic/claude-code-logfire-plugin](https://github.com/repolex-forx/pydantic--claude-code-logfire-plugin) | `0f1b1172a4` | 2026-10-11 |
| [pydantic/monty-helm-chart](https://github.com/repolex-forx/pydantic--monty-helm-chart) | `2ef57eac25` | 2026-10-11 |
| [pydantic/strict-no-cover](https://github.com/repolex-forx/pydantic--strict-no-cover) | `6c644106e0` | 2026-10-11 |
| [pydantic/.github](https://github.com/repolex-forx/pydantic--.github) | `31399f9034` | 2026-10-11 |
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
