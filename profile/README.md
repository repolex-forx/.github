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
| [psf/bylaws](https://github.com/repolex-forx/psf--bylaws) | `8878278034` | 2026-10-11 |
| [psf/infra](https://github.com/repolex-forx/psf--infra) | `fe5c204dab` | 2026-10-11 |
| [encode/sentry-asgi](https://github.com/repolex-forx/encode--sentry-asgi) | `6d4c6353ad` | 2026-10-11 |
| [encode/savannah](https://github.com/repolex-forx/encode--savannah) | `291e73d455` | 2026-10-11 |
| [samuelcolvin/githubproxy](https://github.com/repolex-forx/samuelcolvin--githubproxy) | `0679cb7f60` | 2026-10-11 |
| [samuelcolvin/PaloAlto2SF](https://github.com/repolex-forx/samuelcolvin--PaloAlto2SF) | `98124cdbed` | 2026-10-11 |
| [samuelcolvin/cf-request-error](https://github.com/repolex-forx/samuelcolvin--cf-request-error) | `fbe9c4c953` | 2026-10-11 |
| [agronholm/redis-anyio](https://github.com/repolex-forx/agronholm--redis-anyio) | `cf2c8f2cc8` | 2026-10-11 |
| [agronholm/asyncfusion](https://github.com/repolex-forx/agronholm--asyncfusion) | `8697a78991` | 2026-10-11 |
| [python-trio/trimeter](https://github.com/repolex-forx/python-trio--trimeter) | `85d50671c3` | 2026-10-11 |
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
