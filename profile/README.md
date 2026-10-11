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
| [pytest-dev/py](https://github.com/repolex-forx/pytest-dev--py) | `6b219734fc` | 2026-10-11 |
| [cherrypy/cherrypy](https://github.com/repolex-forx/cherrypy--cherrypy) | `1f75bc9eed` | 2026-10-11 |
| [pydantic/files.pydantic.run](https://github.com/repolex-forx/pydantic--files.pydantic.run) | `6254f2cfe9` | 2026-10-11 |
| [pydantic/pydantic-media-kit](https://github.com/repolex-forx/pydantic--pydantic-media-kit) | `e84e2728e1` | 2026-10-11 |
| [samuelcolvin/cf-run-python](https://github.com/repolex-forx/samuelcolvin--cf-run-python) | `d7db0200c1` | 2026-10-11 |
| [samuelcolvin/logfire_django_demo](https://github.com/repolex-forx/samuelcolvin--logfire_django_demo) | `0e985073ce` | 2026-10-11 |
| [samuelcolvin/datafusion-id-experiment](https://github.com/repolex-forx/samuelcolvin--datafusion-id-experiment) | `e31ed01e44` | 2026-10-11 |
| [samuelcolvin/quick-strings](https://github.com/repolex-forx/samuelcolvin--quick-strings) | `2e427ddeef` | 2026-10-11 |
| [samuelcolvin/RustModel](https://github.com/repolex-forx/samuelcolvin--RustModel) | `df61fe03a3` | 2026-10-11 |
| [samuelcolvin/redis_ping](https://github.com/repolex-forx/samuelcolvin--redis_ping) | `eaae9c32ec` | 2026-10-11 |
| [litestar-org/litestar.dev](https://github.com/repolex-forx/litestar-org--litestar.dev) | `9e5f55dffc` | 2026-10-11 |
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
