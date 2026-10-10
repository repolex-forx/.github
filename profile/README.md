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
| [marshmallow-code/marshmallow](https://github.com/repolex-forx/marshmallow-code--marshmallow) | `d08471b178` | 2026-10-10 |
| [jazzband/pip-tools](https://github.com/repolex-forx/jazzband--pip-tools) | v7.6.2 | 2026-10-10 |
| [marshmallow-code/flask-smorest](https://github.com/repolex-forx/marshmallow-code--flask-smorest) | `3440f0d851` | 2026-10-10 |
| [marshmallow-code/apispec](https://github.com/repolex-forx/marshmallow-code--apispec) | `0b66a26b86` | 2026-10-10 |
| [marshmallow-code/webargs](https://github.com/repolex-forx/marshmallow-code--webargs) | `dd2bc37718` | 2026-10-10 |
| [marshmallow-code/marshmallow-sqlalchemy](https://github.com/repolex-forx/marshmallow-code--marshmallow-sqlalchemy) | `a04b4a8bf4` | 2026-10-10 |
| [jazzband/tablib](https://github.com/repolex-forx/jazzband--tablib) | `966876c76a` | 2026-10-10 |
| [marshmallow-code/flask-marshmallow](https://github.com/repolex-forx/marshmallow-code--flask-marshmallow) | `9a83bbc137` | 2026-10-10 |
| [marshmallow-code/marshmallow-oneofschema](https://github.com/repolex-forx/marshmallow-code--marshmallow-oneofschema) | `6b25e361b7` | 2026-10-10 |
| [marshmallow-code/apispec-webframeworks](https://github.com/repolex-forx/marshmallow-code--apispec-webframeworks) | `b03f02fe2f` | 2026-10-10 |
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
