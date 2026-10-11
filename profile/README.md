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
| [agronholm/python-sdk](https://github.com/repolex-forx/agronholm--python-sdk) | `0bcecffc4c` | 2026-10-11 |
| [agronholm/packaging](https://github.com/repolex-forx/agronholm--packaging) | `3e67fc775e` | 2026-10-11 |
| [agronholm/httpcore](https://github.com/repolex-forx/agronholm--httpcore) | `76f6e199b6` | 2026-10-11 |
| [samuelcolvin/num-bigint](https://github.com/repolex-forx/samuelcolvin--num-bigint) | `14ced94a43` | 2026-10-11 |
| [samuelcolvin/minicbor](https://github.com/repolex-forx/samuelcolvin--minicbor) | `620fa37031` | 2026-10-11 |
| [agronholm/prometheus-fastapi-instrumentator](https://github.com/repolex-forx/agronholm--prometheus-fastapi-instrumentator) | `18dbfd64f1` | 2026-10-11 |
| [agronholm/python-xmlsec](https://github.com/repolex-forx/agronholm--python-xmlsec) | `ebbc3f7346` | 2026-10-11 |
| [agronholm/tkreload](https://github.com/repolex-forx/agronholm--tkreload) | `2c7126b094` | 2026-10-11 |
| [agronholm/llama-cpp-binaries](https://github.com/repolex-forx/agronholm--llama-cpp-binaries) | `0356d5af3d` | 2026-10-11 |
| [agronholm/pep789-testsuite](https://github.com/repolex-forx/agronholm--pep789-testsuite) | `5f0c7df0ca` | 2026-10-11 |
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
