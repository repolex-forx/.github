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
| [diesel-rs/diesel](https://github.com/repolex-forx/diesel-rs--diesel) | v2.3.11 | 2026-11-23 |
| [BurntSushi/fst](https://github.com/repolex-forx/BurntSushi--fst) | fst-regex-0.3.0 | 2026-11-23 |
| [launchbadge/sqlx](https://github.com/repolex-forx/launchbadge--sqlx) | v0.8.5 | 2026-11-23 |
| [amodm/webbrowser-rs](https://github.com/repolex-forx/amodm--webbrowser-rs) | v1.2.3 | 2026-11-23 |
| [Keats/jsonwebtoken](https://github.com/repolex-forx/Keats--jsonwebtoken) | v11.0.0 | 2026-11-23 |
| [sebastienrousseau/libyml](https://github.com/repolex-forx/sebastienrousseau--libyml) | v0.0.6 | 2026-11-23 |
| [djc/rustc-version-rs](https://github.com/repolex-forx/djc--rustc-version-rs) | v0.4.1 | 2026-11-23 |
| [serde-rs/bytes](https://github.com/repolex-forx/serde-rs--bytes) | 0.11.19 | 2026-11-23 |
| [dtolnay/serde-stacker](https://github.com/repolex-forx/dtolnay--serde-stacker) | 0.1.14 | 2026-11-23 |
| [dtolnay/zmij](https://github.com/repolex-forx/dtolnay--zmij) | 1.0.23 | 2026-11-23 |
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
