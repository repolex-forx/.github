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
| [BurntSushi/quickcheck](https://github.com/repolex-forx/BurntSushi--quickcheck) | version.1 | 2026-11-22 |
| [rust-fuzz/honggfuzz-rs](https://github.com/repolex-forx/rust-fuzz--honggfuzz-rs) | v0.5.60 | 2026-11-22 |
| [rust-pretty-assertions/rust-pretty-assertions](https://github.com/repolex-forx/rust-pretty-assertions--rust-pretty-assertions) | v1.4.1 | 2026-11-22 |
| [serde-rs/test](https://github.com/repolex-forx/serde-rs--test) | 1.0.177 | 2026-11-22 |
| [harryfei/which-rs](https://github.com/repolex-forx/harryfei--which-rs) | 8.0.2 | 2026-11-22 |
| [rust-lang/jobserver-rs](https://github.com/repolex-forx/rust-lang--jobserver-rs) | 0.1.34 | 2026-11-22 |
| [open-i18n/rust-unic](https://github.com/repolex-forx/open-i18n--rust-unic) | v0.9.0 | 2026-11-22 |
| [microsoft/rust_debugger_test](https://github.com/repolex-forx/microsoft--rust_debugger_test) | debugger_test_parser-0.2.0 | 2026-11-22 |
| [messense/rustc-test](https://github.com/repolex-forx/messense--rustc-test) | v0.9.1 | 2026-11-22 |
| [docopt/docopt.rs](https://github.com/repolex-forx/docopt--docopt.rs) | version.1 | 2026-11-22 |
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
