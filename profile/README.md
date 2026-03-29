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
| [encode/httpx](https://github.com/encode/httpx) | 0.14.3 | [view](https://github.com/repolex-forx/encode--httpx) | 2026-03-29 |
| [python/typing_extensions](https://github.com/python/typing_extensions) | 3.6.1 | [view](https://github.com/repolex-forx/python--typing_extensions) | 2026-03-29 |
| [pytest-dev/pytest](https://github.com/pytest-dev/pytest) | 1.0.0b9 | [view](https://github.com/repolex-forx/pytest-dev--pytest) | 2026-03-29 |
| [JamesNK/Newtonsoft.Json](https://github.com/JamesNK/Newtonsoft.Json) | 9.0.1 | [view](https://github.com/repolex-forx/JamesNK--Newtonsoft.Json) | 2026-03-29 |
| [encode/httpx](https://github.com/encode/httpx) | 0.13.3 | [view](https://github.com/repolex-forx/encode--httpx) | 2026-03-29 |
| [python/typing_extensions](https://github.com/python/typing_extensions) | 3.5.3.0 | [view](https://github.com/repolex-forx/python--typing_extensions) | 2026-03-29 |
| [psf/requests](https://github.com/psf/requests) | v0.12.1 | [view](https://github.com/repolex-forx/psf--requests) | 2026-03-29 |
| [trpc/trpc](https://github.com/trpc/trpc) | v8.1.4 | [view](https://github.com/repolex-forx/trpc--trpc) | 2026-03-29 |
| [pytest-dev/pytest](https://github.com/pytest-dev/pytest) | 1.0.0b8 | [view](https://github.com/repolex-forx/pytest-dev--pytest) | 2026-03-29 |
| [sdispater/tomlkit](https://github.com/sdispater/tomlkit) | 0.1.1 | [view](https://github.com/repolex-forx/sdispater--tomlkit) | 2026-03-29 |
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
