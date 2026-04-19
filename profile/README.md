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
| [openjdk/jdk](https://github.com/openjdk/jdk) | jdk-27+16 | [view](https://github.com/repolex-forx/openjdk--jdk) | 2026-04-19 |
| [macournoyer/thin](https://github.com/macournoyer/thin) | v0.8.2 | [view](https://github.com/repolex-forx/macournoyer--thin) | 2026-04-19 |
| [apache/arrow](https://github.com/apache/arrow) | r-16.1.0 | [view](https://github.com/repolex-forx/apache--arrow) | 2026-04-19 |
| [microsoft/TypeScript](https://github.com/microsoft/TypeScript) | v5.4.5 | [view](https://github.com/repolex-forx/microsoft--TypeScript) | 2026-04-19 |
| [webpack-contrib/mini-css-extract-plugin](https://github.com/webpack-contrib/mini-css-extract-plugin) | v2.10.2 | [view](https://github.com/repolex-forx/webpack-contrib--mini-css-extract-plugin) | 2026-04-18 |
| [jquery/jquery](https://github.com/jquery/jquery) | 4.0.0-rc.2 | [view](https://github.com/repolex-forx/jquery--jquery) | 2026-04-18 |
| [betsol/lato-font](https://github.com/betsol/lato-font) | v3.0.0 | [view](https://github.com/repolex-forx/betsol--lato-font) | 2026-04-18 |
| [webpack-contrib/imports-loader](https://github.com/webpack-contrib/imports-loader) | v5.0.0 | [view](https://github.com/repolex-forx/webpack-contrib--imports-loader) | 2026-04-18 |
| [webpack-contrib/file-loader](https://github.com/webpack-contrib/file-loader) | v5.0.2 | [view](https://github.com/repolex-forx/webpack-contrib--file-loader) | 2026-04-18 |
| [anthropics/anthropic-sdk-csharp](https://github.com/anthropics/anthropic-sdk-csharp) | v0.1.0 | [view](https://github.com/repolex-forx/anthropics--anthropic-sdk-csharp) | 2026-04-18 |
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
