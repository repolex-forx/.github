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
| [aio-libs/aiomonitor](https://github.com/repolex-forx/aio-libs--aiomonitor) | `73de9b00b2` | 2026-10-10 |
| [aio-libs/aiohttp-remotes](https://github.com/repolex-forx/aio-libs--aiohttp-remotes) | `7aa3efd7ae` | 2026-10-10 |
| [aio-libs/aiozipkin](https://github.com/repolex-forx/aio-libs--aiozipkin) | `978e7cde37` | 2026-10-10 |
| [aio-libs/aiohttp-security](https://github.com/repolex-forx/aio-libs--aiohttp-security) | `b9378635fd` | 2026-10-10 |
| [aio-libs/aiodocker](https://github.com/repolex-forx/aio-libs--aiodocker) | `178d8a0fc9` | 2026-10-10 |
| [aio-libs/aiohttp-client-middlewares](https://github.com/repolex-forx/aio-libs--aiohttp-client-middlewares) | `33cb914393` | 2026-10-10 |
| [aio-libs/aiohttp-sse](https://github.com/repolex-forx/aio-libs--aiohttp-sse) | `a674b62f76` | 2026-10-10 |
| [aio-libs/pytest-aiohttp](https://github.com/repolex-forx/aio-libs--pytest-aiohttp) | `5f01c5f3c5` | 2026-10-10 |
| [aio-libs/aiohttp-jinja2](https://github.com/repolex-forx/aio-libs--aiohttp-jinja2) | `e45cd67400` | 2026-10-10 |
| [aio-libs/aiohttp-cors](https://github.com/repolex-forx/aio-libs--aiohttp-cors) | `041b99b3ea` | 2026-10-10 |
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
