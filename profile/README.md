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
| [aio-libs/multidict](https://github.com/repolex-forx/aio-libs--multidict) | `c728ce1cf0` | 2026-10-10 |
| [aio-libs/yarl](https://github.com/repolex-forx/aio-libs--yarl) | `d0d6a37515` | 2026-10-10 |
| [aio-libs/aiohappyeyeballs](https://github.com/repolex-forx/aio-libs--aiohappyeyeballs) | `5dc56b90fa` | 2026-10-10 |
| [aio-libs/aiojobs](https://github.com/repolex-forx/aio-libs--aiojobs) | `154e3575c2` | 2026-10-10 |
| [aio-libs/async-lru](https://github.com/repolex-forx/aio-libs--async-lru) | `639c403a26` | 2026-10-10 |
| [aio-libs/aiosignal](https://github.com/repolex-forx/aio-libs--aiosignal) | `63b413b5c3` | 2026-10-10 |
| [aio-libs/propcache](https://github.com/repolex-forx/aio-libs--propcache) | `5fc239491c` | 2026-10-10 |
| [aio-libs/frozenlist](https://github.com/repolex-forx/aio-libs--frozenlist) | `fd523c1768` | 2026-10-10 |
| [aio-libs/aiodns](https://github.com/repolex-forx/aio-libs--aiodns) | `ff43a83ea5` | 2026-10-10 |
| [aio-libs/aiorwlock](https://github.com/repolex-forx/aio-libs--aiorwlock) | `420dd9dcc0` | 2026-10-10 |
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
