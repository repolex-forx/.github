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
| [asimov-platform/prefect-asimov](https://github.com/asimov-platform/prefect-asimov) | 0.0.0 | [view](https://github.com/repolex-forx/asimov-platform--prefect-asimov) | 2026-04-15 |
| [rollup/rollup](https://github.com/rollup/rollup) | v4.16.0 | [view](https://github.com/repolex-forx/rollup--rollup) | 2026-04-15 |
| [asimov-platform/llama-index-asimov](https://github.com/asimov-platform/llama-index-asimov) | 0.0.2 | [view](https://github.com/repolex-forx/asimov-platform--llama-index-asimov) | 2026-04-15 |
| [eslint/eslint](https://github.com/eslint/eslint) | v8.22.0 | [view](https://github.com/repolex-forx/eslint--eslint) | 2026-04-15 |
| [asimov-platform/langchain-asimov](https://github.com/asimov-platform/langchain-asimov) | 0.0.4 | [view](https://github.com/repolex-forx/asimov-platform--langchain-asimov) | 2026-04-15 |
| [bcgit/bc-java](https://github.com/bcgit/bc-java) | r1rv82 | [view](https://github.com/repolex-forx/bcgit--bc-java) | 2026-04-15 |
| [asimov-platform/asimov-universe.py](https://github.com/asimov-platform/asimov-universe.py) | 25.0.0.dev0 | [view](https://github.com/repolex-forx/asimov-platform--asimov-universe.py) | 2026-04-15 |
| [rollup/rollup](https://github.com/rollup/rollup) | v4.16.1 | [view](https://github.com/repolex-forx/rollup--rollup) | 2026-04-15 |
| [asimov-platform/asimov-universe.rb](https://github.com/asimov-platform/asimov-universe.rb) | 25.0.0.dev.0 | [view](https://github.com/repolex-forx/asimov-platform--asimov-universe.rb) | 2026-04-15 |
| [asimov-platform/asimov-dataset-cli](https://github.com/asimov-platform/asimov-dataset-cli) | 25.0.0-dev.6 | [view](https://github.com/repolex-forx/asimov-platform--asimov-dataset-cli) | 2026-04-15 |
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
