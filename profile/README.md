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
| [VoidStarKat/widestring-rs](https://github.com/repolex-forx/VoidStarKat--widestring-rs) | v1.2.1 | 2026-11-23 |
| [Manishearth/pathdiff](https://github.com/repolex-forx/Manishearth--pathdiff) | v0.2.3 | 2026-11-22 |
| [gifnksm/topological-sort-rs](https://github.com/repolex-forx/gifnksm--topological-sort-rs) | v0.3.1 | 2026-11-22 |
| [HdrHistogram/HdrHistogram_rust](https://github.com/repolex-forx/HdrHistogram--HdrHistogram_rust) | v7.6.0 | 2026-11-22 |
| [mina86/ansi_colours](https://github.com/repolex-forx/mina86--ansi_colours) | v1.2.2 | 2026-11-22 |
| [al8n/fs4](https://github.com/repolex-forx/al8n--fs4) | 1.1.0 | 2026-11-22 |
| [lunacookies/etcetera](https://github.com/repolex-forx/lunacookies--etcetera) | v0.11.0 | 2026-11-22 |
| [dropbox/rust-brotli-decompressor](https://github.com/repolex-forx/dropbox--rust-brotli-decompressor) | pre-vet-patches | 2026-11-22 |
| [rwf2/multer](https://github.com/repolex-forx/rwf2--multer) | v3.0.0 | 2026-11-22 |
| [assert-rs/predicates-rs](https://github.com/repolex-forx/assert-rs--predicates-rs) | v3.1.4 | 2026-11-22 |
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
