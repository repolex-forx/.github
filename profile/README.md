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
| [pylint-dev/pylint](https://github.com/pylint-dev/pylint) | v3.0.2 | [view](https://github.com/repolex-forx/pylint-dev--pylint) | 2026-04-14 |
| [python-hyper/h2](https://github.com/python-hyper/h2) | v4.3.0 | [view](https://github.com/repolex-forx/python-hyper--h2) | 2026-04-14 |
| [babel/babel](https://github.com/babel/babel) | v8.0.0-alpha.4 | [view](https://github.com/repolex-forx/babel--babel) | 2026-04-14 |
| [python-hyper/brotlicffi](https://github.com/python-hyper/brotlicffi) | v1.2.0.1 | [view](https://github.com/repolex-forx/python-hyper--brotlicffi) | 2026-04-14 |
| [sverweij/dependency-cruiser](https://github.com/sverweij/dependency-cruiser) | v11.7.0 | [view](https://github.com/repolex-forx/sverweij--dependency-cruiser) | 2026-04-14 |
| [pylint-dev/pylint](https://github.com/pylint-dev/pylint) | v3.0.3 | [view](https://github.com/repolex-forx/pylint-dev--pylint) | 2026-04-14 |
| [rollup/rollup](https://github.com/rollup/rollup) | v4.27.0 | [view](https://github.com/repolex-forx/rollup--rollup) | 2026-04-14 |
| [eslint/eslint](https://github.com/eslint/eslint) | v8.46.0 | [view](https://github.com/repolex-forx/eslint--eslint) | 2026-04-14 |
| [pylint-dev/pylint](https://github.com/pylint-dev/pylint) | v3.0.4 | [view](https://github.com/repolex-forx/pylint-dev--pylint) | 2026-04-14 |
| [sverweij/dependency-cruiser](https://github.com/sverweij/dependency-cruiser) | v11.7.1 | [view](https://github.com/repolex-forx/sverweij--dependency-cruiser) | 2026-04-14 |
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
