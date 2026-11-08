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
- **Total Indexed Repositories**: **4,611**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`modal-labs/vhost`](https://github.com/modal-labs/vhost) | `e50f1d8a` | Completed ✅ |
| [`modal-labs/vprox`](https://github.com/modal-labs/vprox) | `4d5a397c` | Completed ✅ |
| [`cohere-ai/melody`](https://github.com/cohere-ai/melody) | `92b4073b` | Completed ✅ |
| [`cohere-ai/htn-2026-multi-agent-demo`](https://github.com/cohere-ai/htn-2026-multi-agent-demo) | `fd5c16c4` | Completed ✅ |
| [`cohere-ai/cvm-measure`](https://github.com/cohere-ai/cvm-measure) | `4f1303e2` | Completed ✅ |
| [`cohere-ai/cohere-megakernel`](https://github.com/cohere-ai/cohere-megakernel) | `67d0b9ca` | Completed ✅ |
| [`cohere-ai/north-mcp-python-sdk`](https://github.com/cohere-ai/north-mcp-python-sdk) | `06948969` | Completed ✅ |
| [`cohere-ai/vllm-skills`](https://github.com/cohere-ai/vllm-skills) | `2a9ed1ff` | Completed ✅ |
| [`explosion/ellf-templates`](https://github.com/explosion/ellf-templates) | `da035be1` | Completed ✅ |
| [`google-deepmind/reaf-sim`](https://github.com/google-deepmind/reaf-sim) | `80aa17f7` | Completed ✅ |

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
