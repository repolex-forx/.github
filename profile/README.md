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
- **Total Indexed Repositories**: **4,742**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`canonical/kafka-k8s-operator`](https://github.com/canonical/kafka-k8s-operator) | `a35dc739` | Completed ✅ |
| [`canonical/zookeeper-k8s-operator`](https://github.com/canonical/zookeeper-k8s-operator) | `b2692794` | Completed ✅ |
| [`canonical/mongodb-k8s-operator`](https://github.com/canonical/mongodb-k8s-operator) | `5150013a` | Completed ✅ |
| [`canonical/redis-k8s-operator`](https://github.com/canonical/redis-k8s-operator) | `06916763` | Completed ✅ |
| [`canonical/cassandra-k8s-operator`](https://github.com/canonical/cassandra-k8s-operator) | `871c3695` | Completed ✅ |
| [`canonical/grafana-k8s-operator`](https://github.com/canonical/grafana-k8s-operator) | `4a94c6df` | Completed ✅ |
| [`canonical/prometheus-scrape-config-k8s-operator`](https://github.com/canonical/prometheus-scrape-config-k8s-operator) | `ab458e76` | Completed ✅ |
| [`canonical/cos-tool`](https://github.com/canonical/cos-tool) | `3cbc09cb` | Completed ✅ |
| [`canonical/bundle-kubeflow`](https://github.com/canonical/bundle-kubeflow) | `81078875` | Completed ✅ |
| [`canonical/charmed-kubeflow-solutions`](https://github.com/canonical/charmed-kubeflow-solutions) | `099687b7` | Completed ✅ |

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
