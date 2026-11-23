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
| [kornelski/cavif-rs](https://github.com/repolex-forx/kornelski--cavif-rs) | v1.8.0 | 2026-11-23 |
| [rust-av/dav1d-rs](https://github.com/repolex-forx/rust-av--dav1d-rs) | v0.11.1 | 2026-11-23 |
| [qnighy/libwebp-rs](https://github.com/repolex-forx/qnighy--libwebp-rs) | v0.1.2 | 2026-11-23 |
| [hsivonen/encoding_rs](https://github.com/repolex-forx/hsivonen--encoding_rs) | v0.8.40 | 2026-11-23 |
| [BurntSushi/ucd-generate](https://github.com/repolex-forx/BurntSushi--ucd-generate) | ucd-util-0.2.1 | 2026-11-23 |
| [BurntSushi/byteorder](https://github.com/repolex-forx/BurntSushi--byteorder) | 1.5.0 | 2026-11-23 |
| [diesel-rs/diesel](https://github.com/repolex-forx/diesel-rs--diesel) | v2.3.11 | 2026-11-23 |
| [BurntSushi/fst](https://github.com/repolex-forx/BurntSushi--fst) | fst-regex-0.3.0 | 2026-11-23 |
| [launchbadge/sqlx](https://github.com/repolex-forx/launchbadge--sqlx) | v0.8.5 | 2026-11-23 |
| [amodm/webbrowser-rs](https://github.com/repolex-forx/amodm--webbrowser-rs) | v1.2.3 | 2026-11-23 |
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
