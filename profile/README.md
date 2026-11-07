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
- **Total Indexed Repositories**: **4,389**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`huggingface/safeagents`](https://github.com/huggingface/safeagents) | `0de8e22d` | Completed ✅ |
| [`huggingface/datatrove`](https://github.com/huggingface/datatrove) | `384d81c0` | Completed ✅ |
| [`huggingface/serge`](https://github.com/huggingface/serge) | `6668325d` | Completed ✅ |
| [`huggingface/relore`](https://github.com/huggingface/relore) | `06a1c99c` | Completed ✅ |
| [`huggingface/Repo2RLEnv`](https://github.com/huggingface/Repo2RLEnv) | `9d8b1557` | Completed ✅ |
| [`huggingface/jobs-actions`](https://github.com/huggingface/jobs-actions) | `10aa428c` | Completed ✅ |
| [`huggingface/research-agent`](https://github.com/huggingface/research-agent) | `d840fa46` | Completed ✅ |
| [`huggingface/pytorch-image-models`](https://github.com/huggingface/pytorch-image-models) | `43b549bf` | Completed ✅ |
| [`huggingface/hf-serve`](https://github.com/huggingface/hf-serve) | `b3ec9755` | Completed ✅ |
| [`huggingface/new-model-addition-cwm`](https://github.com/huggingface/new-model-addition-cwm) | `5baf598d` | Completed ✅ |

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
