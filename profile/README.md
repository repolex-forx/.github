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
- **Total Indexed Repositories**: **4,891**
- **Catalog Strategy**: Strictly WIDE (1 latest HEAD release per unique repo)
- **Local Compute Spend**: **$0.00** (100% GitHub Actions Free Cloud Runners)

### 🚀 Recently Indexed Repositories (Latest Wave)
| Repository | Commit | Status |
| :--- | :--- | :--- |
| [`airbnb/DeepLinkDispatch`](https://github.com/airbnb/DeepLinkDispatch) | `280a91f2` | Completed ✅ |
| [`devicekit/DeviceKit`](https://github.com/devicekit/DeviceKit) | `fab82bd9` | Completed ✅ |
| [`apache/avro`](https://github.com/apache/avro) | `726c25e2` | Completed ✅ |
| [`YousefED/typescript-json-schema`](https://github.com/YousefED/typescript-json-schema) | `9ec6bfce` | Completed ✅ |
| [`sinatra/sinatra`](https://github.com/sinatra/sinatra) | `cb22afd7` | Completed ✅ |
| [`hashicorp/go-cleanhttp`](https://github.com/hashicorp/go-cleanhttp) | `b0e8488e` | Completed ✅ |
| [`chronotope/chrono-tz`](https://github.com/chronotope/chrono-tz) | `64c3e4da` | Completed ✅ |
| [`ikatyang-collab/vnopts`](https://github.com/ikatyang-collab/vnopts) | `eca8ed17` | Completed ✅ |
| [`xujiyou/zhihu-flutter`](https://github.com/xujiyou/zhihu-flutter) | `c1aaaac4` | Completed ✅ |
| [`fthomas/refined`](https://github.com/fthomas/refined) | `2d9cd421` | Completed ✅ |

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
