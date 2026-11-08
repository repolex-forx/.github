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
- **Total Indexed Repositories**: **4,651**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`UKPLab/scicoqa`](https://github.com/UKPLab/scicoqa) | `46316290` | Completed ✅ |
| [`UKPLab/arxiv2026-mic`](https://github.com/UKPLab/arxiv2026-mic) | `53ae2d45` | Completed ✅ |
| [`UKPLab/acl2026-misviz`](https://github.com/UKPLab/acl2026-misviz) | `6a6612b4` | Completed ✅ |
| [`UKPLab/acl2025-rupta`](https://github.com/UKPLab/acl2025-rupta) | `6fe68085` | Completed ✅ |
| [`UKPLab/emnlp2026-magnet`](https://github.com/UKPLab/emnlp2026-magnet) | `4030e4e5` | Completed ✅ |
| [`argilla-io/active-learning-with-rubrix`](https://github.com/argilla-io/active-learning-with-rubrix) | `ef7f7ac2` | Completed ✅ |
| [`argilla-io/coset`](https://github.com/argilla-io/coset) | `f7e56e79` | Completed ✅ |
| [`deepset-ai/haystack-home`](https://github.com/deepset-ai/haystack-home) | `f7981485` | Completed ✅ |
| [`bentoml/chatgpt-lite`](https://github.com/bentoml/chatgpt-lite) | `e4b4d641` | Completed ✅ |
| [`modal-labs/deven-martian-sentry`](https://github.com/modal-labs/deven-martian-sentry) | `2f1e6fe2` | Completed ✅ |

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
