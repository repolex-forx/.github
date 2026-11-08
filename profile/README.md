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
- **Total Indexed Repositories**: **4,780**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`UKPLab/gumbel-softmax-layer-skipping-2024`](https://github.com/UKPLab/gumbel-softmax-layer-skipping-2024) | `3f5eb5ce` | Completed ✅ |
| [`UKPLab/conspired`](https://github.com/UKPLab/conspired) | `7388d896` | Completed ✅ |
| [`UKPLab/iclr2025-obscura-coder`](https://github.com/UKPLab/iclr2025-obscura-coder) | `e7ae88a7` | Completed ✅ |
| [`UKPLab/acl2025-con-instruction`](https://github.com/UKPLab/acl2025-con-instruction) | `43124193` | Completed ✅ |
| [`UKPLab/eacl2026-abcd-link`](https://github.com/UKPLab/eacl2026-abcd-link) | `93296424` | Completed ✅ |
| [`UKPLab/emnlp2025-aspects-in-reviews`](https://github.com/UKPLab/emnlp2025-aspects-in-reviews) | `39076968` | Completed ✅ |
| [`UKPLab/emnlp2025-inferact`](https://github.com/UKPLab/emnlp2025-inferact) | `980b72d5` | Completed ✅ |
| [`UKPLab/argotario`](https://github.com/UKPLab/argotario) | `8f4bbf08` | Completed ✅ |
| [`UKPLab/qnlpai2025-ham-classifier`](https://github.com/UKPLab/qnlpai2025-ham-classifier) | `40720adc` | Completed ✅ |
| [`UKPLab/emnlp2025-poate-attack`](https://github.com/UKPLab/emnlp2025-poate-attack) | `010067ef` | Completed ✅ |

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
