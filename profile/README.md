# repolex-forx

**Source code as a knowledge graph.** Every repo here contains RDF graph data parsed from an open source project — abstract syntax trees, dependency graphs, LSP-enriched semantic analysis, git history, and more — all queryable with SPARQL.

## [forx-index](https://github.com/repolex-forx/forx-index) — The Catalog

The **[forx-index](https://github.com/repolex-forx/forx-index)** repo is the central catalog of everything we've parsed. It contains JSON-LD manifests that form a lightweight knowledge graph: repositories, parsed commits, and the web of dependencies between projects. Load them into any RDF tool and query with SPARQL.

## Getting Started

Install [rlex](https://github.com/repolex-ai/rlex), the query tool for repolex knowledge graphs:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Download a parsed repo:

```bash
rlex download repolex-ai/rlex
```

**rlex is designed to be used by LLMs in a terminal.** Start your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

```
"Claude, can you check the --help menu of rlex"
"Hermes, can you use the rlex tool to download someorg/somerepo"
"What classes are defined in this codebase?"
"Show me the dependency graph"
```

## Recently Parsed

<!-- AUTO-UPDATED BY FORX - DO NOT EDIT BELOW -->
| Data Source | Tag | Parsed |
|-------------|-----|--------|
| [pytest-dev/plugincompat](https://github.com/repolex-forx/pytest-dev--plugincompat) | `148b892c79` | 2026-10-11 |
| [pytest-dev/blog.pytest.org](https://github.com/repolex-forx/pytest-dev--blog.pytest.org) | `eefcfa6534` | 2026-10-11 |
| [pytest-dev/pytest-play](https://github.com/repolex-forx/pytest-dev--pytest-play) | `c39a1a7e74` | 2026-10-11 |
| [urllib3/hypercorn](https://github.com/repolex-forx/urllib3--hypercorn) | `33ed006708` | 2026-10-11 |
| [pytest-dev/design](https://github.com/repolex-forx/pytest-dev--design) | `7d3f9708bf` | 2026-10-11 |
| [samuelcolvin/python-sdk](https://github.com/repolex-forx/samuelcolvin--python-sdk) | `ebb81d3b2b` | 2026-10-11 |
| [psf/bpo-django-gae2django](https://github.com/repolex-forx/psf--bpo-django-gae2django) | `a949341b00` | 2026-10-11 |
| [pytest-dev/meta](https://github.com/repolex-forx/pytest-dev--meta) | `c26b7705e1` | 2026-10-11 |
| [bottlepy/test-docker](https://github.com/repolex-forx/bottlepy--test-docker) | `48cba1bbf1` | 2026-10-11 |
| [psf/.github](https://github.com/repolex-forx/psf--.github) | `41b2bae8ad` | 2026-10-11 |
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

*Powered by [repolex](https://repolex.ai) · Orchestrated by [forx](https://github.com/repolex-ai/forx) · Queried with [rlex](https://github.com/repolex-ai/rlex)*
