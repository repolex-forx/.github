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
| [pytest-dev/pytest-mock](https://github.com/pytest-dev/pytest-mock) | v3.15.1 | [view](https://github.com/repolex-forx/pytest-dev--pytest-mock) | 2026-04-09 |
| [kevin1024/pytest-httpbin](https://github.com/kevin1024/pytest-httpbin) | v2.1.0 | [view](https://github.com/repolex-forx/kevin1024--pytest-httpbin) | 2026-04-09 |
| [requests/httpbin](https://github.com/requests/httpbin) | v0.7.0 | [view](https://github.com/repolex-forx/requests--httpbin) | 2026-04-09 |
| [pyasn1/pyasn1](https://github.com/pyasn1/pyasn1) | v0.6.3 | [view](https://github.com/repolex-forx/pyasn1--pyasn1) | 2026-04-09 |
| [sphinx-doc/alabaster](https://github.com/sphinx-doc/alabaster) | 1.0.0 | [view](https://github.com/repolex-forx/sphinx-doc--alabaster) | 2026-04-09 |
| [pyinvoke/invoke](https://github.com/pyinvoke/invoke) | just-rebased-414 | [view](https://github.com/repolex-forx/pyinvoke--invoke) | 2026-04-09 |
| [pyca/cryptography](https://github.com/pyca/cryptography) | 46.0.7 | [view](https://github.com/repolex-forx/pyca--cryptography) | 2026-04-09 |
| [pytest-dev/pytest-cov](https://github.com/pytest-dev/pytest-cov) | v7.1.0 | [view](https://github.com/repolex-forx/pytest-dev--pytest-cov) | 2026-04-09 |
| [pypa/packaging](https://github.com/pypa/packaging) | 26.0 | [view](https://github.com/repolex-forx/pypa--packaging) | 2026-04-09 |
| [pedroburon/dotenv](https://github.com/pedroburon/dotenv) | 0.0.5 | [view](https://github.com/repolex-forx/pedroburon--dotenv) | 2026-04-09 |
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
