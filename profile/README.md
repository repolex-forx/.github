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
| [openjdk/jdk](https://github.com/openjdk/jdk) | jdk-27+17 | [view](https://github.com/repolex-forx/openjdk--jdk) | 2026-04-18 |
| [macournoyer/thin](https://github.com/macournoyer/thin) | v1.1.0 | [view](https://github.com/repolex-forx/macournoyer--thin) | 2026-04-18 |
| [tox-dev/sphinx-autodoc-typehints](https://github.com/tox-dev/sphinx-autodoc-typehints) | 3.9.10 | [view](https://github.com/repolex-forx/tox-dev--sphinx-autodoc-typehints) | 2026-04-18 |
| [microsoft/TypeScript](https://github.com/microsoft/TypeScript) | v5.5-beta | [view](https://github.com/repolex-forx/microsoft--TypeScript) | 2026-04-18 |
| [python-trio/trio-typing](https://github.com/python-trio/trio-typing) | v0.9.0 | [view](https://github.com/repolex-forx/python-trio--trio-typing) | 2026-04-18 |
| [antlr/antlr4](https://github.com/antlr/antlr4) | runtime/Go/antlr/v4/v4.12.0 | [view](https://github.com/repolex-forx/antlr--antlr4) | 2026-04-18 |
| [jaraco/configparser](https://github.com/jaraco/configparser) | v7.1.0 | [view](https://github.com/repolex-forx/jaraco--configparser) | 2026-04-18 |
| [mkleehammer/pyodbc](https://github.com/mkleehammer/pyodbc) | 5.3.0 | [view](https://github.com/repolex-forx/mkleehammer--pyodbc) | 2026-04-18 |
| [testing-cabal/fixtures](https://github.com/testing-cabal/fixtures) | 4.3.2 | [view](https://github.com/repolex-forx/testing-cabal--fixtures) | 2026-04-18 |
| [anthropics/anthropic-sdk-csharp](https://github.com/anthropics/anthropic-sdk-csharp) | v10.0.1 | [view](https://github.com/repolex-forx/anthropics--anthropic-sdk-csharp) | 2026-04-18 |
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
