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
- **Total Indexed Repositories**: **4,702**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`canonical/self-signed-certificates-operator`](https://github.com/canonical/self-signed-certificates-operator) | `782770e0` | Completed ✅ |
| [`canonical/tls-certificates-operator`](https://github.com/canonical/tls-certificates-operator) | `12f4ccde` | Completed ✅ |
| [`canonical/sdcore-upf-operator`](https://github.com/canonical/sdcore-upf-operator) | `bfaaa490` | Completed ✅ |
| [`canonical/sdcore-amf-operator`](https://github.com/canonical/sdcore-amf-operator) | `3646c47b` | Completed ✅ |
| [`canonical/sdcore-smf-operator`](https://github.com/canonical/sdcore-smf-operator) | `fbd23c36` | Completed ✅ |
| [`canonical/sdcore-nrf-operator`](https://github.com/canonical/sdcore-nrf-operator) | `09413b5b` | Completed ✅ |
| [`canonical/sdcore-ausf-operator`](https://github.com/canonical/sdcore-ausf-operator) | `36c38567` | Completed ✅ |
| [`canonical/sdcore-udr-operator`](https://github.com/canonical/sdcore-udr-operator) | `2405e4e9` | Completed ✅ |
| [`canonical/sdcore-udm-operator`](https://github.com/canonical/sdcore-udm-operator) | `5b405fc2` | Completed ✅ |
| [`canonical/sdcore-pcf-operator`](https://github.com/canonical/sdcore-pcf-operator) | `fc84499e` | Completed ✅ |
| [`canonical/sdcore-nssf-operator`](https://github.com/canonical/sdcore-nssf-operator) | `589823f4` | Completed ✅ |
| [`canonical/sdcore-webui-operator`](https://github.com/canonical/sdcore-webui-operator) | `46a73493` | Completed ✅ |

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
