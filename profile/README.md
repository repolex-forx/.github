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
| [block/ospo](https://github.com/repolex-forx/block--ospo) | main | 2026-11-21 |
| [block/oss-project-template](https://github.com/repolex-forx/block--oss-project-template) | main | 2026-11-21 |
| [facebookresearch/pytorchvideo](https://github.com/repolex-forx/facebookresearch--pytorchvideo) | 0.1.3 | 2026-11-21 |
| [block/nostrino](https://github.com/repolex-forx/block--nostrino) | nostrino-0.0.7 | 2026-11-21 |
| [block/.github](https://github.com/repolex-forx/block--.github) | main | 2026-11-21 |
| [block/ln-invoice](https://github.com/repolex-forx/block--ln-invoice) | v0.0.6 | 2026-11-21 |
| [block/finch](https://github.com/repolex-forx/block--finch) | main | 2026-11-21 |
| [block/radiography](https://github.com/repolex-forx/block--radiography) | v2.10 | 2026-11-21 |
| [block/etre](https://github.com/repolex-forx/block--etre) | v0.16.1 | 2026-11-21 |
| [exa-labs/exa-py](https://github.com/repolex-forx/exa-labs--exa-py) | kronos/0.1.8709-hotfix | 2026-11-21 |
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
