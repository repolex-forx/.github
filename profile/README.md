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
| [open-i18n/rust-unic](https://github.com/repolex-forx/open-i18n--rust-unic) | v0.9.0 | 2026-11-22 |
| [microsoft/rust_debugger_test](https://github.com/repolex-forx/microsoft--rust_debugger_test) | debugger_test_parser-0.2.0 | 2026-11-22 |
| [messense/rustc-test](https://github.com/repolex-forx/messense--rustc-test) | v0.9.1 | 2026-11-22 |
| [docopt/docopt.rs](https://github.com/repolex-forx/docopt--docopt.rs) | version.1 | 2026-11-22 |
| [rust-random/rngs](https://github.com/repolex-forx/rust-random--rngs) | rand_xoshiro-0.8.0-rc.0 | 2026-11-22 |
| [dtolnay/proc-macro-hack](https://github.com/repolex-forx/dtolnay--proc-macro-hack) | 0.5.20 | 2026-11-22 |
| [dtolnay/ref-cast](https://github.com/repolex-forx/dtolnay--ref-cast) | 1.0.25 | 2026-11-22 |
| [slackapi/bolt-python](https://github.com/repolex-forx/slackapi--bolt-python) | v1.28.0 | 2026-11-22 |
| [rapidfuzz/strsim-rs](https://github.com/repolex-forx/rapidfuzz--strsim-rs) | v0.11.1 | 2026-11-22 |
| [comex/rust-shlex](https://github.com/repolex-forx/comex--rust-shlex) | 1.3.0 | 2026-11-22 |
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
