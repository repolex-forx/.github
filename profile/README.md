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
| [jazzband/web3-devkit-cli](https://github.com/repolex-forx/jazzband--web3-devkit-cli) | `402875cce9` | 2026-10-10 |
| [jazzband/django-redshift-backend](https://github.com/repolex-forx/jazzband--django-redshift-backend) | `a11625e445` | 2026-10-10 |
| [tox-dev/mdformat-zola](https://github.com/repolex-forx/tox-dev--mdformat-zola) | `bceb47770b` | 2026-10-10 |
| [tox-dev/PyVenvManage](https://github.com/repolex-forx/tox-dev--PyVenvManage) | `754fc1a3b7` | 2026-10-10 |
| [tox-dev/toml-fmt](https://github.com/repolex-forx/tox-dev--toml-fmt) | `58709e88fc` | 2026-10-10 |
| [tox-dev/tox-docker](https://github.com/repolex-forx/tox-dev--tox-docker) | `ccadc6e341` | 2026-10-10 |
| [pypa/cibuildwheel](https://github.com/repolex-forx/pypa--cibuildwheel) | `b3395e271a` | 2026-10-10 |
| [pytest-dev/pytest-bpdb](https://github.com/repolex-forx/pytest-dev--pytest-bpdb) | `c6a97b8d8b` | 2026-10-10 |
| [pytest-dev/pytest-faker](https://github.com/repolex-forx/pytest-dev--pytest-faker) | `5d21f74298` | 2026-10-10 |
| [pytest-dev/pytest-faulthandler](https://github.com/repolex-forx/pytest-dev--pytest-faulthandler) | `11cfc20668` | 2026-10-10 |
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
