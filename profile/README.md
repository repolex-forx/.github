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
| [readthedocs/sphinx-autoapi](https://github.com/repolex-forx/readthedocs--sphinx-autoapi) | v3.8.1 | 2026-11-23 |
| [sphinx-contrib/emojicodes](https://github.com/repolex-forx/sphinx-contrib--emojicodes) | v0.3.2 | 2026-11-23 |
| [dropbox/rust-brotli](https://github.com/repolex-forx/dropbox--rust-brotli) | 8.0.3 | 2026-11-23 |
| [termcolor/termcolor](https://github.com/repolex-forx/termcolor--termcolor) | 3.3.0 | 2026-11-23 |
| [wolph/portalocker](https://github.com/repolex-forx/wolph--portalocker) | v4.3.2 | 2026-11-23 |
| [rapidfuzz/Levenshtein](https://github.com/repolex-forx/rapidfuzz--Levenshtein) | v0.27.5 | 2026-11-23 |
| [carsongee/pytest-pylint](https://github.com/repolex-forx/carsongee--pytest-pylint) | v0.21.0 | 2026-11-23 |
| [pytest-dev/pytest-runner](https://github.com/repolex-forx/pytest-dev--pytest-runner) | v6.0.1 | 2026-11-23 |
| [darvid/python-hyperscan](https://github.com/repolex-forx/darvid--python-hyperscan) | v0.8.2 | 2026-11-23 |
| [DelSkayn/rquickjs](https://github.com/repolex-forx/DelSkayn--rquickjs) | v0.12.2 | 2026-11-23 |
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
