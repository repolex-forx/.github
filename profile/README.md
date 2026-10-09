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
| Data Source | Tag | Parsed |
|-------------|-----|--------|
| [modelcontextprotocol/ext-server-card](https://github.com/repolex-forx/modelcontextprotocol--ext-server-card) | main | 2026-10-09 |
| [modelcontextprotocol/use-mcp](https://github.com/repolex-forx/modelcontextprotocol--use-mcp) | v0.0.21 | 2026-10-09 |
| [modelcontextprotocol/create-python-server](https://github.com/repolex-forx/modelcontextprotocol--create-python-server) | main | 2026-10-09 |
| [modelcontextprotocol/actions](https://github.com/repolex-forx/modelcontextprotocol--actions) | main | 2026-10-09 |
| [modelcontextprotocol/ext-auth](https://github.com/repolex-forx/modelcontextprotocol--ext-auth) | main | 2026-10-09 |
| [modelcontextprotocol/access](https://github.com/repolex-forx/modelcontextprotocol--access) | main | 2026-10-09 |
| [modelcontextprotocol/experimental-ext-tool-annotations](https://github.com/repolex-forx/modelcontextprotocol--experimental-ext-tool-annotations) | main | 2026-10-09 |
| [modelcontextprotocol/ext-apps](https://github.com/repolex-forx/modelcontextprotocol--ext-apps) | v2.0.3 | 2026-10-09 |
| [modelcontextprotocol/experimental-ext-interceptors](https://github.com/repolex-forx/modelcontextprotocol--experimental-ext-interceptors) | main | 2026-10-09 |
| [modelcontextprotocol/example-remote-client](https://github.com/repolex-forx/modelcontextprotocol--example-remote-client) | main | 2026-10-09 |
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
