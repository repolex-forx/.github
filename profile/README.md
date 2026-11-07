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
- **Total Indexed Repositories**: **4,319**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`allenai/miles-olmo-core`](https://github.com/allenai/miles-olmo-core) | `1be18d63` | Completed ✅ |
| [`allenai/infinigram-api`](https://github.com/allenai/infinigram-api) | `d1e8b09e` | Completed ✅ |
| [`allenai/asta-autodiscovery`](https://github.com/allenai/asta-autodiscovery) | `30e080f4` | Completed ✅ |
| [`allenai/maniflow-tb`](https://github.com/allenai/maniflow-tb) | `c04eab7f` | Completed ✅ |
| [`allenai/olmoearth_pretrain_minimal`](https://github.com/allenai/olmoearth_pretrain_minimal) | `8d5aa7c8` | Completed ✅ |
| [`allenai/pier`](https://github.com/allenai/pier) | `cadf0491` | Completed ✅ |
| [`allenai/asta-bench`](https://github.com/allenai/asta-bench) | `ce758d29` | Completed ✅ |
| [`allenai/S2AND`](https://github.com/allenai/S2AND) | `fe0081df` | Completed ✅ |
| [`allenai/peS2o`](https://github.com/allenai/peS2o) | `cc4800ff` | Completed ✅ |
| [`allenai/S2AFF`](https://github.com/allenai/S2AFF) | `87dce9fd` | Completed ✅ |

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
