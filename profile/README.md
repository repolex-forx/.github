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
- **Total Indexed Repositories**: **4,439**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`argilla-io/synthetic-data-generator`](https://github.com/argilla-io/synthetic-data-generator) | `771d5d78` | Completed ✅ |
| [`argilla-io/mlflow-inference`](https://github.com/argilla-io/mlflow-inference) | `83aa0246` | Completed ✅ |
| [`argilla-io/spacy-wordnet`](https://github.com/argilla-io/spacy-wordnet) | `fddfb6f1` | Completed ✅ |
| [`argilla-io/selectra`](https://github.com/argilla-io/selectra) | `e903cce1` | Completed ✅ |
| [`argilla-io/services`](https://github.com/argilla-io/services) | `16b0c95c` | Completed ✅ |
| [`argilla-io/argilla-haystack`](https://github.com/argilla-io/argilla-haystack) | `358f4294` | Completed ✅ |
| [`argilla-io/open-human-feedback-chat`](https://github.com/argilla-io/open-human-feedback-chat) | `d8dddd15` | Completed ✅ |
| [`argilla-io/argilla-llama-index`](https://github.com/argilla-io/argilla-llama-index) | `7bd3aaae` | Completed ✅ |
| [`argilla-io/argilla-hf-dataset-sync`](https://github.com/argilla-io/argilla-hf-dataset-sync) | `8fd06190` | Completed ✅ |
| [`argilla-io/dataset-cron-refresh`](https://github.com/argilla-io/dataset-cron-refresh) | `b8b61ad2` | Completed ✅ |

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
