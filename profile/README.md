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
| [mhammond/pywin32](https://github.com/repolex-forx/mhammond--pywin32) | py3k-merge-complete | 2026-09-15 |
| [webpack/webpack](https://github.com/repolex-forx/webpack--webpack) | v5.25.1 | 2026-09-15 |
| [huggingface/transformers](https://github.com/repolex-forx/huggingface--transformers) | v4.55.1 | 2026-09-15 |
| [coveragepy/coveragepy](https://github.com/repolex-forx/coveragepy--coveragepy) | coverage-5.6b1 | 2026-09-15 |
| [Kludex/uvicorn](https://github.com/repolex-forx/Kludex--uvicorn) | 0.44.0 | 2026-09-15 |
| [apache/arrow](https://github.com/repolex-forx/apache--arrow) | r-12.0.1.1 | 2026-09-15 |
| [apple/foundationdb](https://github.com/repolex-forx/apple--foundationdb) | snowflake-71.3.0-rc3 | 2026-09-15 |
| [cypress-io/cypress](https://github.com/repolex-forx/cypress-io--cypress) | v8.7.0 | 2026-09-15 |
| [python/tzdata](https://github.com/repolex-forx/python--tzdata) | 2026.1 | 2026-09-15 |
| [babel/babel](https://github.com/repolex-forx/babel--babel) | v7.15.4 | 2026-09-15 |
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
