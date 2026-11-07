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
- **Total Indexed Repositories**: **4,309**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`scrapinghub/scrapy-frontera`](https://github.com/scrapinghub/scrapy-frontera) | `56ea2e1e` | Completed ✅ |
| [`scrapinghub/hcf-backend`](https://github.com/scrapinghub/hcf-backend) | `bbdc50cd` | Completed ✅ |
| [`scrapinghub/splash`](https://github.com/scrapinghub/splash) | `ab28b023` | Completed ✅ |
| [`scrapinghub/varanus`](https://github.com/scrapinghub/varanus) | `383ef738` | Completed ✅ |
| [`scrapinghub/pastebin`](https://github.com/scrapinghub/pastebin) | `a712e603` | Completed ✅ |
| [`allenai/agent-eval`](https://github.com/allenai/agent-eval) | `28fb1751` | Completed ✅ |
| [`allenai/tutormoments`](https://github.com/allenai/tutormoments) | `f62fce98` | Completed ✅ |
| [`allenai/curobo`](https://github.com/allenai/curobo) | `87e857d4` | Completed ✅ |
| [`allenai/agentic_robotics`](https://github.com/allenai/agentic_robotics) | `340731d9` | Completed ✅ |
| [`allenai/XYBench`](https://github.com/allenai/XYBench) | `e39eb25a` | Completed ✅ |

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
