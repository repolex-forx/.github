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
| [samuelcolvin/forgettable](https://github.com/repolex-forx/samuelcolvin--forgettable) | `a411426afc` | 2026-10-10 |
| [samuelcolvin/coverage-badge](https://github.com/repolex-forx/samuelcolvin--coverage-badge) | `5b90140d73` | 2026-10-10 |
| [pallets-eco/flask-admin](https://github.com/repolex-forx/pallets-eco--flask-admin) | `9f0d23c03d` | 2026-10-10 |
| [pypa/sampleproject](https://github.com/repolex-forx/pypa--sampleproject) | `621e4974ca` | 2026-10-10 |
| [pypa/scripttest](https://github.com/repolex-forx/pypa--scripttest) | `3bebe70d11` | 2026-10-10 |
| [pypa/gh-action-pip-audit](https://github.com/repolex-forx/pypa--gh-action-pip-audit) | `fb241f5816` | 2026-10-10 |
| [pypa/distutils](https://github.com/repolex-forx/pypa--distutils) | `3ed42426ce` | 2026-10-10 |
| [pypa/gh-action-pypi-publish](https://github.com/repolex-forx/pypa--gh-action-pypi-publish) | `c0d6f8e4af` | 2026-10-10 |
| [pypa/hatch-code](https://github.com/repolex-forx/pypa--hatch-code) | `cebff56f5d` | 2026-10-10 |
| [pypa/bootstrap](https://github.com/repolex-forx/pypa--bootstrap) | `9797ac6a73` | 2026-10-10 |
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
