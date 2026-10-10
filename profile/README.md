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
| [samuelcolvin/openartifact](https://github.com/repolex-forx/samuelcolvin--openartifact) | `29b03bc46c` | 2026-10-10 |
| [mkdocstrings/pytkdocs](https://github.com/repolex-forx/mkdocstrings--pytkdocs) | 0.16.5 | 2026-10-10 |
| [tox-dev/sphinx-argparse-cli](https://github.com/repolex-forx/tox-dev--sphinx-argparse-cli) | `dbdc5c366d` | 2026-10-10 |
| [samuelcolvin/check-python-version](https://github.com/repolex-forx/samuelcolvin--check-python-version) | `db74af5ee0` | 2026-10-10 |
| [samuelcolvin/tinicly](https://github.com/repolex-forx/samuelcolvin--tinicly) | `2486fa3ea4` | 2026-10-10 |
| [tox-dev/tox-extra](https://github.com/repolex-forx/tox-dev--tox-extra) | `9e16b11f7a` | 2026-10-10 |
| [tox-dev/tox-pre-commit](https://github.com/repolex-forx/tox-dev--tox-pre-commit) | `f8808711e8` | 2026-10-10 |
| [tox-dev/tox-towncrier](https://github.com/repolex-forx/tox-dev--tox-towncrier) | `ed81edcc77` | 2026-10-10 |
| [tox-dev/tox-report](https://github.com/repolex-forx/tox-dev--tox-report) | `344d0f299c` | 2026-10-10 |
| [tox-dev/xml-fmt](https://github.com/repolex-forx/tox-dev--xml-fmt) | `eb813b4479` | 2026-10-10 |
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
