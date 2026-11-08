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
- **Total Indexed Repositories**: **4,760**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`UKPLab/Anonymous-LatentGraphRag`](https://github.com/UKPLab/Anonymous-LatentGraphRag) | `6d3fcb4e` | Completed ✅ |
| [`UKPLab/tmlr2026-phantom-specialization`](https://github.com/UKPLab/tmlr2026-phantom-specialization) | `1db9d331` | Completed ✅ |
| [`UKPLab/emnlp2026-reground`](https://github.com/UKPLab/emnlp2026-reground) | `36c2942f` | Completed ✅ |
| [`UKPLab/eacl2026-culturecare`](https://github.com/UKPLab/eacl2026-culturecare) | `ad950b84` | Completed ✅ |
| [`UKPLab/aaai2026-spare-prm`](https://github.com/UKPLab/aaai2026-spare-prm) | `d1076e02` | Completed ✅ |
| [`UKPLab/incorporating-relevance`](https://github.com/UKPLab/incorporating-relevance) | `454a5c75` | Completed ✅ |
| [`UKPLab/eacl2026-meta-review-as-dialog`](https://github.com/UKPLab/eacl2026-meta-review-as-dialog) | `94e80d92` | Completed ✅ |
| [`UKPLab/tacl2026-counter-review-logic`](https://github.com/UKPLab/tacl2026-counter-review-logic) | `47c8efa7` | Completed ✅ |
| [`UKPLab/tmlr2026-manifold-analysis`](https://github.com/UKPLab/tmlr2026-manifold-analysis) | `b2ac1d3a` | Completed ✅ |

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
