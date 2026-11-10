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
- **Total Indexed Repositories**: **4,910**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`typelevel/skunk`](https://github.com/typelevel/skunk) | `1045d3b2` | Completed ✅ |
| [`dremin/RetroBar`](https://github.com/dremin/RetroBar) | `d2b0b853` | Completed ✅ |
| [`ChadCSong/ShineButton`](https://github.com/ChadCSong/ShineButton) | `91983d10` | Completed ✅ |
| [`duemunk/Async`](https://github.com/duemunk/Async) | `0004dec3` | Completed ✅ |
| [`google/zx`](https://github.com/google/zx) | `3b04a6ae` | Completed ✅ |
| [`weirdpattern/eslint-config-typescript`](https://github.com/weirdpattern/eslint-config-typescript) | `98ab70a4` | Completed ✅ |
| [`tagliala/coveralls-ruby-reborn`](https://github.com/tagliala/coveralls-ruby-reborn) | `7f6287e8` | Completed ✅ |
| [`hashicorp/go-retryablehttp`](https://github.com/hashicorp/go-retryablehttp) | `fd004584` | Completed ✅ |
| [`indexmap-rs/indexmap`](https://github.com/indexmap-rs/indexmap) | `41a87088` | Completed ✅ |
| [`mycoboco/wcwidth.js`](https://github.com/mycoboco/wcwidth.js) | `465c4042` | Completed ✅ |

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
