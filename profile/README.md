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
- **Total Indexed Repositories**: **4,527**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`zenml-io/kitaru-workshop`](https://github.com/zenml-io/kitaru-workshop) | `92dfd17a` | Completed ✅ |
| [`zenml-io/zenml-projects`](https://github.com/zenml-io/zenml-projects) | `544862bd` | Completed ✅ |
| [`zenml-io/zenml-product-engineer-challenge`](https://github.com/zenml-io/zenml-product-engineer-challenge) | `ae6d7799` | Completed ✅ |
| [`zenml-io/deep-research`](https://github.com/zenml-io/deep-research) | `b98b6c0a` | Completed ✅ |
| [`zenml-io/zenml-platform-engineer-challenge`](https://github.com/zenml-io/zenml-platform-engineer-challenge) | `d419c3f1` | Completed ✅ |
| [`zenml-io/zenml-enterprise-mlops`](https://github.com/zenml-io/zenml-enterprise-mlops) | `6c13ccf0` | Completed ✅ |
| [`zenml-io/zenml-solution-engineering-challenge`](https://github.com/zenml-io/zenml-solution-engineering-challenge) | `86152e0e` | Completed ✅ |
| [`zenml-io/rust-pipeline`](https://github.com/zenml-io/rust-pipeline) | `c7e8ed50` | Completed ✅ |
| [`zenml-io/template-starter`](https://github.com/zenml-io/template-starter) | `3cdcd74d` | Completed ✅ |
| [`zenml-io/zenml-gitflow`](https://github.com/zenml-io/zenml-gitflow) | `9d832d02` | Completed ✅ |

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
