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
| [fastapi/fastapi](https://github.com/repolex-forx/fastapi--fastapi) | 0.135.3 | 2026-09-20 |
| [bigcat88/pillow_heif](https://github.com/repolex-forx/bigcat88--pillow_heif) | v0.1.3 | 2026-09-20 |
| [jd/tenacity](https://github.com/repolex-forx/jd--tenacity) | 4.6.1 | 2026-09-20 |
| [jpadilla/pyjwt](https://github.com/repolex-forx/jpadilla--pyjwt) | 2.0.0a2 | 2026-09-20 |
| [urllib3/urllib3](https://github.com/repolex-forx/urllib3--urllib3) | 1.26.8 | 2026-09-20 |
| [Kludex/uvicorn](https://github.com/repolex-forx/Kludex--uvicorn) | 0.20.0 | 2026-09-20 |
| [yaml/pyyaml](https://github.com/repolex-forx/yaml--pyyaml) | 3.07 | 2026-09-20 |
| [Python-Markdown/markdown](https://github.com/repolex-forx/Python-Markdown--markdown) | 2.5-final | 2026-09-20 |
| [cpburnz/python-pathspec](https://github.com/repolex-forx/cpburnz--python-pathspec) | v0.10.3 | 2026-09-20 |
| [Textualize/rich](https://github.com/repolex-forx/Textualize--rich) | v12.3.0 | 2026-09-20 |
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
