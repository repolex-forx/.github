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
| Data Source | Tag | Parsed |
|-------------|-----|--------|
| [eslint/rewrite](https://github.com/repolex-forx/eslint--rewrite) | plugin-kit-v0.7.1 | 2026-09-17 |
| [firecrawl/anydoc](https://github.com/repolex-forx/firecrawl--anydoc) | v0.2.2 | 2026-09-17 |
| [openjdk/jdk](https://github.com/repolex-forx/openjdk--jdk) | jdk-26+15 | 2026-09-17 |
| [repolex-ai/git-lex](https://github.com/repolex-forx/repolex-ai--git-lex) | `3a993b9535` | 2026-09-17 |
| [repolex-ai/rlex](https://github.com/repolex-forx/repolex-ai--rlex) | `77a6a8c614` | 2026-09-17 |
| [blitz-js/superjson](https://github.com/repolex-forx/blitz-js--superjson) | v2.2.5 | 2026-09-17 |
| [repolex-ai/git-lex](https://github.com/repolex-forx/repolex-ai--git-lex) | `5e836b878b` | 2026-09-17 |
| [bcomnes/npm-run-all2](https://github.com/repolex-forx/bcomnes--npm-run-all2) | v8.1.0-beta.0 | 2026-09-17 |
| [repolex-ai/pan](https://github.com/repolex-forx/repolex-ai--pan) | `d05b12a33f` | 2026-09-17 |
| [repolex-ai/pan](https://github.com/repolex-forx/repolex-ai--pan) | `79d0c16a26` | 2026-09-17 |
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
