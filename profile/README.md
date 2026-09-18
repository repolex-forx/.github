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
| [openai/openai-python](https://github.com/repolex-forx/openai--openai-python) | v2.29.0 | 2026-09-18 |
| [giampaolo/psutil](https://github.com/repolex-forx/giampaolo--psutil) | v7.1.3 | 2026-09-18 |
| [Textualize/rich](https://github.com/repolex-forx/Textualize--rich) | v14.0.0 | 2026-09-18 |
| [python/tzdata](https://github.com/repolex-forx/python--tzdata) | 2025.2 | 2026-09-18 |
| [NousResearch/hermes-agent](https://github.com/repolex-forx/NousResearch--hermes-agent) | v2026.9.14 | 2026-09-18 |
| [python-pillow/Pillow](https://github.com/repolex-forx/python-pillow--Pillow) | 12.1.0 | 2026-09-18 |
| [bigcat88/pillow_heif](https://github.com/repolex-forx/bigcat88--pillow_heif) | v1.1.0 | 2026-09-18 |
| [snowballstem/snowball](https://github.com/repolex-forx/snowballstem--snowball) | v2.1.0 | 2026-09-18 |
| [pypa/packaging](https://github.com/repolex-forx/pypa--packaging) | 25.0 | 2026-09-18 |
| [yaml/pyyaml](https://github.com/repolex-forx/yaml--pyyaml) | 6.0 | 2026-09-18 |
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
