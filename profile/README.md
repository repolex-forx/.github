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
| [anthropics/anthropic-sdk-csharp](https://github.com/anthropics/anthropic-sdk-csharp) | Vertex-v0.2.1 | [view](https://github.com/repolex-forx/anthropics--anthropic-sdk-csharp) | 2026-04-23 |
| [anthropics/anthropic-sdk-csharp](https://github.com/anthropics/anthropic-sdk-csharp) | Bedrock-v0.1.2 | [view](https://github.com/repolex-forx/anthropics--anthropic-sdk-csharp) | 2026-04-23 |
| [ruby/ruby](https://github.com/ruby/ruby) | v4.0.2 | [view](https://github.com/repolex-forx/ruby--ruby) | 2026-04-23 |
| [jquery/jquery](https://github.com/jquery/jquery) | 3.1.0 | [view](https://github.com/repolex-forx/jquery--jquery) | 2026-04-23 |
| [webpack/webpack](https://github.com/webpack/webpack) | v5.84.0 | [view](https://github.com/repolex-forx/webpack--webpack) | 2026-04-23 |
| [jquery/jquery](https://github.com/jquery/jquery) | 3.2.1 | [view](https://github.com/repolex-forx/jquery--jquery) | 2026-04-23 |
| [anthropics/anthropic-sdk-csharp](https://github.com/anthropics/anthropic-sdk-csharp) | Vertex-v0.0.1 | [view](https://github.com/repolex-forx/anthropics--anthropic-sdk-csharp) | 2026-04-23 |
| [webpack/webpack](https://github.com/webpack/webpack) | v5.84.1 | [view](https://github.com/repolex-forx/webpack--webpack) | 2026-04-23 |
| [ratatui/ratatui](https://github.com/ratatui/ratatui) | v0.30.0-alpha.1 | [view](https://github.com/repolex-forx/ratatui--ratatui) | 2026-04-23 |
| [pygments/pygments](https://github.com/pygments/pygments) | 2.19.1 | [view](https://github.com/repolex-forx/pygments--pygments) | 2026-04-23 |
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
