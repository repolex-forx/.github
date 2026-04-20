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
| [praw-dev/praw](https://github.com/praw-dev/praw) | v4.3.0 | [view](https://github.com/repolex-forx/praw-dev--praw) | 2026-04-20 |
| [apple/swift-numerics](https://github.com/apple/swift-numerics) | 1.1.1 | [view](https://github.com/repolex-forx/apple--swift-numerics) | 2026-04-20 |
| [cypress-io/cypress](https://github.com/cypress-io/cypress) | v14.3.0 | [view](https://github.com/repolex-forx/cypress-io--cypress) | 2026-04-20 |
| [anthropics/anthropic-sdk-csharp](https://github.com/anthropics/anthropic-sdk-csharp) | Vertex-v0.1.0 | [view](https://github.com/repolex-forx/anthropics--anthropic-sdk-csharp) | 2026-04-20 |
| [openjdk/jdk](https://github.com/openjdk/jdk) | jdk-27+15 | [view](https://github.com/repolex-forx/openjdk--jdk) | 2026-04-20 |
| [webpack/webpack](https://github.com/webpack/webpack) | v5.102.1 | [view](https://github.com/repolex-forx/webpack--webpack) | 2026-04-20 |
| [apple/foundationdb](https://github.com/apple/foundationdb) | snowflake-71.3.6-rc1 | [view](https://github.com/repolex-forx/apple--foundationdb) | 2026-04-20 |
| [webpack/webpack](https://github.com/webpack/webpack) | v5.103.0 | [view](https://github.com/repolex-forx/webpack--webpack) | 2026-04-20 |
| [microsoft/TypeScript](https://github.com/microsoft/TypeScript) | v5.4.2 | [view](https://github.com/repolex-forx/microsoft--TypeScript) | 2026-04-20 |
| [apple/swift-nio](https://github.com/apple/swift-nio) | 2.97.1 | [view](https://github.com/repolex-forx/apple--swift-nio) | 2026-04-20 |
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
