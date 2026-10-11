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
| [jazzband/django-embed-video](https://github.com/repolex-forx/jazzband--django-embed-video) | `2b644987ac` | 2026-10-10 |
| [jazzband/django-dbtemplates](https://github.com/repolex-forx/jazzband--django-dbtemplates) | `eab2ce0a7e` | 2026-10-10 |
| [jazzband/docopt-ng](https://github.com/repolex-forx/jazzband--docopt-ng) | `587f41a614` | 2026-10-10 |
| [jazzband/contextlib2](https://github.com/repolex-forx/jazzband--contextlib2) | `9a547a3247` | 2026-10-10 |
| [jazzband/django-recurrence](https://github.com/repolex-forx/jazzband--django-recurrence) | `14bb9b303a` | 2026-10-10 |
| [tox-dev/gh-action-tox](https://github.com/repolex-forx/tox-dev--gh-action-tox) | `65b0b019d2` | 2026-10-10 |
| [tox-dev/jetbrains-fish](https://github.com/repolex-forx/tox-dev--jetbrains-fish) | `6bc004c209` | 2026-10-10 |
| [pytest-dev/cookiecutter-pytest-plugin](https://github.com/repolex-forx/pytest-dev--cookiecutter-pytest-plugin) | `8f38e95b34` | 2026-10-10 |
| [pytest-dev/sprint](https://github.com/repolex-forx/pytest-dev--sprint) | `1a4b61d6e1` | 2026-10-10 |
| [pytest-dev/pytest-messenger](https://github.com/repolex-forx/pytest-dev--pytest-messenger) | `f91694959e` | 2026-10-10 |
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
