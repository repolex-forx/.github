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
| [pygments/pygments](https://github.com/pygments/pygments) | 2.17.0 | [view](https://github.com/repolex-forx/pygments--pygments) | 2026-09-05 |
| [oxigraph/oxigraph](https://github.com/oxigraph/oxigraph) | v0.5.11 | [view](https://github.com/repolex-forx/oxigraph--oxigraph) | 2026-09-05 |
| [serde-rs/serde](https://github.com/serde-rs/serde) | v1.0.229 | [view](https://github.com/repolex-forx/serde-rs--serde) | 2026-09-05 |
| [anthropics/anthropic-sdk-csharp](https://github.com/anthropics/anthropic-sdk-csharp) | Foundry-v0.4.0 | [view](https://github.com/repolex-forx/anthropics--anthropic-sdk-csharp) | 2026-09-05 |
| [repolex-ai/pan](https://github.com/repolex-ai/pan) | main | [view](https://github.com/repolex-forx/repolex-ai--pan) | 2026-09-05 |
| [repolex-ai/rlex](https://github.com/repolex-ai/rlex) | main | [view](https://github.com/repolex-forx/repolex-ai--rlex) | 2026-09-05 |
| [repolex-ai/multilspy](https://github.com/repolex-ai/multilspy) | main | [view](https://github.com/repolex-forx/repolex-ai--multilspy) | 2026-09-05 |
| [hukkin/tomli-w](https://github.com/hukkin/tomli-w) | 1.2.0 | [view](https://github.com/repolex-forx/hukkin--tomli-w) | 2026-09-05 |
| [near/near-cli-rs](https://github.com/near/near-cli-rs) | v0.23.4 | [view](https://github.com/repolex-forx/near--near-cli-rs) | 2026-05-12 |
| [apache/airflow](https://github.com/apache/airflow) | upgrade-check/1.4.0rc1 | [view](https://github.com/repolex-forx/apache--airflow) | 2026-05-12 |
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
