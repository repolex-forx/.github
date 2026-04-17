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
| [bigcat88/pillow_heif](https://github.com/bigcat88/pillow_heif) | v1.3.0 | [view](https://github.com/repolex-forx/bigcat88--pillow_heif) | 2026-04-17 |
| [openjdk/jdk](https://github.com/openjdk/jdk) | jdk-27+17 | [view](https://github.com/repolex-forx/openjdk--jdk) | 2026-04-17 |
| [anthropics/anthropic-sdk-csharp](https://github.com/anthropics/anthropic-sdk-csharp) | v10.1.1 | [view](https://github.com/repolex-forx/anthropics--anthropic-sdk-csharp) | 2026-04-17 |
| [praw-dev/prawcore](https://github.com/praw-dev/prawcore) | v3.0.2 | [view](https://github.com/repolex-forx/praw-dev--prawcore) | 2026-04-17 |
| [eslint/eslint](https://github.com/eslint/eslint) | v8.4.1 | [view](https://github.com/repolex-forx/eslint--eslint) | 2026-04-17 |
| [cypress-io/cypress](https://github.com/cypress-io/cypress) | v15.13.0 | [view](https://github.com/repolex-forx/cypress-io--cypress) | 2026-04-17 |
| [anthropics/anthropic-sdk-java](https://github.com/anthropics/anthropic-sdk-java) | v2.16.1 | [view](https://github.com/repolex-forx/anthropics--anthropic-sdk-java) | 2026-04-17 |
| [deedy5/duckduckgo_search](https://github.com/deedy5/duckduckgo_search) | v9.12.1 | [view](https://github.com/repolex-forx/deedy5--duckduckgo_search) | 2026-04-17 |
| [macournoyer/thin](https://github.com/macournoyer/thin) | v1.2.1 | [view](https://github.com/repolex-forx/macournoyer--thin) | 2026-04-17 |
| [swc-project/swc](https://github.com/swc-project/swc) | v1.15.12-nightly-20260222.1 | [view](https://github.com/repolex-forx/swc-project--swc) | 2026-04-17 |
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
