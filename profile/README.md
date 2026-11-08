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
- **Total Indexed Repositories**: **4,722**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`canonical/cos-configuration-k8s-operator`](https://github.com/canonical/cos-configuration-k8s-operator) | `9364ce7e` | Completed ✅ |
| [`canonical/cos-proxy-operator`](https://github.com/canonical/cos-proxy-operator) | `621c314d` | Completed ✅ |
| [`canonical/loki-k8s-operator`](https://github.com/canonical/loki-k8s-operator) | `b26f8963` | Completed ✅ |
| [`canonical/tempo-k8s-operator`](https://github.com/canonical/tempo-k8s-operator) | `16d9d066` | Completed ✅ |
| [`canonical/alertmanager-k8s-operator`](https://github.com/canonical/alertmanager-k8s-operator) | `4f77240c` | Completed ✅ |
| [`canonical/grafana-agent-k8s-operator`](https://github.com/canonical/grafana-agent-k8s-operator) | `1b88dc61` | Completed ✅ |
| [`canonical/karma-k8s-operator`](https://github.com/canonical/karma-k8s-operator) | `695cabcc` | Completed ✅ |
| [`canonical/catalogue-k8s-operator`](https://github.com/canonical/catalogue-k8s-operator) | `86343dfa` | Completed ✅ |
| [`canonical/saml-integrator-operator`](https://github.com/canonical/saml-integrator-operator) | `651358e8` | Completed ✅ |
| [`canonical/oauth2-proxy-k8s-operator`](https://github.com/canonical/oauth2-proxy-k8s-operator) | `933570c2` | Completed ✅ |

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
