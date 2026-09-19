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
| [urllib3/urllib3](https://github.com/repolex-forx/urllib3--urllib3) | 1.26.13 | 2026-09-19 |
| [yaml/pyyaml](https://github.com/repolex-forx/yaml--pyyaml) | 3.12 | 2026-09-19 |
| [jd/tenacity](https://github.com/repolex-forx/jd--tenacity) | 4.12.0 | 2026-09-19 |
| [pypa/packaging](https://github.com/repolex-forx/pypa--packaging) | 14.4 | 2026-09-19 |
| [pallets/jinja](https://github.com/repolex-forx/pallets--jinja) | 2.7 | 2026-09-19 |
| [jpadilla/pyjwt](https://github.com/repolex-forx/jpadilla--pyjwt) | 2.5.0 | 2026-09-19 |
| [theskumar/python-dotenv](https://github.com/repolex-forx/theskumar--python-dotenv) | v0.2.0 | 2026-09-19 |
| [Textualize/rich](https://github.com/repolex-forx/Textualize--rich) | v12.5.1 | 2026-09-19 |
| [giampaolo/psutil](https://github.com/repolex-forx/giampaolo--psutil) | v5.9.2 | 2026-09-19 |
| [Kludex/uvicorn](https://github.com/repolex-forx/Kludex--uvicorn) | 0.24.0.post1 | 2026-09-19 |
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
