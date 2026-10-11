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
| [samuelcolvin/spread](https://github.com/repolex-forx/samuelcolvin--spread) | `180cfaccbc` | 2026-10-10 |
| [samuelcolvin/nextcall](https://github.com/repolex-forx/samuelcolvin--nextcall) | `3ef572168c` | 2026-10-10 |
| [samuelcolvin/deckx](https://github.com/repolex-forx/samuelcolvin--deckx) | `ff0a0c4644` | 2026-10-10 |
| [cherrypy/cheroot](https://github.com/repolex-forx/cherrypy--cheroot) | `a6283c12ca` | 2026-10-10 |
| [aio-libs/aiohttp-theme](https://github.com/repolex-forx/aio-libs--aiohttp-theme) | `6bb6d4bbf4` | 2026-10-10 |
| [aio-libs/aiohttp-asyncmdnsresolver](https://github.com/repolex-forx/aio-libs--aiohttp-asyncmdnsresolver) | `238407713a` | 2026-10-10 |
| [aio-libs/aiofastnet](https://github.com/repolex-forx/aio-libs--aiofastnet) | `29bcb0f991` | 2026-10-10 |
| [aio-libs/aiosmtpd](https://github.com/repolex-forx/aio-libs--aiosmtpd) | `07e5f26b0c` | 2026-10-10 |
| [aio-libs/aiohttp-devtools](https://github.com/repolex-forx/aio-libs--aiohttp-devtools) | `5a5d4222c3` | 2026-10-10 |
| [aio-libs/aiokafka](https://github.com/repolex-forx/aio-libs--aiokafka) | `13a6400024` | 2026-10-10 |
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
