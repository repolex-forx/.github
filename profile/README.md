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
| [serde-rs/serde](https://github.com/repolex-forx/serde-rs--serde) | v1.0.229 | 2026-09-26 |
| [Preston-Landers/concurrent-log-handler](https://github.com/repolex-forx/Preston-Landers--concurrent-log-handler) | 0.9.27 | 2026-09-26 |
| [psf/requests](https://github.com/repolex-forx/psf--requests) | v2.13.0 | 2026-09-26 |
| [jpadilla/pyjwt](https://github.com/repolex-forx/jpadilla--pyjwt) | 1.0.0 | 2026-09-26 |
| [Textualize/rich](https://github.com/repolex-forx/Textualize--rich) | v10.11.0 | 2026-09-26 |
| [firecrawl/anydoc](https://github.com/repolex-forx/firecrawl--anydoc) | v0.1.9 | 2026-09-26 |
| [prompt-toolkit/python-prompt-toolkit](https://github.com/repolex-forx/prompt-toolkit--python-prompt-toolkit) | 3.0.24 | 2026-09-26 |
| [python-websockets/websockets](https://github.com/repolex-forx/python-websockets--websockets) | 11.0.1 | 2026-09-26 |
| [giampaolo/psutil](https://github.com/repolex-forx/giampaolo--psutil) | v5.6.2 | 2026-09-26 |
| [Python-Markdown/markdown](https://github.com/repolex-forx/Python-Markdown--markdown) | 1.7_Final | 2026-09-26 |
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
