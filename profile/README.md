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
| [apache/logging-log4j2](https://github.com/apache/logging-log4j2) | log4j-2.0-beta8 | [view](https://github.com/repolex-forx/apache--logging-log4j2) | 2026-03-30 |
| [Jelly-RDF/jelly-jvm](https://github.com/Jelly-RDF/jelly-jvm) | v2.0.3 | [view](https://github.com/repolex-forx/Jelly-RDF--jelly-jvm) | 2026-03-30 |
| [sdispater/tomlkit](https://github.com/sdispater/tomlkit) | 0.12.0 | [view](https://github.com/repolex-forx/sdispater--tomlkit) | 2026-03-30 |
| [readthedocs/sphinx_rtd_theme](https://github.com/readthedocs/sphinx_rtd_theme) | 0.2.0 | [view](https://github.com/repolex-forx/readthedocs--sphinx_rtd_theme) | 2026-03-30 |
| [willmcgugan/rich](https://github.com/willmcgugan/rich) | v0.7.2 | [view](https://github.com/repolex-forx/willmcgugan--rich) | 2026-03-30 |
| [agronholm/anyio](https://github.com/agronholm/anyio) | 4.1.0 | [view](https://github.com/repolex-forx/agronholm--anyio) | 2026-03-30 |
| [Jelly-RDF/jelly-jvm](https://github.com/Jelly-RDF/jelly-jvm) | v2.0.2 | [view](https://github.com/repolex-forx/Jelly-RDF--jelly-jvm) | 2026-03-30 |
| [colinhacks/zod](https://github.com/colinhacks/zod) | v3.25.76 | [view](https://github.com/repolex-forx/colinhacks--zod) | 2026-03-30 |
| [sdispater/tomlkit](https://github.com/sdispater/tomlkit) | 0.11.8 | [view](https://github.com/repolex-forx/sdispater--tomlkit) | 2026-03-30 |
| [apache/logging-log4j2](https://github.com/apache/logging-log4j2) | log4j-2.0-beta7-rc2 | [view](https://github.com/repolex-forx/apache--logging-log4j2) | 2026-03-30 |
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
