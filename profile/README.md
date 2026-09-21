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
| [repolex-ai/ravel](https://github.com/repolex-forx/repolex-ai--ravel) | `e897e6be7f` | 2026-09-21 |
| [python-websockets/websockets](https://github.com/repolex-forx/python-websockets--websockets) | 11.0.3 | 2026-09-21 |
| [pallets-eco/croniter](https://github.com/repolex-forx/pallets-eco--croniter) | 5.0.1 | 2026-09-21 |
| [urllib3/urllib3](https://github.com/repolex-forx/urllib3--urllib3) | 1.25.9 | 2026-09-21 |
| [Python-Markdown/markdown](https://github.com/repolex-forx/Python-Markdown--markdown) | 2.0-rc1 | 2026-09-21 |
| [jd/tenacity](https://github.com/repolex-forx/jd--tenacity) | 3.2.1 | 2026-09-21 |
| [prompt-toolkit/python-prompt-toolkit](https://github.com/repolex-forx/prompt-toolkit--python-prompt-toolkit) | 3.0.27 | 2026-09-21 |
| [Kludex/uvicorn](https://github.com/repolex-forx/Kludex--uvicorn) | 0.16.0 | 2026-09-21 |
| [Preston-Landers/concurrent-log-handler](https://github.com/repolex-forx/Preston-Landers--concurrent-log-handler) | 0.9.27 | 2026-09-21 |
| [firecrawl/anydoc](https://github.com/repolex-forx/firecrawl--anydoc) | v0.1.9 | 2026-09-21 |
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
