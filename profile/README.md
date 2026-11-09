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
### 📊 Live Index Statistics
- **Total Indexed Repositories**: **4,828**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`TopQuadrant/shacl-js`](https://github.com/TopQuadrant/shacl-js) | `7ed360b7` | Completed ✅ |
| [`isar/hive`](https://github.com/isar/hive) | `1b4febe9` | Completed ✅ |
| [`spark-jobserver/spark-jobserver`](https://github.com/spark-jobserver/spark-jobserver) | `f58280bb` | Completed ✅ |
| [`BililiveRecorder/BililiveRecorder`](https://github.com/BililiveRecorder/BililiveRecorder) | `2744d605` | Completed ✅ |
| [`block/trailblaze`](https://github.com/block/trailblaze) | `1c42e5e1` | Completed ✅ |
| [`XcodesOrg/xcodes`](https://github.com/XcodesOrg/xcodes) | `a5b72c81` | Completed ✅ |
| [`yahoo/serialize-javascript`](https://github.com/yahoo/serialize-javascript) | `4d0d8a68` | Completed ✅ |
| [`block/berd`](https://github.com/block/berd) | `a6b03407` | Completed ✅ |
| [`cucumber/cucumber-ruby`](https://github.com/cucumber/cucumber-ruby) | `0a5512bd` | Completed ✅ |
| [`block/spirit`](https://github.com/block/spirit) | `a0a8e828` | Completed ✅ |

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
