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
| [samuelcolvin/uqrl](https://github.com/repolex-forx/samuelcolvin--uqrl) | `e10907542e` | 2026-10-11 |
| [aio-libs/aio-libs.github.io](https://github.com/repolex-forx/aio-libs--aio-libs.github.io) | `9a757da589` | 2026-10-11 |
| [tiangolo/typer-cli](https://github.com/repolex-forx/tiangolo--typer-cli) | `36a49a4ec5` | 2026-10-11 |
| [tiangolo/poetry-version-plugin](https://github.com/repolex-forx/tiangolo--poetry-version-plugin) | `96835bf262` | 2026-10-11 |
| [pallets/website-2016](https://github.com/repolex-forx/pallets--website-2016) | `9f97f1ead3` | 2026-10-11 |
| [pallets/website](https://github.com/repolex-forx/pallets--website) | `ec1afc9789` | 2026-10-11 |
| [python-trio/exceptiongroup](https://github.com/repolex-forx/python-trio--exceptiongroup) | `dd8fe794d5` | 2026-10-11 |
| [python-trio/python-trio.github.io](https://github.com/repolex-forx/python-trio--python-trio.github.io) | `25fecb307a` | 2026-10-11 |
| [bottlepy/blog.bottlepy.org](https://github.com/repolex-forx/bottlepy--blog.bottlepy.org) | `409834c380` | 2026-10-11 |
| [python-poetry/test-fixture-vcs-repository](https://github.com/repolex-forx/python-poetry--test-fixture-vcs-repository) | `0be1215c90` | 2026-10-11 |
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
