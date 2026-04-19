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
| [openjdk/jdk](https://github.com/openjdk/jdk) | jdk-27+15 | [view](https://github.com/repolex-forx/openjdk--jdk) | 2026-04-19 |
| [webpack/webpack-cli](https://github.com/webpack/webpack-cli) | v4.0.0-beta.9 | [view](https://github.com/repolex-forx/webpack--webpack-cli) | 2026-04-19 |
| [snide/wyrm](https://github.com/snide/wyrm) | 1.0.9 | [view](https://github.com/repolex-forx/snide--wyrm) | 2026-04-19 |
| [webpack/webpack](https://github.com/webpack/webpack) | v5.105.2 | [view](https://github.com/repolex-forx/webpack--webpack) | 2026-04-19 |
| [Fridus/webpack-watch-files-plugin](https://github.com/Fridus/webpack-watch-files-plugin) | v1.2.1 | [view](https://github.com/repolex-forx/Fridus--webpack-watch-files-plugin) | 2026-04-19 |
| [antlr/antlr4](https://github.com/antlr/antlr4) | runtime/Go/antlr/v4/v4.11.0 | [view](https://github.com/repolex-forx/antlr--antlr4) | 2026-04-19 |
| [jquery/jquery](https://github.com/jquery/jquery) | 4.0.0-beta.2 | [view](https://github.com/repolex-forx/jquery--jquery) | 2026-04-19 |
| [1337programming/webpack-shell-plugin](https://github.com/1337programming/webpack-shell-plugin) | 0.3.2 | [view](https://github.com/repolex-forx/1337programming--webpack-shell-plugin) | 2026-04-19 |
| [macournoyer/thin](https://github.com/macournoyer/thin) | v0.7.0 | [view](https://github.com/repolex-forx/macournoyer--thin) | 2026-04-19 |
| [survivejs/webpack-merge](https://github.com/survivejs/webpack-merge) | v6.0.1 | [view](https://github.com/repolex-forx/survivejs--webpack-merge) | 2026-04-19 |
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
