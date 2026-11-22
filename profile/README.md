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
| [dtolnay/prettyplease](https://github.com/repolex-forx/dtolnay--prettyplease) | 0.2.37 | 2026-11-22 |
| [mgeisler/textwrap](https://github.com/repolex-forx/mgeisler--textwrap) | 0.16.2 | 2026-11-22 |
| [rust-lang/backtrace-rs](https://github.com/repolex-forx/rust-lang--backtrace-rs) | backtrace-v0.3.76 | 2026-11-22 |
| [dtolnay/semver](https://github.com/repolex-forx/dtolnay--semver) | 1.0.28 | 2026-11-22 |
| [rust-lang-nursery/lazy-static.rs](https://github.com/repolex-forx/rust-lang-nursery--lazy-static.rs) | 1.5.0 | 2026-11-22 |
| [zkat/supports-color](https://github.com/repolex-forx/zkat--supports-color) | v3.0.2 | 2026-11-22 |
| [zkat/supports-hyperlinks](https://github.com/repolex-forx/zkat--supports-hyperlinks) | v3.2.0 | 2026-11-22 |
| [documatt/sphinx-reredirects](https://github.com/repolex-forx/documatt--sphinx-reredirects) | v1.1.0 | 2026-11-22 |
| [jaraco/pytest-home](https://github.com/repolex-forx/jaraco--pytest-home) | v0.6.0 | 2026-11-22 |
| [jaraco/jaraco.envs](https://github.com/repolex-forx/jaraco--jaraco.envs) | v2.6.0 | 2026-11-22 |
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
