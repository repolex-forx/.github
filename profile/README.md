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
| [pydantic/logfire-vscode](https://github.com/repolex-forx/pydantic--logfire-vscode) | `fe7c609d07` | 2026-10-11 |
| [pydantic/connect4](https://github.com/repolex-forx/pydantic--connect4) | `339a8902e6` | 2026-10-11 |
| [pydantic/braindump](https://github.com/repolex-forx/pydantic--braindump) | `11a3431f11` | 2026-10-11 |
| [pydantic/ollama-action](https://github.com/repolex-forx/pydantic--ollama-action) | `46b8bf0ffb` | 2026-10-11 |
| [pydantic/logfire-mcp](https://github.com/repolex-forx/pydantic--logfire-mcp) | `1e11c2ce19` | 2026-10-11 |
| [pydantic/pydantic.run](https://github.com/repolex-forx/pydantic--pydantic.run) | `3fa1680b1d` | 2026-10-11 |
| [agronholm/redio](https://github.com/repolex-forx/agronholm--redio) | `6f3eab2071` | 2026-10-11 |
| [pydantic/hooky](https://github.com/repolex-forx/pydantic--hooky) | `2bd7ce0ac5` | 2026-10-11 |
| [agronholm/tzlocal](https://github.com/repolex-forx/agronholm--tzlocal) | `5c5e35ec8c` | 2026-10-11 |
| [agronholm/dummyrepo](https://github.com/repolex-forx/agronholm--dummyrepo) | `69ea67ec88` | 2026-10-11 |
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
