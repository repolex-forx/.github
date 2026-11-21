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
| [sean2077/jsonpath-python](https://github.com/repolex-forx/sean2077--jsonpath-python) | v1.0.5 | 2026-11-21 |
| [sphinx-doc/sphinxcontrib-devhelp](https://github.com/repolex-forx/sphinx-doc--sphinxcontrib-devhelp) | 2.0.0 | 2026-11-21 |
| [sphinx-doc/sphinxcontrib-applehelp](https://github.com/repolex-forx/sphinx-doc--sphinxcontrib-applehelp) | 2.0.0 | 2026-11-21 |
| [conduit-rust/conduit-git-http-backend](https://github.com/repolex-forx/conduit-rust--conduit-git-http-backend) | v0.10.0 | 2026-11-21 |
| [jtgeibel/rust-civet](https://github.com/repolex-forx/jtgeibel--rust-civet) | v0.12.0-alpha.0 | 2026-11-21 |
| [chrisjsewell/markdown-it-pyrs](https://github.com/repolex-forx/chrisjsewell--markdown-it-pyrs) | v0.4.0 | 2026-11-21 |
| [smol-rs/atomic-waker](https://github.com/repolex-forx/smol-rs--atomic-waker) | v1.1.2 | 2026-11-21 |
| [seanmonstar/spmc](https://github.com/repolex-forx/seanmonstar--spmc) | v0.3.0 | 2026-11-21 |
| [zkat/supports-unicode](https://github.com/repolex-forx/zkat--supports-unicode) | v3.0.0 | 2026-11-21 |
| [bluss/bencher](https://github.com/repolex-forx/bluss--bencher) | 0.1.5 | 2026-11-21 |
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
