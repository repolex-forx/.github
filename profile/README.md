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
| [block/bundle-cache](https://github.com/repolex-forx/block--bundle-cache) | main | 2026-10-03 |
| [block/thread-manager-for-amp](https://github.com/repolex-forx/block--thread-manager-for-amp) | main | 2026-10-03 |
| [anysphere/priompt](https://github.com/repolex-forx/anysphere--priompt) | main | 2026-10-03 |
| [block/canopy](https://github.com/repolex-forx/block--canopy) | main | 2026-10-02 |
| [block/ide-metrics-plugin](https://github.com/repolex-forx/block--ide-metrics-plugin) | v0.2.14 | 2026-10-02 |
| [block/plug-and-play-template](https://github.com/repolex-forx/block--plug-and-play-template) | main | 2026-10-02 |
| [block/apple-codesign-action-example](https://github.com/repolex-forx/block--apple-codesign-action-example) | main | 2026-10-02 |
| [block/gradle-monorepo-ij-plugin](https://github.com/repolex-forx/block--gradle-monorepo-ij-plugin) | v0.1.28 | 2026-10-02 |
| [block/bazel-gradle-plugin](https://github.com/repolex-forx/block--bazel-gradle-plugin) | main | 2026-10-02 |
| [block/bitcoin-augur-reference](https://github.com/repolex-forx/block--bitcoin-augur-reference) | main | 2026-10-02 |
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
