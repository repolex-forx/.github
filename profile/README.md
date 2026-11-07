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
- **Total Indexed Repositories**: **4,359**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`allenai/autodiscovery-neurips`](https://github.com/allenai/autodiscovery-neurips) | `66aa2d51` | Completed ✅ |
| [`allenai/intent-aware-lfqa`](https://github.com/allenai/intent-aware-lfqa) | `7c75aa23` | Completed ✅ |
| [`allenai/autodiscovery-continual-beliefs`](https://github.com/allenai/autodiscovery-continual-beliefs) | `7962443f` | Completed ✅ |
| [`allenai/genesys`](https://github.com/allenai/genesys) | `a38edfd0` | Completed ✅ |
| [`allenai/olmo-cookbook`](https://github.com/allenai/olmo-cookbook) | `c226eb6a` | Completed ✅ |
| [`allenai/beaker-gantry`](https://github.com/allenai/beaker-gantry) | `30fa3a74` | Completed ✅ |
| [`allenai/artifact-linker`](https://github.com/allenai/artifact-linker) | `ad29148b` | Completed ✅ |
| [`allenai/S2APLER`](https://github.com/allenai/S2APLER) | `bb4bfbce` | Completed ✅ |
| [`allenai/asta-resource-repo`](https://github.com/allenai/asta-resource-repo) | `8ab06f1e` | Completed ✅ |
| [`allenai/molmospaces_policy_zoo`](https://github.com/allenai/molmospaces_policy_zoo) | `dc54f532` | Completed ✅ |
| [`scverse/scirpy`](https://github.com/scverse/scirpy) | `8496483d` | Completed ✅ |

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
