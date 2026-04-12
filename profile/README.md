# repolex-forx

**Source code as a knowledge graph.** Every repo here contains RDF graph data parsed from an open source project — abstract syntax trees, dependency graphs, LSP-enriched semantic analysis, git history, and more — all queryable with SPARQL.

## [forx-index](https://github.com/repolex-forx/forx-index) — The Catalog

The **[forx-index](https://github.com/repolex-forx/forx-index)** repo is the central catalog of everything we've parsed. It contains JSON-LD manifests that form a lightweight knowledge graph: repositories, parsed commits, and the web of dependencies between projects. Load them into any RDF tool and query with SPARQL.

## Getting Started

Install [lexq](https://github.com/repolex-ai/lexq), the query tool for repolex knowledge graphs:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

Download a parsed repo:

```bash
lexq download repolex-ai/lexq
```

**lexq is designed to be used by LLMs in a terminal.** Start your favorite AI assistant and ask it to use lexq. It handles the SPARQL — you just ask questions in plain English.

```
"Claude, can you check the --help menu of lexq"
"Hermes, can you use the lexq tool to download someorg/somerepo"
"What classes are defined in this codebase?"
"Show me the dependency graph"
```

## Recently Parsed

<!-- AUTO-UPDATED BY FORX - DO NOT EDIT BELOW -->
| Source | Tag | Data | Parsed |
|--------|-----|------|--------|
| [rollup/rollup](https://github.com/rollup/rollup) | v4.34.4 | [view](https://github.com/repolex-forx/rollup--rollup) | 2026-04-12 |
| [hmrc/service-manager](https://github.com/hmrc/service-manager) | 0.0.19 | [view](https://github.com/repolex-forx/hmrc--service-manager) | 2026-04-12 |
| [sverweij/dependency-cruiser](https://github.com/sverweij/dependency-cruiser) | v12.10.1 | [view](https://github.com/repolex-forx/sverweij--dependency-cruiser) | 2026-04-12 |
| [aws/aws-sdk-ruby](https://github.com/aws/aws-sdk-ruby) | v2.11.632 | [view](https://github.com/repolex-forx/aws--aws-sdk-ruby) | 2026-04-12 |
| [MatthewGilbert/mapping](https://github.com/MatthewGilbert/mapping) | v0.1.5 | [view](https://github.com/repolex-forx/MatthewGilbert--mapping) | 2026-04-12 |
| [davidfraser/WSGIUtils](https://github.com/davidfraser/WSGIUtils) | v0.7.1 | [view](https://github.com/repolex-forx/davidfraser--WSGIUtils) | 2026-04-12 |
| [eslint/eslint](https://github.com/eslint/eslint) | v9.0.0 | [view](https://github.com/repolex-forx/eslint--eslint) | 2026-04-12 |
| [swc-project/swc](https://github.com/swc-project/swc) | v1.15.20-nightly-20260302.1 | [view](https://github.com/repolex-forx/swc-project--swc) | 2026-04-12 |
| [macournoyer/thin](https://github.com/macournoyer/thin) | v1.7.0 | [view](https://github.com/repolex-forx/macournoyer--thin) | 2026-04-12 |
| [PyTables/PyTables](https://github.com/PyTables/PyTables) | v3.11.0 | [view](https://github.com/repolex-forx/PyTables--PyTables) | 2026-04-12 |
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

*Powered by [repolex](https://repolex.ai) · Orchestrated by [forx](https://github.com/repolex-ai/forx) · Queried with [lexq](https://github.com/repolex-ai/lexq)*
