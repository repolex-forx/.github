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
- **Total Indexed Repositories**: **4,732**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`canonical/hydra-operator`](https://github.com/canonical/hydra-operator) | `da50d480` | Completed ✅ |
| [`canonical/kratos-operator`](https://github.com/canonical/kratos-operator) | `f68a7740` | Completed ✅ |
| [`canonical/glauth-k8s-operator`](https://github.com/canonical/glauth-k8s-operator) | `c001d5fd` | Completed ✅ |
| [`canonical/parca-k8s-operator`](https://github.com/canonical/parca-k8s-operator) | `89fe873c` | Completed ✅ |
| [`canonical/s3-integrator`](https://github.com/canonical/s3-integrator) | `64daa19f` | Completed ✅ |
| [`qdrant/qdrant-client`](https://github.com/qdrant/qdrant-client) | `1b5bb858` | Completed ✅ |
| [`pyg-team/pyg-lib`](https://github.com/pyg-team/pyg-lib) | `d13e2066` | Completed ✅ |
| [`canonical/postgresql-operator`](https://github.com/canonical/postgresql-operator) | `009abbb6` | Completed ✅ |
| [`canonical/mysql-router-k8s-operator`](https://github.com/canonical/mysql-router-k8s-operator) | `1a5bea73` | Completed ✅ |
| [`canonical/opensearch-operator`](https://github.com/canonical/opensearch-operator) | `3148defe` | Completed ✅ |

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
