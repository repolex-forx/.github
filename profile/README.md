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
- **Total Indexed Repositories**: **4,818**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`FilledStacks/flutter-tutorials`](https://github.com/FilledStacks/flutter-tutorials) | `ea17632f` | Completed ✅ |
| [`softwaremill/elasticmq`](https://github.com/softwaremill/elasticmq) | `73a1c655` | Completed ✅ |
| [`HMBSbige/NatTypeTester`](https://github.com/HMBSbige/NatTypeTester) | `a1935d46` | Completed ✅ |
| [`block/mdx-daemon-plugin`](https://github.com/block/mdx-daemon-plugin) | `071e4b0b` | Completed ✅ |
| [`JohnSundell/Publish`](https://github.com/JohnSundell/Publish) | `58e94304` | Completed ✅ |
| [`ulid/javascript`](https://github.com/ulid/javascript) | `11c20678` | Completed ✅ |
| [`block/goose-mobile-demo-personal-shopper`](https://github.com/block/goose-mobile-demo-personal-shopper) | `bb6876e5` | Completed ✅ |
| [`apple/device-management`](https://github.com/apple/device-management) | `9e7fdbe2` | Completed ✅ |
| [`block/finch`](https://github.com/block/finch) | `3f4bb5c0` | Completed ✅ |
| [`repolex-ai/repolex-parser-py`](https://github.com/repolex-ai/repolex-parser-py) | `4ad4d822` | Completed ✅ |

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
