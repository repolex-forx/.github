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
| [encode/httpx](https://github.com/encode/httpx) | 0.28.1 | [view](https://github.com/repolex-forx/encode--httpx) | 2026-03-30 |
| [Jelly-RDF/jelly-jvm](https://github.com/Jelly-RDF/jelly-jvm) | v0.11.4 | [view](https://github.com/repolex-forx/Jelly-RDF--jelly-jvm) | 2026-03-30 |
| [bobfang1992/pytomlpp](https://github.com/bobfang1992/pytomlpp) | 0.3.4 | [view](https://github.com/repolex-forx/bobfang1992--pytomlpp) | 2026-03-30 |
| [bobfang1992/pytomlpp](https://github.com/bobfang1992/pytomlpp) | 0.3.3 | [view](https://github.com/repolex-forx/bobfang1992--pytomlpp) | 2026-03-30 |
| [apache/jena](https://github.com/apache/jena) | jena-2.11.0 | [view](https://github.com/repolex-forx/apache--jena) | 2026-03-30 |
| [junit-team/junit4](https://github.com/junit-team/junit4) | r4.13-beta-2 | [view](https://github.com/repolex-forx/junit-team--junit4) | 2026-03-30 |
| [bobfang1992/pytomlpp](https://github.com/bobfang1992/pytomlpp) | 0.3.2 | [view](https://github.com/repolex-forx/bobfang1992--pytomlpp) | 2026-03-30 |
| [sqlalchemy/sqlalchemy](https://github.com/sqlalchemy/sqlalchemy) | rel_0_2_4 | [view](https://github.com/repolex-forx/sqlalchemy--sqlalchemy) | 2026-03-30 |
| [apache/logging-log4j2](https://github.com/apache/logging-log4j2) | log4j-2.0-beta3-rc2 | [view](https://github.com/repolex-forx/apache--logging-log4j2) | 2026-03-30 |
| [junit-team/junit4](https://github.com/junit-team/junit4) | r4.13-beta-1 | [view](https://github.com/repolex-forx/junit-team--junit4) | 2026-03-30 |
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
