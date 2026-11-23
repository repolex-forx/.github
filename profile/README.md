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
| [hirezio/observer-spy](https://github.com/repolex-forx/hirezio--observer-spy) | v2.2.0 | 2026-11-23 |
| [mesqueeb/copy-anything](https://github.com/repolex-forx/mesqueeb--copy-anything) | v4.1.0 | 2026-11-23 |
| [tinylibs/tinyspy](https://github.com/repolex-forx/tinylibs--tinyspy) | v4.0.6 | 2026-11-23 |
| [facelessuser/pymdown-extensions](https://github.com/repolex-forx/facelessuser--pymdown-extensions) | 12.0.1 | 2026-11-23 |
| [redis-rs/redis-rs](https://github.com/repolex-forx/redis-rs--redis-rs) | redis-test-1.0.2 | 2026-11-23 |
| [jaraco/jaraco.itertools](https://github.com/repolex-forx/jaraco--jaraco.itertools) | v6.4.3 | 2026-11-23 |
| [coherent-oss/pytest-ignore-flaky](https://github.com/repolex-forx/coherent-oss--pytest-ignore-flaky) | v2.2.1 | 2026-11-23 |
| [django/daphne](https://github.com/repolex-forx/django--daphne) | 4.2.3 | 2026-11-23 |
| [executablebooks/sphinx-tabs](https://github.com/repolex-forx/executablebooks--sphinx-tabs) | v3.5.0 | 2026-11-23 |
| [readthedocs/sphinx-autoapi](https://github.com/repolex-forx/readthedocs--sphinx-autoapi) | v3.8.1 | 2026-11-23 |
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
