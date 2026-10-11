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
| [encode/dashboard](https://github.com/repolex-forx/encode--dashboard) | `a184d749a3` | 2026-10-11 |
| [samuelcolvin/datafusion-sql-udfs](https://github.com/repolex-forx/samuelcolvin--datafusion-sql-udfs) | `d173e9ba6e` | 2026-10-11 |
| [samuelcolvin/cloudkv](https://github.com/repolex-forx/samuelcolvin--cloudkv) | `c5cb4dec9f` | 2026-10-11 |
| [agronholm/unasync](https://github.com/repolex-forx/agronholm--unasync) | `3d7a369509` | 2026-10-11 |
| [agronholm/httpx-ws](https://github.com/repolex-forx/agronholm--httpx-ws) | `c9efdda0ce` | 2026-10-11 |
| [agronholm/httpx-sse](https://github.com/repolex-forx/agronholm--httpx-sse) | `643938c805` | 2026-10-11 |
| [agronholm/sniffio](https://github.com/repolex-forx/agronholm--sniffio) | `95190ad580` | 2026-10-11 |
| [pallets-eco/flask-stache](https://github.com/repolex-forx/pallets-eco--flask-stache) | `b3bbd326bd` | 2026-10-11 |
| [pallets-eco/flask-api-examples](https://github.com/repolex-forx/pallets-eco--flask-api-examples) | `837ba43230` | 2026-10-11 |
| [pallets-eco/click-bash4.2-completion](https://github.com/repolex-forx/pallets-eco--click-bash4.2-completion) | `b0fcf111ad` | 2026-10-11 |
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
