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
| [sqlalchemy/sqlalchemy](https://github.com/sqlalchemy/sqlalchemy) | rel_0_1_0 | [view](https://github.com/repolex-forx/sqlalchemy--sqlalchemy) | 2026-03-29 |
| [sqlalchemy/sqlalchemy](https://github.com/sqlalchemy/sqlalchemy) | origin | [view](https://github.com/repolex-forx/sqlalchemy--sqlalchemy) | 2026-03-29 |
| [lodash/lodash](https://github.com/lodash/lodash) | 4.5.1 | [view](https://github.com/repolex-forx/lodash--lodash) | 2026-03-29 |
| [lodash/lodash](https://github.com/lodash/lodash) | 4.4.0 | [view](https://github.com/repolex-forx/lodash--lodash) | 2026-03-29 |
| [lodash/lodash](https://github.com/lodash/lodash) | 4.3.0 | [view](https://github.com/repolex-forx/lodash--lodash) | 2026-03-29 |
| [lodash/lodash](https://github.com/lodash/lodash) | 4.2.1 | [view](https://github.com/repolex-forx/lodash--lodash) | 2026-03-29 |
| [lodash/lodash](https://github.com/lodash/lodash) | 4.1.0 | [view](https://github.com/repolex-forx/lodash--lodash) | 2026-03-29 |
| [lodash/lodash](https://github.com/lodash/lodash) | 4.0.1 | [view](https://github.com/repolex-forx/lodash--lodash) | 2026-03-29 |
| [expressjs/express](https://github.com/expressjs/express) | 2.3.12 | [view](https://github.com/repolex-forx/expressjs--express) | 2026-03-29 |
| [expressjs/express](https://github.com/expressjs/express) | 2.2.2 | [view](https://github.com/repolex-forx/expressjs--express) | 2026-03-29 |
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
