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
| [pyenchant/pyenchant](https://github.com/repolex-forx/pyenchant--pyenchant) | v3.3.0 | 2026-11-22 |
| [sindresorhus/tempy](https://github.com/repolex-forx/sindresorhus--tempy) | v3.2.0 | 2026-11-22 |
| [Stebalien/tempfile](https://github.com/repolex-forx/Stebalien--tempfile) | v3.27.0 | 2026-11-22 |
| [rust-cli/anstyle](https://github.com/repolex-forx/rust-cli--anstyle) | v1.0.14 | 2026-11-22 |
| [jedisct1/rust-siphash](https://github.com/repolex-forx/jedisct1--rust-siphash) | 1.0.2 | 2026-11-22 |
| [dtolnay/dissimilar](https://github.com/repolex-forx/dtolnay--dissimilar) | 1.0.11 | 2026-11-22 |
| [pyparsing/pyparsing](https://github.com/repolex-forx/pyparsing--pyparsing) | pyparsing_3.1.2 | 2026-11-22 |
| [pypa/virtualenv](https://github.com/repolex-forx/pypa--virtualenv) | 21.2.3 | 2026-11-22 |
| [apache/datafusion-python](https://github.com/repolex-forx/apache--datafusion-python) | ci-release-mode-rc1 | 2026-11-22 |
| [scikit-learn/scikit-learn](https://github.com/repolex-forx/scikit-learn--scikit-learn) | sprint01 | 2026-11-22 |
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
