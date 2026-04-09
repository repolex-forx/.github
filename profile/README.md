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
| [typescript-eslint/typescript-eslint](https://github.com/typescript-eslint/typescript-eslint) | v8.58.1 | [view](https://github.com/repolex-forx/typescript-eslint--typescript-eslint) | 2026-04-09 |
| [sphinx-doc/sphinx](https://github.com/sphinx-doc/sphinx) | v9.1.0 | [view](https://github.com/repolex-forx/sphinx-doc--sphinx) | 2026-04-09 |
| [benmosher/eslint-plugin-import](https://github.com/benmosher/eslint-plugin-import) | v2.32.0 | [view](https://github.com/repolex-forx/benmosher--eslint-plugin-import) | 2026-04-09 |
| [okonet/lint-staged](https://github.com/okonet/lint-staged) | v16.4.0 | [view](https://github.com/repolex-forx/okonet--lint-staged) | 2026-04-09 |
| [rollup/plugins](https://github.com/rollup/plugins) | yaml-v4.1.2 | [view](https://github.com/repolex-forx/rollup--plugins) | 2026-04-09 |
| [eslint/eslint](https://github.com/eslint/eslint) | v10.2.0 | [view](https://github.com/repolex-forx/eslint--eslint) | 2026-04-09 |
| [DefinitelyTyped/DefinitelyTyped](https://github.com/DefinitelyTyped/DefinitelyTyped) | 0.1.450 | [view](https://github.com/repolex-forx/DefinitelyTyped--DefinitelyTyped) | 2026-04-09 |
| [pandas-dev/pandas](https://github.com/pandas-dev/pandas) | v3.1.0.dev0 | [view](https://github.com/repolex-forx/pandas-dev--pandas) | 2026-04-09 |
| [pyca/cryptography](https://github.com/pyca/cryptography) | 46.0.7 | [view](https://github.com/repolex-forx/pyca--cryptography) | 2026-04-09 |
| [sverweij/dependency-cruiser](https://github.com/sverweij/dependency-cruiser) | v17.3.10 | [view](https://github.com/repolex-forx/sverweij--dependency-cruiser) | 2026-04-09 |
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
