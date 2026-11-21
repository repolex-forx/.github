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
| [dryrust/jq.rs](https://github.com/repolex-forx/dryrust--jq.rs) | 0.1.0 | 2026-11-21 |
| [GuillaumeGomez/doc-comment](https://github.com/repolex-forx/GuillaumeGomez--doc-comment) | v0.3.4 | 2026-11-21 |
| [baoyachi/rust_is_debug](https://github.com/repolex-forx/baoyachi--rust_is_debug) | v1.1.0 | 2026-11-21 |
| [timmywil/grunt-npmcopy](https://github.com/repolex-forx/timmywil--grunt-npmcopy) | 0.2.0 | 2026-11-21 |
| [kennethreitz/envoy](https://github.com/repolex-forx/kennethreitz--envoy) | v0.0.2 | 2026-11-21 |
| [rails/rails](https://github.com/repolex-forx/rails--rails) | `126d0d64d5` | 2026-11-10 |
| [softwaremill/macwire](https://github.com/repolex-forx/softwaremill--macwire) | `10571d5991` | 2026-11-10 |
| [zubairehman/flutter_boilerplate_project](https://github.com/repolex-forx/zubairehman--flutter_boilerplate_project) | `70657cd1e7` | 2026-11-10 |
| [total-typescript/ts-reset](https://github.com/repolex-forx/total-typescript--ts-reset) | `81b3b2614a` | 2026-11-10 |
| [rubocop/rubocop-rubycw](https://github.com/repolex-forx/rubocop--rubocop-rubycw) | `ac73b642d6` | 2026-11-10 |
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
