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
- **Total Indexed Repositories**: **4,770**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`UKPLab/ukp-project-template`](https://github.com/UKPLab/ukp-project-template) | `0784f169` | Completed ✅ |
| [`UKPLab/eacl2026-assessing-paper-novelty`](https://github.com/UKPLab/eacl2026-assessing-paper-novelty) | `11887f3f` | Completed ✅ |
| [`UKPLab/eacl2026-auditing-unlearning`](https://github.com/UKPLab/eacl2026-auditing-unlearning) | `eba33614` | Completed ✅ |
| [`UKPLab/BrokerIO`](https://github.com/UKPLab/BrokerIO) | `50638fc4` | Completed ✅ |
| [`UKPLab/naacl2025-cove`](https://github.com/UKPLab/naacl2025-cove) | `4f76e18d` | Completed ✅ |
| [`UKPLab/5pils`](https://github.com/UKPLab/5pils) | `acf672a2` | Completed ✅ |
| [`UKPLab/acl2025-stricta`](https://github.com/UKPLab/acl2025-stricta) | `1c74d73f` | Completed ✅ |
| [`canonical/accountsservice-snap`](https://github.com/canonical/accountsservice-snap) | `333550cf` | Completed ✅ |
| [`canonical/ubuntu-desktop-session-snap`](https://github.com/canonical/ubuntu-desktop-session-snap) | `f8ff55e5` | Completed ✅ |
| [`canonical/transition-tracker-operator`](https://github.com/canonical/transition-tracker-operator) | `be0bd9af` | Completed ✅ |

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
