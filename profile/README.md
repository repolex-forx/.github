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
- **Total Indexed Repositories**: **4,517**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`zenml-io/zenml`](https://github.com/zenml-io/zenml) | `2babcd8c` | Completed ✅ |
| [`zenml-io/kitaru`](https://github.com/zenml-io/kitaru) | `9b33e757` | Completed ✅ |
| [`zenml-io/mcp-zenml`](https://github.com/zenml-io/mcp-zenml) | `3de0643d` | Completed ✅ |
| [`zenml-io/zenml-changelog`](https://github.com/zenml-io/zenml-changelog) | `fc98ce9c` | Completed ✅ |
| [`zenml-io/zenml-io-v2`](https://github.com/zenml-io/zenml-io-v2) | `c8371c37` | Completed ✅ |
| [`zenml-io/gpudoctor`](https://github.com/zenml-io/gpudoctor) | `858554cd` | Completed ✅ |
| [`zenml-io/kitaru-skills`](https://github.com/zenml-io/kitaru-skills) | `777cd41e` | Completed ✅ |
| [`zenml-io/agent-benchmarks`](https://github.com/zenml-io/agent-benchmarks) | `d971fbe6` | Completed ✅ |
| [`zenml-io/vscode-zenml`](https://github.com/zenml-io/vscode-zenml) | `e43dcca1` | Completed ✅ |
| [`zenml-io/zenml-bench`](https://github.com/zenml-io/zenml-bench) | `3a5c89b2` | Completed ✅ |

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
