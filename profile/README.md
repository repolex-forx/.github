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
| Data Source | Tag | Parsed |
|-------------|-----|--------|
| [webpack/webpack](https://github.com/repolex-forx/webpack--webpack) | v5.62.2 | 2026-09-14 |
| [image-rs/image](https://github.com/repolex-forx/image-rs--image) | v0.25.5 | 2026-09-14 |
| [dtolnay/unicode-ident](https://github.com/repolex-forx/dtolnay--unicode-ident) | 1.0.19 | 2026-09-14 |
| [babel/babel](https://github.com/repolex-forx/babel--babel) | v7.19.1 | 2026-09-09 |
| [huggingface/transformers](https://github.com/repolex-forx/huggingface--transformers) | v5.5.1 | 2026-09-09 |
| [webpack/webpack](https://github.com/repolex-forx/webpack--webpack) | v5.63.0 | 2026-09-09 |
| [image-rs/image](https://github.com/repolex-forx/image-rs--image) | v0.25.6 | 2026-09-09 |
| [asciidoctor/asciidoctor-tabs](https://github.com/repolex-forx/asciidoctor--asciidoctor-tabs) | v1.0.0-beta.6 | 2026-09-09 |
| [babel/babel](https://github.com/repolex-forx/babel--babel) | v7.19.2 | 2026-09-09 |
| [dtolnay/unicode-ident](https://github.com/repolex-forx/dtolnay--unicode-ident) | 1.0.20 | 2026-09-09 |
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
