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
| [anthropics/anthropic-sdk-csharp](https://github.com/anthropics/anthropic-sdk-csharp) | v10.4.0 | [view](https://github.com/repolex-forx/anthropics--anthropic-sdk-csharp) | 2026-04-16 |
| [macournoyer/thin](https://github.com/macournoyer/thin) | v1.2.7 | [view](https://github.com/repolex-forx/macournoyer--thin) | 2026-04-16 |
| [eslint/eslint](https://github.com/eslint/eslint) | v8.10.0 | [view](https://github.com/repolex-forx/eslint--eslint) | 2026-04-16 |
| [swc-project/swc](https://github.com/swc-project/swc) | v1.15.16-nightly-20260226.1 | [view](https://github.com/repolex-forx/swc-project--swc) | 2026-04-16 |
| [anthropics/anthropic-sdk-java](https://github.com/anthropics/anthropic-sdk-java) | v2.21.0 | [view](https://github.com/repolex-forx/anthropics--anthropic-sdk-java) | 2026-04-16 |
| [eslint/eslint](https://github.com/eslint/eslint) | v8.11.0 | [view](https://github.com/repolex-forx/eslint--eslint) | 2026-04-16 |
| [anthropics/buffa](https://github.com/anthropics/buffa) | v0.3.0 | [view](https://github.com/repolex-forx/anthropics--buffa) | 2026-04-16 |
| [anthropics/connect-rust](https://github.com/anthropics/connect-rust) | v0.3.2 | [view](https://github.com/repolex-forx/anthropics--connect-rust) | 2026-04-16 |
| [anthropics/healthcare](https://github.com/anthropics/healthcare) | v1.0.0 | [view](https://github.com/repolex-forx/anthropics--healthcare) | 2026-04-16 |
| [eslint/eslint](https://github.com/eslint/eslint) | v8.12.0 | [view](https://github.com/repolex-forx/eslint--eslint) | 2026-04-16 |
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
