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
| [nox/serde_urlencoded](https://github.com/repolex-forx/nox--serde_urlencoded) | v0.6.1 | 2026-11-22 |
| [SergioBenitez/cookie-rs](https://github.com/repolex-forx/SergioBenitez--cookie-rs) | 0.18.2 | 2026-11-22 |
| [rust-lang/annotate-snippets-rs](https://github.com/repolex-forx/rust-lang--annotate-snippets-rs) | 0.12.16 | 2026-11-22 |
| [RustCrypto/stream-ciphers](https://github.com/repolex-forx/RustCrypto--stream-ciphers) | salsa20-v0.11.0 | 2026-11-22 |
| [snapview/tokio-tungstenite](https://github.com/repolex-forx/snapview--tokio-tungstenite) | v0.30.0 | 2026-11-22 |
| [rust-random/rand_core](https://github.com/repolex-forx/rust-random--rand_core) | v0.10.1 | 2026-11-22 |
| [BurntSushi/tabwriter](https://github.com/repolex-forx/BurntSushi--tabwriter) | tabwriter-bin-0.2.2 | 2026-11-22 |
| [hyperium/h2](https://github.com/repolex-forx/hyperium--h2) | v0.4.19 | 2026-11-22 |
| [alexcrichton/curl-rust](https://github.com/repolex-forx/alexcrichton--curl-rust) | curl-sys-0.4.90 | 2026-11-22 |
| [TeXitoi/structopt](https://github.com/repolex-forx/TeXitoi--structopt) | v0.3.26 | 2026-11-22 |
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
