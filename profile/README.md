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
| [rubocop/rubocop](https://github.com/rubocop/rubocop) | v1.86.1 | [view](https://github.com/repolex-forx/rubocop--rubocop) | 2026-04-22 |
| [babel/babel](https://github.com/babel/babel) | v7.22.8 | [view](https://github.com/repolex-forx/babel--babel) | 2026-04-22 |
| [webpack/webpack](https://github.com/webpack/webpack) | v5.90.0 | [view](https://github.com/repolex-forx/webpack--webpack) | 2026-04-22 |
| [rust-lang/cc-rs](https://github.com/rust-lang/cc-rs) | find-msvc-tools-v0.1.9 | [view](https://github.com/repolex-forx/rust-lang--cc-rs) | 2026-04-22 |
| [known-facts/known-errors](https://github.com/known-facts/known-errors) | 0.1.1 | [view](https://github.com/repolex-forx/known-facts--known-errors) | 2026-04-22 |
| [baoyachi/shadow-rs](https://github.com/baoyachi/shadow-rs) | v1.7.1 | [view](https://github.com/repolex-forx/baoyachi--shadow-rs) | 2026-04-22 |
| [katharostech/cfg_aliases](https://github.com/katharostech/cfg_aliases) | v0.2.1 | [view](https://github.com/repolex-forx/katharostech--cfg_aliases) | 2026-04-22 |
| [dtolnay/indoc](https://github.com/dtolnay/indoc) | 2.0.7 | [view](https://github.com/repolex-forx/dtolnay--indoc) | 2026-04-22 |
| [webpack/webpack](https://github.com/webpack/webpack) | v5.90.1 | [view](https://github.com/repolex-forx/webpack--webpack) | 2026-04-22 |
| [hyperium/mime](https://github.com/hyperium/mime) | v0.3.17 | [view](https://github.com/repolex-forx/hyperium--mime) | 2026-04-22 |
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
