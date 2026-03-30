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
| [Textualize/rich](https://github.com/Textualize/rich) | v5.0.0 | [view](https://github.com/repolex-forx/Textualize--rich) | 2026-03-30 |
| [anthropics/claude-agent-sdk-python](https://github.com/anthropics/claude-agent-sdk-python) | v0.1.36 | [view](https://github.com/repolex-forx/anthropics--claude-agent-sdk-python) | 2026-03-30 |
| [python/typing_extensions](https://github.com/python/typing_extensions) | 4.14.0rc1 | [view](https://github.com/repolex-forx/python--typing_extensions) | 2026-03-30 |
| [pixeltable/pixeltable](https://github.com/pixeltable/pixeltable) | v0.2.19 | [view](https://github.com/repolex-forx/pixeltable--pixeltable) | 2026-03-30 |
| [anthropics/claude-agent-sdk-python](https://github.com/anthropics/claude-agent-sdk-python) | v0.1.35 | [view](https://github.com/repolex-forx/anthropics--claude-agent-sdk-python) | 2026-03-30 |
| [Textualize/rich](https://github.com/Textualize/rich) | v4.2.1 | [view](https://github.com/repolex-forx/Textualize--rich) | 2026-03-30 |
| [python/typing_extensions](https://github.com/python/typing_extensions) | 4.14.0 | [view](https://github.com/repolex-forx/python--typing_extensions) | 2026-03-30 |
| [psf/requests](https://github.com/psf/requests) | v2.4.3 | [view](https://github.com/repolex-forx/psf--requests) | 2026-03-30 |
| [apache/jena](https://github.com/apache/jena) | jena-2.10.0 | [view](https://github.com/repolex-forx/apache--jena) | 2026-03-30 |
| [Jelly-RDF/jelly-jvm](https://github.com/Jelly-RDF/jelly-jvm) | v0.11.6 | [view](https://github.com/repolex-forx/Jelly-RDF--jelly-jvm) | 2026-03-30 |
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
