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
| [testing-library/dom-testing-library](https://github.com/repolex-forx/testing-library--dom-testing-library) | v10.4.1 | 2026-09-17 |
| [facebook/react](https://github.com/repolex-forx/facebook--react) | v19.2.5 | 2026-09-17 |
| [tanstack/intent](https://github.com/repolex-forx/tanstack--intent) | release-2026-03-16-1953 | 2026-09-17 |
| [tailwindlabs/prettier-plugin-tailwindcss](https://github.com/repolex-forx/tailwindlabs--prettier-plugin-tailwindcss) | v0.7.2 | 2026-09-17 |
| [cypress-io/cypress](https://github.com/repolex-forx/cypress-io--cypress) | v6.4.0 | 2026-09-17 |
| [sindresorhus/eslint-plugin-unicorn](https://github.com/repolex-forx/sindresorhus--eslint-plugin-unicorn) | v64.0.0 | 2026-09-17 |
| [open-cli-tools/concurrently](https://github.com/repolex-forx/open-cli-tools--concurrently) | v9.2.1 | 2026-09-17 |
| [pygments/pygments](https://github.com/repolex-forx/pygments--pygments) | 1.6 | 2026-09-17 |
| [cypress-io/cypress](https://github.com/repolex-forx/cypress-io--cypress) | v6.5.0 | 2026-09-17 |
| [mrmlnc/fast-glob](https://github.com/repolex-forx/mrmlnc--fast-glob) | v3.1.0 | 2026-09-17 |
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
