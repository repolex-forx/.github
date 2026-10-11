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
| [scrapy/itemloaders](https://github.com/repolex-forx/scrapy--itemloaders) | `f3e680016d` | 2026-10-10 |
| [scrapy/queuelib](https://github.com/repolex-forx/scrapy--queuelib) | `885ef61c6a` | 2026-10-10 |
| [pytest-dev/pytest-services](https://github.com/repolex-forx/pytest-dev--pytest-services) | `bf6132c858` | 2026-10-10 |
| [pytest-dev/pytest-repeat](https://github.com/repolex-forx/pytest-dev--pytest-repeat) | `a84eaa9196` | 2026-10-10 |
| [pytest-dev/pytest-html](https://github.com/repolex-forx/pytest-dev--pytest-html) | `dd163c5408` | 2026-10-10 |
| [pytest-dev/pytest-subtests](https://github.com/repolex-forx/pytest-dev--pytest-subtests) | `1e5760131d` | 2026-10-10 |
| [pytest-dev/pytest-timeout](https://github.com/repolex-forx/pytest-dev--pytest-timeout) | `16edd491cb` | 2026-10-10 |
| [pytest-dev/pytest-randomly](https://github.com/repolex-forx/pytest-dev--pytest-randomly) | `35dcf0a5df` | 2026-10-10 |
| [pytest-dev/pytest-flask](https://github.com/repolex-forx/pytest-dev--pytest-flask) | `22120c079d` | 2026-10-10 |
| [pytest-dev/pytest-django](https://github.com/repolex-forx/pytest-dev--pytest-django) | `ad5867df0b` | 2026-10-10 |
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
