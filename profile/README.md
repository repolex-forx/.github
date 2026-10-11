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
| [samuelcolvin/parplot](https://github.com/repolex-forx/samuelcolvin--parplot) | `236f42423c` | 2026-10-11 |
| [samuelcolvin/qrcam](https://github.com/repolex-forx/samuelcolvin--qrcam) | `ed1fffdd9d` | 2026-10-11 |
| [tox-dev/action-pre-commit-uv](https://github.com/repolex-forx/tox-dev--action-pre-commit-uv) | `4de52c139e` | 2026-10-11 |
| [pytest-dev/pytest-nunit](https://github.com/repolex-forx/pytest-dev--pytest-nunit) | `3890ee8ed4` | 2026-10-11 |
| [pytest-dev/pytest-cloud](https://github.com/repolex-forx/pytest-dev--pytest-cloud) | `d4409d69af` | 2026-10-11 |
| [pytest-dev/pytest-talks](https://github.com/repolex-forx/pytest-dev--pytest-talks) | `6eae44166e` | 2026-10-11 |
| [pytest-dev/pytest-tcpclient](https://github.com/repolex-forx/pytest-dev--pytest-tcpclient) | `aa8b88db66` | 2026-10-11 |
| [pytest-dev/pytest-stress](https://github.com/repolex-forx/pytest-dev--pytest-stress) | `2f4a6fb8a3` | 2026-10-11 |
| [pytest-dev/pytest-splinter](https://github.com/repolex-forx/pytest-dev--pytest-splinter) | `1b0aa1efae` | 2026-10-11 |
| [pytest-dev/regendoc](https://github.com/repolex-forx/pytest-dev--regendoc) | `e6013a994f` | 2026-10-11 |
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
