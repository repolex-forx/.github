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
| [pallets/flask-website](https://github.com/repolex-forx/pallets--flask-website) | `8b083412f9` | 2026-10-11 |
| [tiangolo/tiangolo.com](https://github.com/repolex-forx/tiangolo--tiangolo.com) | `e61748bd41` | 2026-10-11 |
| [tiangolo/dockerswarm.rocks](https://github.com/repolex-forx/tiangolo--dockerswarm.rocks) | `c504a4b34d` | 2026-10-11 |
| [tiangolo/meinheld-gunicorn-flask-docker](https://github.com/repolex-forx/tiangolo--meinheld-gunicorn-flask-docker) | `e871de6864` | 2026-10-11 |
| [agronholm/docker-vernemq](https://github.com/repolex-forx/agronholm--docker-vernemq) | `dca9e7ba5a` | 2026-10-11 |
| [agronholm/pythonfutures](https://github.com/repolex-forx/agronholm--pythonfutures) | `738e37148b` | 2026-10-11 |
| [pydantic/skills](https://github.com/repolex-forx/pydantic--skills) | `238d971026` | 2026-10-11 |
| [pydantic/thrust](https://github.com/repolex-forx/pydantic--thrust) | `8505b55a97` | 2026-10-11 |
| [pydantic/datafusion-functions-json](https://github.com/repolex-forx/pydantic--datafusion-functions-json) | `30e05810d7` | 2026-10-11 |
| [pydantic/datafusion-variant](https://github.com/repolex-forx/pydantic--datafusion-variant) | `9e1c846981` | 2026-10-11 |
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
