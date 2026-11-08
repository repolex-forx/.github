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
- **Total Indexed Repositories**: **4,555**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`deepset-ai/spring-into-haystack`](https://github.com/deepset-ai/spring-into-haystack) | `33743038` | Completed ✅ |
| [`deepset-ai/dap-github-agent-template`](https://github.com/deepset-ai/dap-github-agent-template) | `0ee0930a` | Completed ✅ |
| [`vllm-project/production-stack`](https://github.com/vllm-project/production-stack) | `405a2fa7` | Completed ✅ |
| [`vllm-project/compressed-tensors`](https://github.com/vllm-project/compressed-tensors) | `11489fea` | Completed ✅ |
| [`argilla-io/argilla-server`](https://github.com/argilla-io/argilla-server) | `6130c634` | Completed ✅ |
| [`PrefectHQ/prefect-recipes`](https://github.com/PrefectHQ/prefect-recipes) | `ebc974b2` | Completed ✅ |
| [`cohere-ai/notebooks`](https://github.com/cohere-ai/notebooks) | `62cfb71b` | Completed ✅ |
| [`cohere-ai/sandbox-toy-semantic-search`](https://github.com/cohere-ai/sandbox-toy-semantic-search) | `c27c9174` | Completed ✅ |
| [`chroma-core/docs`](https://github.com/chroma-core/docs) | `e83a441e` | Completed ✅ |
| [`EleutherAI/cookbook`](https://github.com/EleutherAI/cookbook) | `827ee3b2` | Completed ✅ |

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
