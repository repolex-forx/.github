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
- **Total Indexed Repositories**: **4,621**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`google-deepmind/fusion_surrogates`](https://github.com/google-deepmind/fusion_surrogates) | `f9266968` | Completed ✅ |
| [`google-deepmind/tapnet`](https://github.com/google-deepmind/tapnet) | `ceedd60b` | Completed ✅ |
| [`predibase/lora_bakeoff`](https://github.com/predibase/lora_bakeoff) | `2ac88b95` | Completed ✅ |
| [`cohere-ai/cohere-security-toolkit`](https://github.com/cohere-ai/cohere-security-toolkit) | `fb385ad2` | Completed ✅ |
| [`cohere-ai/htn-2025-techtalk`](https://github.com/cohere-ai/htn-2025-techtalk) | `9cbf9068` | Completed ✅ |
| [`cohere-ai/cohere-go`](https://github.com/cohere-ai/cohere-go) | `63f3b380` | Completed ✅ |
| [`explosion/gha-cibuildwheel`](https://github.com/explosion/gha-cibuildwheel) | `2ade48ac` | Completed ✅ |
| [`explosion/cython-blis`](https://github.com/explosion/cython-blis) | `44dd5910` | Completed ✅ |
| [`explosion/ellf-terraform-cluster`](https://github.com/explosion/ellf-terraform-cluster) | `14633726` | Completed ✅ |
| [`explosion/ellf-helm-cluster`](https://github.com/explosion/ellf-helm-cluster) | `cafcdd3e` | Completed ✅ |

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
