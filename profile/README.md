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
| [cypress-io/cypress](https://github.com/repolex-forx/cypress-io--cypress) | v7.2.0 | 2026-09-16 |
| [pypdfium2-team/pypdfium2](https://github.com/repolex-forx/pypdfium2-team--pypdfium2) | 5.7.0 | 2026-09-16 |
| [tinylibs/tinyexec](https://github.com/repolex-forx/tinylibs--tinyexec) | 1.1.1 | 2026-09-16 |
| [laurent-laporte-pro/deprecated](https://github.com/repolex-forx/laurent-laporte-pro--deprecated) | v1.3.1 | 2026-09-16 |
| [readthedocs/sphinx-notfound-page](https://github.com/repolex-forx/readthedocs--sphinx-notfound-page) | 1.1.0 | 2026-09-16 |
| [openjdk/jdk](https://github.com/repolex-forx/openjdk--jdk) | jdk-26+15 | 2026-09-16 |
| [micromatch/picomatch](https://github.com/repolex-forx/micromatch--picomatch) | 4.0.4 | 2026-09-16 |
| [sysid/sse-starlette](https://github.com/repolex-forx/sysid--sse-starlette) | v3.3.4 | 2026-09-16 |
| [mccormicka/string-argv](https://github.com/repolex-forx/mccormicka--string-argv) | v0.3.0 | 2026-09-16 |
| [cypress-io/cypress](https://github.com/repolex-forx/cypress-io--cypress) | v7.3.0 | 2026-09-16 |
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
