# repolex-forx

**Source code as a knowledge graph.** Every repo here contains RDF graph data parsed from an open source project — abstract syntax trees, dependency graphs, LSP-enriched semantic analysis, git history, and more — all queryable with SPARQL.

## [forx-index](https://github.com/repolex-forx/forx-index) — The Catalog

The **[forx-index](https://github.com/repolex-forx/forx-index)** repo is the central catalog of everything we've parsed. It contains JSON-LD manifests that form a lightweight knowledge graph: repositories, parsed commits, and the web of dependencies between projects. Load them into any RDF tool and query with SPARQL.

## Getting Started

Install [lexq](https://github.com/repolex-ai/lexq), the query tool for repolex knowledge graphs:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

Download a parsed repo:

```bash
lexq download repolex-ai/lexq
```

**lexq is designed to be used by LLMs in a terminal.** Start your favorite AI assistant and ask it to use lexq. It handles the SPARQL — you just ask questions in plain English.

```
"Claude, can you check the --help menu of lexq"
"Hermes, can you use the lexq tool to download someorg/somerepo"
"What classes are defined in this codebase?"
"Show me the dependency graph"
```

## Recently Parsed

<!-- AUTO-UPDATED BY FORX - DO NOT EDIT BELOW -->
| Source | Tag | Data | Parsed |
|--------|-----|------|--------|
| [openjdk/jdk](https://github.com/openjdk/jdk) | jdk-27+1 | [view](https://github.com/repolex-forx/openjdk--jdk) | 2026-04-25 |
| [kpdecker/jsdiff](https://github.com/kpdecker/jsdiff) | v8.0.2 | [view](https://github.com/repolex-forx/kpdecker--jsdiff) | 2026-04-25 |
| [webpack/webpack](https://github.com/webpack/webpack) | v5.67.0 | [view](https://github.com/repolex-forx/webpack--webpack) | 2026-04-25 |
| [cspotcode/v8-compile-cache-lib](https://github.com/cspotcode/v8-compile-cache-lib) | v3.0.1 | [view](https://github.com/repolex-forx/cspotcode--v8-compile-cache-lib) | 2026-04-25 |
| [run-llama/llama_index](https://github.com/run-llama/llama_index) | v0.14.7 | [view](https://github.com/repolex-forx/run-llama--llama_index) | 2026-04-25 |
| [webpack/webpack](https://github.com/webpack/webpack) | v5.68.0 | [view](https://github.com/repolex-forx/webpack--webpack) | 2026-04-25 |
| [jquery/jquery](https://github.com/jquery/jquery) | 2.2.0 | [view](https://github.com/repolex-forx/jquery--jquery) | 2026-04-25 |
| [cspotcode/node-source-map-support](https://github.com/cspotcode/node-source-map-support) | v0.8.0 | [view](https://github.com/repolex-forx/cspotcode--node-source-map-support) | 2026-04-25 |
| [webpack/webpack](https://github.com/webpack/webpack) | v5.69.0 | [view](https://github.com/repolex-forx/webpack--webpack) | 2026-04-25 |
| [acornjs/acorn](https://github.com/acornjs/acorn) | v0.1 | [view](https://github.com/repolex-forx/acornjs--acorn) | 2026-04-25 |
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

*Powered by [repolex](https://repolex.ai) · Orchestrated by [forx](https://github.com/repolex-ai/forx) · Queried with [lexq](https://github.com/repolex-ai/lexq)*
