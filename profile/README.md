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
| [repolex-ai/multilspy](https://github.com/repolex-ai/multilspy) | main | [view](https://github.com/repolex-forx/repolex-ai--multilspy) | 2026-09-05 |
| [hukkin/tomli-w](https://github.com/hukkin/tomli-w) | 1.2.0 | [view](https://github.com/repolex-forx/hukkin--tomli-w) | 2026-09-05 |
| [clap-rs/clap](https://github.com/clap-rs/clap) | v4.5.55 | [view](https://github.com/repolex-forx/clap-rs--clap) | 2026-05-12 |
| [run-llama/llama_index](https://github.com/run-llama/llama_index) | v0.14.20 | [view](https://github.com/repolex-forx/run-llama--llama_index) | 2026-05-12 |
| [pallets/markupsafe](https://github.com/pallets/markupsafe) | 2.1.4 | [view](https://github.com/repolex-forx/pallets--markupsafe) | 2026-05-12 |
| [tokio-rs/tokio](https://github.com/tokio-rs/tokio) | tokio-util-0.7.11 | [view](https://github.com/repolex-forx/tokio-rs--tokio) | 2026-05-12 |
| [near/near-api-rs](https://github.com/near/near-api-rs) | v0.6.0 | [view](https://github.com/repolex-forx/near--near-api-rs) | 2026-05-11 |
| [apache/airflow](https://github.com/apache/airflow) | upgrade-check/1.4.0rc2 | [view](https://github.com/repolex-forx/apache--airflow) | 2026-05-11 |
| [dtolnay/indoc](https://github.com/dtolnay/indoc) | 2.0.6 | [view](https://github.com/repolex-forx/dtolnay--indoc) | 2026-05-11 |
| [katharostech/cfg_aliases](https://github.com/katharostech/cfg_aliases) | v0.2.0 | [view](https://github.com/repolex-forx/katharostech--cfg_aliases) | 2026-05-11 |
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
