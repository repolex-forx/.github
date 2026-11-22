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
| [rkyv/rkyv](https://github.com/repolex-forx/rkyv--rkyv) | v0.7.43 | 2026-11-22 |
| [dtolnay/unsafe-libyaml](https://github.com/repolex-forx/dtolnay--unsafe-libyaml) | 0.2.11 | 2026-11-22 |
| [cecton/pure-rust-locales](https://github.com/repolex-forx/cecton--pure-rust-locales) | v0.8.2 | 2026-11-22 |
| [dtolnay/build-alert](https://github.com/repolex-forx/dtolnay--build-alert) | 0.1.8 | 2026-11-22 |
| [python-telegram-bot/python-telegram-bot](https://github.com/repolex-forx/python-telegram-bot--python-telegram-bot) | v22.7 | 2026-11-22 |
| [dtolnay/ryu](https://github.com/repolex-forx/dtolnay--ryu) | 1.0.23 | 2026-11-22 |
| [BurntSushi/termcolor](https://github.com/repolex-forx/BurntSushi--termcolor) | wincolor-1.0.2 | 2026-11-22 |
| [composefs/tar-rs](https://github.com/repolex-forx/composefs--tar-rs) | v0.4.0 | 2026-11-22 |
| [mitsuhiko/similar-asserts](https://github.com/repolex-forx/mitsuhiko--similar-asserts) | 2.0.0 | 2026-11-22 |
| [stub42/pytz](https://github.com/repolex-forx/stub42--pytz) | release_2026.3 | 2026-11-22 |
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
