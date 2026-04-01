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
| [qos-ch/slf4j](https://github.com/qos-ch/slf4j) | v_1.6.3 | [view](https://github.com/repolex-forx/qos-ch--slf4j) | 2026-04-01 |
| [django/django](https://github.com/django/django) | 1.0 | [view](https://github.com/repolex-forx/django--django) | 2026-04-01 |
| [pallets/jinja](https://github.com/pallets/jinja) | 2.11.3 | [view](https://github.com/repolex-forx/pallets--jinja) | 2026-04-01 |
| [Textualize/rich](https://github.com/Textualize/rich) | v10.8.0 | [view](https://github.com/repolex-forx/Textualize--rich) | 2026-04-01 |
| [python-greenlet/greenlet](https://github.com/python-greenlet/greenlet) | 0.3.1 | [view](https://github.com/repolex-forx/python-greenlet--greenlet) | 2026-04-01 |
| [pallets/itsdangerous](https://github.com/pallets/itsdangerous) | 0.13 | [view](https://github.com/repolex-forx/pallets--itsdangerous) | 2026-04-01 |
| [willmcgugan/rich](https://github.com/willmcgugan/rich) | v12.5.1 | [view](https://github.com/repolex-forx/willmcgugan--rich) | 2026-04-01 |
| [qos-ch/slf4j](https://github.com/qos-ch/slf4j) | v_1.6.2 | [view](https://github.com/repolex-forx/qos-ch--slf4j) | 2026-04-01 |
| [pallets/jinja](https://github.com/pallets/jinja) | 2.11.2 | [view](https://github.com/repolex-forx/pallets--jinja) | 2026-04-01 |
| [readthedocs/sphinx_rtd_theme](https://github.com/readthedocs/sphinx_rtd_theme) | 1.3.0rc1 | [view](https://github.com/repolex-forx/readthedocs--sphinx_rtd_theme) | 2026-04-01 |
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
