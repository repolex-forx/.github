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
| [apple/servicetalk](https://github.com/apple/servicetalk) | 0.42.63 | [view](https://github.com/repolex-forx/apple--servicetalk) | 2026-04-23 |
| [pygments/pygments](https://github.com/pygments/pygments) | 2.18.0 | [view](https://github.com/repolex-forx/pygments--pygments) | 2026-04-23 |
| [cypress-io/cypress](https://github.com/cypress-io/cypress) | v13.6.2 | [view](https://github.com/repolex-forx/cypress-io--cypress) | 2026-04-23 |
| [palantir/tslint](https://github.com/palantir/tslint) | 6.1.3 | [view](https://github.com/repolex-forx/palantir--tslint) | 2026-04-23 |
| [anthropics/anthropic-sdk-csharp](https://github.com/anthropics/anthropic-sdk-csharp) | Anthropic-v12.8.0 | [view](https://github.com/repolex-forx/anthropics--anthropic-sdk-csharp) | 2026-04-23 |
| [webpack/webpack](https://github.com/webpack/webpack) | v5.83.0 | [view](https://github.com/repolex-forx/webpack--webpack) | 2026-04-23 |
| [rubocop/rubocop](https://github.com/rubocop/rubocop) | v1.86.0 | [view](https://github.com/repolex-forx/rubocop--rubocop) | 2026-04-23 |
| [rust-rdf/rdf.rs](https://github.com/rust-rdf/rdf.rs) | 0.1.1 | [view](https://github.com/repolex-forx/rust-rdf--rdf.rs) | 2026-04-23 |
| [pygments/pygments](https://github.com/pygments/pygments) | 2.19.0 | [view](https://github.com/repolex-forx/pygments--pygments) | 2026-04-23 |
| [rust-rdf/rdf.rs](https://github.com/rust-rdf/rdf.rs) | 0.2.0 | [view](https://github.com/repolex-forx/rust-rdf--rdf.rs) | 2026-04-23 |
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
