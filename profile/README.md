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
| [jaraco/portend](https://github.com/jaraco/portend) | v3.2.1 | [view](https://github.com/repolex-forx/jaraco--portend) | 2026-04-13 |
| [sverweij/dependency-cruiser](https://github.com/sverweij/dependency-cruiser) | v12.5.0-beta-1 | [view](https://github.com/repolex-forx/sverweij--dependency-cruiser) | 2026-04-13 |
| [microsoft/TypeScript](https://github.com/microsoft/TypeScript) | v5.9.2 | [view](https://github.com/repolex-forx/microsoft--TypeScript) | 2026-04-13 |
| [kennethreitz/clint](https://github.com/kennethreitz/clint) | v0.5.1 | [view](https://github.com/repolex-forx/kennethreitz--clint) | 2026-04-13 |
| [rollup/rollup](https://github.com/rollup/rollup) | v4.32.0 | [view](https://github.com/repolex-forx/rollup--rollup) | 2026-04-13 |
| [pypa/readme_renderer](https://github.com/pypa/readme_renderer) | 44.0 | [view](https://github.com/repolex-forx/pypa--readme_renderer) | 2026-04-13 |
| [sverweij/dependency-cruiser](https://github.com/sverweij/dependency-cruiser) | v12.5.0-beta-2 | [view](https://github.com/repolex-forx/sverweij--dependency-cruiser) | 2026-04-13 |
| [swc-project/swc](https://github.com/swc-project/swc) | v1.15.20-nightly-20260302.1 | [view](https://github.com/repolex-forx/swc-project--swc) | 2026-04-13 |
| [zopefoundation/Zope](https://github.com/zopefoundation/Zope) | philikon-aq-checkpoint | [view](https://github.com/repolex-forx/zopefoundation--Zope) | 2026-04-13 |
| [dchest/pyblake2](https://github.com/dchest/pyblake2) | v1.1.1 | [view](https://github.com/repolex-forx/dchest--pyblake2) | 2026-04-13 |
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
