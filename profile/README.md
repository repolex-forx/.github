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
| [mde/ejs](https://github.com/mde/ejs) | v5.0.1 | [view](https://github.com/repolex-forx/mde--ejs) | 2026-04-10 |
| [rollup/rollup](https://github.com/rollup/rollup) | v4.60.0 | [view](https://github.com/repolex-forx/rollup--rollup) | 2026-04-10 |
| [shouldjs/should.js](https://github.com/shouldjs/should.js) | 13.2.3 | [view](https://github.com/repolex-forx/shouldjs--should.js) | 2026-04-10 |
| [babel/babel](https://github.com/babel/babel) | v8.0.0-beta.4 | [view](https://github.com/repolex-forx/babel--babel) | 2026-04-10 |
| [microsoft/TypeScript](https://github.com/microsoft/TypeScript) | v6.0-beta | [view](https://github.com/repolex-forx/microsoft--TypeScript) | 2026-04-10 |
| [sverweij/dependency-cruiser](https://github.com/sverweij/dependency-cruiser) | v16.10.4 | [view](https://github.com/repolex-forx/sverweij--dependency-cruiser) | 2026-04-10 |
| [gotwarlost/istanbul](https://github.com/gotwarlost/istanbul) | v1.1.0-alpha.1 | [view](https://github.com/repolex-forx/gotwarlost--istanbul) | 2026-04-10 |
| [sindresorhus/merge-descriptors](https://github.com/sindresorhus/merge-descriptors) | v2.0.0 | [view](https://github.com/repolex-forx/sindresorhus--merge-descriptors) | 2026-04-10 |
| [DefinitelyTyped/DefinitelyTyped](https://github.com/DefinitelyTyped/DefinitelyTyped) | 0.1.450 | [view](https://github.com/repolex-forx/DefinitelyTyped--DefinitelyTyped) | 2026-04-10 |
| [vitest-dev/vitest](https://github.com/vitest-dev/vitest) | v4.1.2 | [view](https://github.com/repolex-forx/vitest-dev--vitest) | 2026-04-10 |
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
