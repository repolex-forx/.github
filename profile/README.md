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
| [samuelcolvin/json-cases](https://github.com/repolex-forx/samuelcolvin--json-cases) | `12caaa624f` | 2026-10-10 |
| [agronholm/mqttproto](https://github.com/repolex-forx/agronholm--mqttproto) | `2c416ad1d1` | 2026-10-10 |
| [mkdocstrings/griffe-tui](https://github.com/repolex-forx/mkdocstrings--griffe-tui) | 1.0.1 | 2026-10-10 |
| [samuelcolvin/pydantic-ai-pii](https://github.com/repolex-forx/samuelcolvin--pydantic-ai-pii) | `2ff638b7cd` | 2026-10-10 |
| [agronholm/smtpproto](https://github.com/repolex-forx/agronholm--smtpproto) | `75dcb6c6ac` | 2026-10-10 |
| [mkdocstrings/griffe-sphinx](https://github.com/repolex-forx/mkdocstrings--griffe-sphinx) | 0.3.1 | 2026-10-10 |
| [mkdocstrings/griffe-autodocstringstyle](https://github.com/repolex-forx/mkdocstrings--griffe-autodocstringstyle) | 0.2.2 | 2026-10-10 |
| [samuelcolvin/py-ai-mcp](https://github.com/repolex-forx/samuelcolvin--py-ai-mcp) | `d878d6478c` | 2026-10-10 |
| [mkdocstrings/griffe-public-wildcard-imports](https://github.com/repolex-forx/mkdocstrings--griffe-public-wildcard-imports) | 0.3.2 | 2026-10-10 |
| [mkdocstrings/griffe-runtime-objects](https://github.com/repolex-forx/mkdocstrings--griffe-runtime-objects) | 0.3.2 | 2026-10-10 |
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
